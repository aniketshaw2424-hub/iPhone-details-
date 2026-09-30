const iphones = [
    {
        name: "iPhone 17 Pro Max",
        year: 2025,
        display: "6.9-inch",
        type: "Pro"
    },
    {
        name: "iPhone 17 Pro",
        year: 2025,
        display: "6.3-inch",
        type: "Pro"
    },
    {
        name: "iPhone Air",
        year: 2025,
        display: "6.5-inch",
        type: "Air"
    },
    {
        name: "iPhone 17",
        year: 2025,
        display: "6.3-inch",
        type: "Standard"
    },
    {
        name: "iPhone 17e",
        year: 2026,
        display: "6.3-inch",
        type: "e"
    },

    {
        name: "iPhone 16 Pro Max",
        year: 2024,
        display: "6.9-inch",
        type: "Pro"
    },
    {
        name: "iPhone 16 Pro",
        year: 2024,
        display: "6.3-inch",
        type: "Pro"
    },
    {
        name: "iPhone 16 Plus",
        year: 2024,
        display: "6.7-inch",
        type: "Plus"
    },
    {
        name: "iPhone 16",
        year: 2024,
        display: "6.1-inch",
        type: "Standard"
    },
    {
        name: "iPhone 16e",
        year: 2025,
        display: "6.1-inch",
        type: "e"
    },

    {
        name: "iPhone 15 Pro Max",
        year: 2023,
        display: "6.7-inch",
        type: "Pro"
    },
    {
        name: "iPhone 15 Pro",
        year: 2023,
        display: "6.1-inch",
        type: "Pro"
    },
    {
        name: "iPhone 15 Plus",
        year: 2023,
        display: "6.7-inch",
        type: "Plus"
    },
    {
        name: "iPhone 15",
        year: 2023,
        display: "6.1-inch",
        type: "Standard"
    },

    {
        name: "iPhone 14 Pro Max",
        year: 2022,
        display: "6.7-inch",
        type: "Pro"
    },
    {
        name: "iPhone 14 Pro",
        year: 2022,
        display: "6.1-inch",
        type: "Pro"
    },
    {
        name: "iPhone 14 Plus",
        year: 2022,
        display: "6.7-inch",
        type: "Plus"
    },
    {
        name: "iPhone 14",
        year: 2022,
        display: "6.1-inch",
        type: "Standard"
    },

    {
        name: "iPhone 13 Pro Max",
        year: 2021,
        display: "6.7-inch",
        type: "Pro"
    },
    {
        name: "iPhone 13 Pro",
        year: 2021,
        display: "6.1-inch",
        type: "Pro"
    },
    {
        name: "iPhone 13",
        year: 2021,
        display: "6.1-inch",
        type: "Standard"
    },
    {
        name: "iPhone 13 mini",
        year: 2021,
        display: "5.4-inch",
        type: "Mini"
    },

    {
        name: "iPhone 12 Pro Max",
        year: 2020,
        display: "6.7-inch",
        type: "Pro"
    },
    {
        name: "iPhone 12 Pro",
        year: 2020,
        display: "6.1-inch",
        type: "Pro"
    },
    {
        name: "iPhone 12",
        year: 2020,
        display: "6.1-inch",
        type: "Standard"
    },
    {
        name: "iPhone 12 mini",
        year: 2020,
        display: "5.4-inch",
        type: "Mini"
    },

    {
        name: "iPhone 11 Pro Max",
        year: 2019,
        display: "6.5-inch",
        type: "Pro"
    },
    {
        name: "iPhone 11 Pro",
        year: 2019,
        display: "5.8-inch",
        type: "Pro"
    },
    {
        name: "iPhone 11",
        year: 2019,
        display: "6.1-inch",
        type: "Standard"
    },

    {
        name: "iPhone XS Max",
        year: 2018,
        display: "6.5-inch",
        type: "Standard"
    },
    {
        name: "iPhone XS",
        year: 2018,
        display: "5.8-inch",
        type: "Standard"
    },
    {
        name: "iPhone XR",
        year: 2018,
        display: "6.1-inch",
        type: "Standard"
    },

    {
        name: "iPhone X",
        year: 2017,
        display: "5.8-inch",
        type: "Standard"
    },

    {
        name: "iPhone 8 Plus",
        year: 2017,
        display: "5.5-inch",
        type: "Plus"
    },
    {
        name: "iPhone 8",
        year: 2017,
        display: "4.7-inch",
        type: "Standard"
    },

    {
        name: "iPhone 7 Plus",
        year: 2016,
        display: "5.5-inch",
        type: "Plus"
    },
    {
        name: "iPhone 7",
        year: 2016,
        display: "4.7-inch",
        type: "Standard"
    }
];


// Display phones on the website
const phoneList = document.getElementById("phoneList");

function displayPhones(list) {

    phoneList.innerHTML = "";

    list.forEach(phone => {

        const card = document.createElement("div");

        card.className = "phone-card";

        card.innerHTML = `
            <h2>${phone.name}</h2>
            <p><strong>Year:</strong> ${phone.year}</p>
            <p><strong>Display:</strong> ${phone.display}</p>
            <p><strong>Type:</strong> ${phone.type}</p>
        `;

        phoneList.appendChild(card);
    });
}


// Search
const searchBox = document.getElementById("searchBox");

searchBox.addEventListener("input", function () {

    const search = searchBox.value.toLowerCase();

    const results = iphones.filter(phone =>
        phone.name.toLowerCase().includes(search)
    );

    displayPhones(results);
});


// Show all phones when website opens
displayPhones(iphones);