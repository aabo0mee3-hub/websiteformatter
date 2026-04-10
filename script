document.addEventListener('DOMContentLoaded', () => {
    const addBtn = document.getElementById('add-btn');
    const repoGrid = document.getElementById('repo-grid');

    addBtn.addEventListener('click', () => {
        const title = document.getElementById('asset-title').value;
        const url = document.getElementById('asset-url').value;
        const type = document.getElementById('asset-type').value;

        if (!title || !url) {
            alert("Please fill in both fields!");
            return;
        }

        createCard(title, url, type);
        clearInputs();
    });

    function createCard(title, url, type) {
        const card = document.createElement('div');
        card.className = 'repo-item';
        
        // Logical rendering based on type
        let preview = '';
        if (type === 'image') {
            preview = `<img src="${url}" style="width:100%; border-radius:4px; margin-top:10px;">`;
        }

        card.innerHTML = `
            <span class="tag">${type}</span>
            <h4 style="margin: 10px 0;">${title}</h4>
            <a href="${url}" target="_blank" style="color: #38bdf8; font-size: 13px; text-decoration: none; word-break: break-all;">${url}</a>
            ${preview}
            <div style="margin-top:15px;">
                <button onclick="this.parentElement.parentElement.remove()" style="background: #ef4444; font-size: 10px; padding: 5px 10px;">Remove</button>
            </div>
        `;

        repoGrid.prepend(card);
    }

    function clearInputs() {
        document.getElementById('asset-title').value = '';
        document.getElementById('asset-url').value = '';
    }
});
