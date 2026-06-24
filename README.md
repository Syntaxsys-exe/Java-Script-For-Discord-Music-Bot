# Java-Script-For-Discord-Music-Bot
NOTE:- Java Script For Discord, Music Bot 

















const { SlashCommandBuilder } = require('discord.js');

module.exports = {
    data: new SlashCommandBuilder()
        .setName('play')
        .setDescription('Play a song')
        .addStringOption(option =>
            option.setName('song')
                .setDescription('Song name or URL')
                .setRequired(true)
        ),

    async execute(interaction) {
        const song = interaction.options.getString('song');

        await interaction.reply(
            `🎵 Searching for: ${song}`
        );

        // Music playback logic would go here
    },
};