document.addEventListener('DOMContentLoaded', function() {
    // Add smooth scrolling to all links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
            e.preventDefault();
            document.querySelector(this.getAttribute('href')).scrollIntoView({
                behavior: 'smooth'
            });
        });
    });

    // Popup handling
    const overlay = document.getElementById('overlay');

    const openPopupButtons = {
        'open-professional-development': 'professional-development-popup',
        'open-languages': 'languages-popup',
        'open-interests': 'interests-popup',
        'open-references': 'references-popup'
    };

    const closePopupButtons = {
        'close-professional-development': 'professional-development-popup',
        'close-languages': 'languages-popup',
        'close-interests': 'interests-popup',
        'close-references': 'references-popup'
    };

    for (let buttonId in openPopupButtons) {
        const button = document.getElementById(buttonId);
        const popup = document.getElementById(openPopupButtons[buttonId]);
        button.addEventListener('click', () => {
            overlay.style.display = 'block';
            popup.style.display = 'block';
        });
    }

    for (let buttonId in closePopupButtons) {
        const button = document.getElementById(buttonId);
        const popup = document.getElementById(closePopupButtons[buttonId]);
        button.addEventListener('click', () => {
            overlay.style.display = 'none';
            popup.style.display = 'none';
        });
    }

    overlay.addEventListener('click', () => {
        overlay.style.display = 'none';
        for (let popupId in openPopupButtons) {
            const popup = document.getElementById(openPopupButtons[popupId]);
            popup.style.display = 'none';
        }
    });
});
