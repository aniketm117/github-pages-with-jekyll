---
layout: default
title: Bharat: Journey Through History
---

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>{{ page.title }}</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://unpkg.com/lucide@latest/dist/umd/lucide.js"></script>
  <style>
    .line-clamp-3 {
      display: -webkit-box;
      -webkit-line-clamp: 3;
      -webkit-box-orient: vertical;
      overflow: hidden;
    }
  </style>
</head>
<body class="min-h-screen bg-gradient-to-br from-orange-50 via-white to-green-50">
  <!-- Header -->
  <div class="bg-gradient-to-r from-orange-600 to-green-600 text-white p-6 shadow-lg">
    <div class="max-w-6xl mx-auto">
      <h1 class="text-3xl font-bold flex items-center gap-2">
        <i data-lucide="sparkles" class="w-8 h-8"></i>
        Bharat: Journey Through History
      </h1>
      <p class="text-orange-100 mt-2">Discover the rich heritage and timeless wisdom of India</p>
    </div>
  </div>

  <!-- Navigation -->
  <div class="max-w-6xl mx-auto mt-6 px-4">
    <div class="flex gap-4 border-b border-gray-200">
      <button data-tab="daily" class="tab-btn px-6 py-3 font-medium transition-all flex items-center gap-2">
        <i data-lucide="calendar" class="w-5 h-5"></i>
        Daily Fact
      </button>
      <button data-tab="explore" class="tab-btn px-6 py-3 font-medium transition-all flex items-center gap-2">
        <i data-lucide="clock" class="w-5 h-5"></i>
        Explore Timeline
      </button>
      <button data-tab="books" class="tab-btn px-6 py-3 font-medium transition-all flex items-center gap-2">
        <i data-lucide="book" class="w-5 h-5"></i>
        Historical Texts
      </button>
    </div>
  </div>

  <!-- Content -->
  <div class="max-w-6xl mx-auto mt-8 px-4 pb-12">
    <!-- Daily Fact Tab -->
    <div id="daily-tab" class="tab-content hidden bg-white rounded-lg shadow-xl p-8 border-l-4 border-orange-600">
      <div class="flex items-center gap-2 text-orange-600 mb-4">
        <i data-lucide="calendar" class="w-6 h-6"></i>
        <span class="font-semibold">Today's Historical Insight</span>
      </div>
      <div id="daily-fact-content"></div>
    </div>

    <!-- Explore Timeline Tab -->
    <div id="explore-tab" class="tab-content hidden">
      <div class="flex gap-4 mb-6 flex-wrap">
        <button data-era="all" class="era-btn px-4 py-2 rounded-lg font-medium transition-all bg-gray-200 text-gray-700 hover:bg-gray-300">
          All Eras
        </button>
        <button data-era="ancient" class="era-btn px-4 py-2 rounded-lg font-medium transition-all bg-gray-200 text-gray-700 hover:bg-gray-300">
          Ancient (3300 BCE - 500 CE)
        </button>
        <button data-era="medieval" class="era-btn px-4 py-2 rounded-lg font-medium transition-all bg-gray-200 text-gray-700 hover:bg-gray-300">
          Medieval (500 - 1800 CE)
        </button>
        <button data-era="modern" class="era-btn px-4 py-2 rounded-lg font-medium transition-all bg-gray-200 text-gray-700 hover:bg-gray-300">
          Modern (1800 - Present)
        </button>
      </div>

      <div id="facts-grid" class="space-y-6"></div>
    </div>

    <!-- Historical Books Tab -->
    <div id="books-tab" class="tab-content hidden">
      <div class="mb-6">
        <div class="relative">
          <i data-lucide="search" class="absolute left-3 top-3 w-5 h-5 text-gray-400"></i>
          <input type="text" id="search-input" placeholder="Search books by title, content, or themes..." class="w-full pl-10 pr-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500">
        </div>
      </div>

      <div id="book-detail" class="hidden bg-white rounded-lg shadow-xl p-8">
        <button id="back-to-books" class="text-orange-600 hover:text-orange-700 mb-4 flex items-center gap-2">
          <i data-lucide="arrow-left" class="w-4 h-4"></i>
          Back to all books
        </button>
        <div id="book-detail-content"></div>
      </div>

      <div id="books-grid" class="grid gap-6"></div>
    </div>
  </div>

  <script>
    // Initialize Lucide icons
    lucide.createIcons();

    // Historical facts database
    const historicalFacts = {
      ancient: [
        {
          title: "Indus Valley Civilization",
          period: "3300-1300 BCE",
          fact: "The Indus Valley Civilization was one of the world's earliest urban civilizations, featuring advanced city planning with grid-pattern streets, sophisticated drainage systems, and standardized weights and measures. Cities like Mohenjo-daro and Harappa had multi-story buildings and public baths.",
          context: "This civilization predated the Egyptian pyramids and was contemporary with ancient Mesopotamia, showcasing Bharat's early contribution to human civilization."
        },
        {
          title: "Vedic Period Mathematics",
          period: "1500-500 BCE",
          fact: "The concept of zero as a number was developed in ancient Bharat during the Vedic period. The Rigveda contains hymns that discuss mathematical concepts, and the Sulba Sutras (800-500 BCE) contain geometric principles including an approximation of π and the Pythagorean theorem.",
          context: "This mathematical innovation would later spread to the Arab world and Europe, fundamentally changing mathematics globally."
        },
        {
          title: "Takshashila University",
          period: "5th Century BCE",
          fact: "Takshashila (Taxila) was one of the world's first universities, attracting students from across Asia. It offered over 60 subjects including medicine, astronomy, mathematics, politics, and warfare. The renowned scholar Chanakya taught here.",
          context: "At its peak, Takshashila hosted over 10,000 students, making it a global center of learning centuries before European universities."
        }
      ],
      medieval: [
        {
          title: "Nalanda University",
          period: "5th-12th Century CE",
          fact: "Nalanda University was a residential center of learning with a library called Dharmaganja containing nine million manuscripts. The library was so vast it reportedly burned for three months when destroyed in 1193 CE. Scholars like Aryabhata and Xuanzang studied here.",
          context: "Nalanda attracted students from Tibet, China, Korea, Japan, and Central Asia, making it truly international in scope."
        },
        {
          title: "Chola Naval Empire",
          period: "9th-13th Century CE",
          fact: "The Chola Dynasty established one of the most powerful naval forces in Asian history. Raja Raja Chola I and Rajendra Chola I extended their maritime empire to Southeast Asia, conquering territories in present-day Malaysia, Indonesia, and Thailand.",
          context: "The Chola naval expeditions spread Indian culture, art, and architecture across Southeast Asia, evidenced by temples like Angkor Wat."
        },
        {
          title: "Delhi Sultanate Architecture",
          period: "1206-1526 CE",
          fact: "The Qutub Minar, built by Qutb ud-Din Aibak, stands at 73 meters and is the tallest brick minaret in the world. It showcases the fusion of Islamic and Indian architectural styles, with intricate carvings and calligraphy.",
          context: "This period saw the introduction of the arch, dome, and true vaulting in Indian architecture, blending with traditional Indian design elements."
        }
      ],
      modern: [
        {
          title: "The Revolt of 1857",
          period: "1857",
          fact: "The Indian Rebellion of 1857, also called the First War of Independence, began in Meerut and spread across northern and central India. Led by figures like Rani Lakshmibai, Bahadur Shah Zafar, and Mangal Pandey, it challenged British East India Company rule.",
          context: "Though suppressed, this rebellion marked the beginning of organized resistance to colonial rule and led to the British Crown taking direct control of India."
        },
        {
          title: "Indian National Congress Formation",
          period: "1885",
          fact: "The Indian National Congress was founded by Allan Octavian Hume, Dadabhai Naoroji, and Dinshaw Wacha in Mumbai. It initially sought greater Indian participation in governance but evolved into the primary vehicle for the independence movement.",
          context: "From 72 delegates at its first session, the INC grew to lead a mass movement that eventually achieved independence through non-violent resistance."
        },
        {
          title: "Independence and Partition",
          period: "1947",
          fact: "India gained independence on August 15, 1947, ending nearly 200 years of British rule. The partition created India and Pakistan, resulting in one of the largest mass migrations in human history with 10-20 million people displaced.",
          context: "Despite the tragedy of partition, India emerged as the world's largest democracy, adopting a constitution that guaranteed fundamental rights to all citizens."
        }
      ]
    };

    // Historical books database
    const historicalBooks = [
      {
        id: 1,
        title: "Arthashastra by Kautilya (Chanakya)",
        period: "4th Century BCE",
        summary: "The Arthashastra is an ancient Indian treatise on statecraft, economic policy, and military strategy. Written by Chanakya (also known as Kautilya), it served as a guide for Emperor Chandragupta Maurya. The text covers governance, law, economics, diplomacy, and warfare with remarkable sophistication.",
        themes: ["Statecraft", "Economics", "Military Strategy", "Governance"]
      },
      {
        id: 2,
        title: "Mahabharata",
        period: "400 BCE - 400 CE (composition period)",
        summary: "The Mahabharata is the world's longest epic poem, containing over 100,000 verses. Attributed to sage Vyasa, it narrates the Kurukshetra War between the Pandavas and Kauravas, but encompasses profound philosophical teachings, particularly the Bhagavad Gita.",
        themes: ["Dharma", "War", "Philosophy", "Ethics"]
      },
      {
        id: 3,
        title: "Ramayana by Valmiki",
        period: "5th-4th Century BCE",
        summary: "The Ramayana, composed by sage Valmiki, tells the story of Prince Rama's exile, his wife Sita's abduction by demon king Ravana, and her eventual rescue. Comprising 24,000 verses in seven books, it is both an epic narrative and a moral guide.",
        themes: ["Dharma", "Devotion", "Ideal Governance", "Virtue"]
      },
      {
        id: 4,
        title: "The Discovery of India by Jawaharlal Nehru",
        period: "1946",
        summary: "Written by India's first Prime Minister Jawaharlal Nehru during his imprisonment in Ahmednagar Fort (1942-1946), this book is a comprehensive survey of Indian history, culture, and philosophy.",
        themes: ["History", "Philosophy", "Nationalism", "Culture"]
      },
      {
        id: 5,
        title: "Indica by Megasthenes",
        period: "4th Century BCE",
        summary: "Indica is an account of India written by Megasthenes, the Greek ambassador to the Mauryan court of Chandragupta Maurya. Though the original text is lost, fragments preserved in later works provide valuable insights into ancient Indian society.",
        themes: ["Ancient India", "Mauryan Empire", "Foreign Perspective", "Society"]
      }
    ];

    let activeTab = 'daily';
    let selectedEra = 'all';
    let searchQuery = '';
    let selectedBook = null;

    // Initialize app
    function initApp() {
      loadDailyFact();
      setupEventListeners();
      renderBooks();
      renderFacts();
      lucide.createIcons();
    }

    // Load daily fact
    function loadDailyFact() {
      const today = new Date();
      const dayOfYear = Math.floor((today - new Date(today.getFullYear(), 0, 0)) / 1000 / 60 / 60 / 24);
      const allFacts = [...historicalFacts.ancient, ...historicalFacts.medieval, ...historicalFacts.modern];
      const factIndex = dayOfYear % allFacts.length;
      const dailyFact = allFacts[factIndex];
      
      document.getElementById('daily-fact-content').innerHTML = `
        <h2 class="text-2xl font-bold text-gray-800 mb-2">${dailyFact.title}</h2>
        <p class="text-sm text-gray-500 mb-4">${dailyFact.period}</p>
        <p class="text-gray-700 leading-relaxed mb-4">${dailyFact.fact}</p>
        <div class="bg-orange-50 p-4 rounded-lg border-l-4 border-orange-300">
          <p class="text-sm font-semibold text-orange-800 mb-2">Historical Context:</p>
          <p class="text-gray-700 leading-relaxed">${dailyFact.context}</p>
        </div>
      `;
    }

    // Setup event listeners
    function setupEventListeners() {
      // Tab switching
      document.querySelectorAll('.tab-btn').forEach(btn => {
        btn.addEventListener('click', () => {
          activeTab = btn.dataset.tab;
          switchTab();
        });
      });

      // Era filtering
      document.querySelectorAll('.era-btn').forEach(btn => {
        btn.addEventListener('click', () => {
          selectedEra = btn.dataset.era;
          updateEraButtons();
          renderFacts();
        });
      });

      // Search
      document.getElementById('search-input').addEventListener('input', (e) => {
        searchQuery = e.target.value;
        renderBooks();
      });

      // Back to books
      document.getElementById('back-to-books').addEventListener('click', () => {
        selectedBook = null;
        document.getElementById('book-detail').classList.add('hidden');
        document.getElementById('books-grid').classList.remove('hidden');
        renderBooks();
      });
    }

    // Switch tabs
    function switchTab() {
      document.querySelectorAll('.tab-content').forEach(content => {
        content.classList.add('hidden');
      });
      document.querySelectorAll('.tab-btn').forEach(btn => {
        btn.classList.remove('border-b-2', 'border-orange-600', 'text-orange-600');
        btn.classList.add('text-gray-600', 'hover:text-orange-600');
      });

      document.getElementById(`${activeTab}-tab`).classList.remove('hidden');
      document.querySelector(`[data-tab="${activeTab}"]`).classList.add('border-b-2', 'border-orange-600', 'text-orange-600');
      document.querySelector(`[data-tab="${activeTab}"]`).classList.remove('text-gray-600', 'hover:text-orange-600');

      if (activeTab === 'daily') loadDailyFact();
      if (activeTab === 'explore') renderFacts();
      if (activeTab === 'books') renderBooks();
    }

    // Update era buttons
    function updateEraButtons() {
      document.querySelectorAll('.era-btn').forEach(btn => {
        btn.classList.remove('bg-orange-600', 'text-white');
        btn.classList.add('bg-gray-200', 'text-gray-700', 'hover:bg-gray-300');
        if (btn.dataset.era === selectedEra) {
          btn.classList.remove('bg-gray-200', 'text-gray-700', 'hover:bg-gray-300');
          btn.classList.add('bg-orange-600', 'text-white');
        }
      });
    }

    // Get filtered facts
    function getFilteredFacts() {
      if (selectedEra === 'all') {
        return [...historicalFacts.ancient, ...historicalFacts.medieval, ...historicalFacts.modern];
      }
      return historicalFacts[selectedEra] || [];
    }

    // Render facts
    function renderFacts() {
      const facts = getFilteredFacts();
      const container = document.getElementById('facts-grid');
      container.innerHTML = facts.map(fact => `
        <div class="bg-white rounded-lg shadow-lg p-6 hover:shadow-xl transition-shadow">
          <div class="flex items-start gap-4">
            <div class="bg-orange-100 p-3 rounded-full">
              <i data-lucide="chevron-right" class="w-6 h-6 text-orange-600"></i>
            </div>
            <div class="flex-1">
              <h3 class="text-xl font-bold text-gray-800 mb-1">${fact.title}</h3>
              <p class="text-sm text-orange-600 font-semibold mb-3">${fact.period}</p>
              <p class="text-gray-700 leading-relaxed mb-4">${fact.fact}</p>
              <div class="bg-green-50 p-4 rounded-lg">
                <p class="text-sm font-semibold text-green-800 mb-2">Context:</p>
                <p class="text-gray-700 text-sm leading-relaxed">${fact.context}</p>
              </div>
            </div>
          </div>
        </div>
      `).join('');
      lucide.createIcons();
    }

    // Get filtered books
    function getFilteredBooks() {
      if (!searchQuery) return historicalBooks;
      return historicalBooks.filter(book => 
        book.title.toLowerCase().includes(searchQuery.toLowerCase()) ||
        book.summary.toLowerCase().includes(searchQuery.toLowerCase()) ||
        book.themes.some(theme => theme.toLowerCase().includes(searchQuery.toLowerCase()))
      );
    }

    // Render books
    function renderBooks() {
      const books = getFilteredBooks();
      const container = document.getElementById('books-grid');
      container.innerHTML = books.map(book => `
        <div class="bg-white rounded-lg shadow-lg p-6 hover:shadow-xl transition-all cursor-pointer book-card" data-book-id="${book.id}">
          <div class="flex items-start gap-4">
            <div class="bg-orange-100 p-3 rounded-lg">
              <i data-lucide="file-text" class="w-8 h-8 text-orange-600"></i>
            </div>
            <div class="flex-1">
              <h3 class="text-xl font-bold text-gray-800 mb-1">${book.title}</h3>
              <p class="text-sm text-orange-600 font-semibold mb-3">${book.period}</p>
              <p class="text-gray-600 leading-relaxed mb-4 line-clamp-3">${book.summary}</p>
              <div class="flex flex-wrap gap-2">
                ${book.themes.map(theme => `<span class="bg-gray-100 text-gray-700 px-2 py-1 rounded text-xs font-medium">${theme}</span>`).join('')}
              </div>
            </div>
          </div>
        </div>
      `).join('');

      // Add click listeners to book cards
      document.querySelectorAll('.book-card').forEach(card => {
        card.addEventListener('click', () => {
          const bookId = parseInt(card.dataset.bookId);
          selectedBook = historicalBooks.find(b => b.id === bookId);
          showBookDetail();
        });
      });

      lucide.createIcons();
    }

    // Show book detail
    function showBookDetail() {
      const detailContainer = document.getElementById('book-detail');
      const booksGrid = document.getElementById('books-grid');
      
      detailContainer.classList.remove('hidden');
      booksGrid.classList.add('hidden');
      
      document.getElementById('book-detail-content').innerHTML = `
        <h2 class="text-3xl font-bold text-gray-800 mb-2">${selectedBook.title}</h2>
        <p class="text-orange-600 font-semibold mb-6">${selectedBook.period}</p>
        <h3 class="text-xl font-bold text-gray-800 mb-3">Summary</h3>
        <p class="text-gray-700 leading-relaxed mb-6">${selectedBook.summary}</p>
        <h3 class="text-xl font-bold text-gray-800 mb-3">Key Themes</h3>
        <div class="flex flex-wrap gap-2">
          ${selectedBook.themes.map(theme => `<span class="bg-orange-100 text-orange-800 px-3 py-1 rounded-full text-sm font-medium">${theme}</span>`).join('')}
        </div>
      `;
      lucide.createIcons();
    }

    // Initialize when DOM is loaded
    document.addEventListener('DOMContentLoaded', initApp);
  </script>
</body>
</html>
