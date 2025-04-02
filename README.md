# Samy-Ai
Cc❤️‍🩹moi c'est samy AI🥺 j'suis la pour répondre à tout vos questions 💋❤️‍🩹
const { Client, LocalAuth } = require('whatsapp-web.js'); const qrcode = require('qrcode-terminal'); const axios = require('axios'); const fs = require('fs');

const client = new Client({ authStrategy: new LocalAuth() });

client.on('qr', qr => { console.log('Scannez ce QR Code avec WhatsApp Web pour connecter le bot :'); qrcode.generate(qr, { small: true }); });

client.on('ready', () => { console.log('🚀 Bot WhatsApp prêt à l'emploi !'); });

// Liste des commandes avancées const commands = { 'bonjour': '👋 Salut ! Comment puis-je vous aider ?', 'date': 📅 Nous sommes le ${new Date().toLocaleDateString()}., 'heure': ⏰ Il est actuellement ${new Date().toLocaleTimeString()}., 'aide': '🛠 Liste des commandes : bonjour, date, heure, blague, sticker, yt, tiktok.', 'blague': '😂 Pourquoi les plongeurs plongent-ils toujours en arrière ? Parce que sinon ils tombent dans le bateau !', };

client.on('message', async message => { console.log(Message reçu de ${message.from}: ${message.body}); const command = message.body.toLowerCase();

if (commands[command]) {
    message.reply(commands[command]);
} else if (command.startsWith('!sticker')) {
    // Convertir une image en sticker
    message.reply('📸 Envoi une image pour créer un sticker !');
} else if (command.startsWith('!yt ')) {
    const url = command.split(' ')[1];
    message.reply(`🎬 Téléchargement de la vidéo YouTube en cours : ${url}`);
    // Implémentation API YouTube nécessaire
} else if (command.startsWith('!tiktok ')) {
    const url = command.split(' ')[1];
    message.reply(`🎵 Téléchargement de la vidéo TikTok en cours : ${url}`);
    // Implémentation API TikTok nécessaire
} else if (command.startsWith('!gpt ')) {
    const query = command.replace('!gpt ', '');
    message.reply(`🤖 Réponse de ChatGPT en cours pour : ${query}`);
    // Implémentation API ChatGPT nécessaire
}

});

client.initialize();
const { Client, LocalAuth } = require('whatsapp-web.js');
const qrcode = require('qrcode-terminal');
const axios = require('axios');
const fs = require('fs');

const client = new Client({
    authStrategy: new LocalAuth()
});

client.on('qr', qr => {
    console.log('Scannez ce QR Code avec WhatsApp Web pour connecter le bot :');
    qrcode.generate(qr, { small: true });
});

client.on('ready', () => {
    console.log('🚀 Bot WhatsApp prêt à l'emploi !');
});

const menuMessage = `
┏━━━━━━━━⚜️ Bot-MD ⚜️━━━━━━━━┓
┃
┃   *Préfixe* : 🔥
┃   *Mode* : Public
┃   *Commandes* : 192
┃   *Date* : ${new Date().toLocaleDateString()}
┃   *Heure* : ${new Date().toLocaleTimeString()}
┃   *Mémoire* : 1.31 GB/15.62 GB
┃   *Plateforme* : Linux
┃   *Développeur* : Toi
┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

🎛️ 𝐅𝐞𝐚𝐭𝐮𝐫𝐞𝐬
┌───────────────┐
│ *❯ IA*
│ *❯ General*
│ *❯ Mods*
│ *❯ Group*
│ *❯ Fun*
│ *❯ Search*
│ *❯ Conversion*
│ *❯ Audio-Edit*
│ *❯ Image-Edit*
│ *❯ Games*
│ *❯ Hentai*
│ *❯ Params*
│ *❯ Download*
│ *❯ Logo*
│ *❯ Recherche*
│ *❯ Reaction*
│ *❯ Stickers*
│ *❯ TTS*
│ *❯ Weeb*
└───────────────┘

Utilisez 🔥 suivi de la commande !
`;

client.on('message', async message => {
    console.log(`Message reçu de ${message.from}: ${message.body}`);
    const command = message.body.toLowerCase();

    if (command === '.menu') {
        message.reply(menuMessage);
    } else if (command.startsWith('!sticker')) {
        message.reply('📸 Envoi une image pour créer un sticker !');
    } else if (command.startsWith('!yt ')) {
        const url = command.split(' ')[1];
        message.reply(`🎬 Téléchargement de la vidéo YouTube en cours : ${url}`);
    } else if (command.startsWith('!tiktok ')) {
        const url = command.split(' ')[1];
        message.reply(`🎵 Téléchargement de la vidéo TikTok en cours : ${url}`);
    } else if (command.startsWith('!gpt ')) {
        const query = command.replace('!gpt ', '');
        message.reply(`🤖 Réponse de ChatGPT en cours pour : ${query}`);
    }
});

client.initialize();



