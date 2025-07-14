🧠 Open  AI  Based Bot🎤🖼️
A smooth and stylish Discord bot powered by OpenAI's GPT and DALL·E — now fully rebranded, cleaned, and maintained by Eshant.
This bot lets users chat with ChatGPT directly in Discord and generate AI images on command — all wrapped in a clean UI with slash commands, ephemeral responses, and a no-bloat experience.

Formerly based on Aurora AI by KrozT.
Now simplified, upgraded, and Pillow-fied by Eshant 💤

📸 Demo & Preview
Coming soon. Stay tuned for clean banners, Discord UI demos, and example responses.

⚙️ Built With
TypeScript

discord.js

OpenAI SDK

fs-extra, winston, dotenv

🚀 Features
🤖 Chat with GPT-3.5 Turbo (GPT-4 optional)

🎨 Generate AI Images using DALL·E

🧼 Clean slash command structure with ephemeral toggle

📜 Custom embeds for request/response clarity

🔧 Easy to customize and extend

🛠️ Getting Started
Prerequisites
Discord Bot Token

OpenAI API Key

Installation
bash
Copy
Edit
git clone https://github.com/Ind-Eshant/Open-Ai-based-discord-bot.git
cd Pillow-AI-Bot
pnpm install
Add your API keys to .env
env
Copy
Edit
DISCORD_API_KEY=your_token
OPENAI_API_KEY=your_openai_key
Build and Run
bash
Copy
Edit
pnpm run build
pnpm run start
🧾 Commands
Command	Type	Description
/ping	embed-info	Check if the bot is alive
/about	embed-info	About the bot
/help	embed-info	Shows all commands
/chat	embed-request / embed-response	Ask a question, get a reply
/image	embed-request / embed-response	Generate image using a prompt
/clear	embed-info	Clear bot history

🎨 Embeds Guide
Footer Tag	Color	Purpose
embed-info	Aqua	System messages
embed-error	Red	Error messages
embed-response	Green	AI-generated response
embed-request	Gold	User prompt/request

📁 Adding Your Own Commands
Create a new file in src/bot/commands/:

ts
Copy
Edit
import { Command } from '@/bot/models/command';
import { Client, CommandInteraction } from 'discord.js';

export class MyCommand extends Command {
    public configure(): void {
        this.setName('mycmd');
        this.setDescription('My custom command');
        this.addEphemeralOption();
    }

    protected async execute(client: Client, interaction: CommandInteraction): Promise<void> {
        await interaction.reply({ content: 'Hello from Eshant’s brainchild!', ephemeral: this.ephermeral });
    }
}
🛣️ Roadmap
 GPT-3.5 Chat

 DALL·E Image Generation

 Docker Support

 REST API Layer

 GPT-4 Support

 Multi-user Chat Context

 Context-based image editing

 Web dashboard (👀 maybe)

📜 License
This project is licensed under the MIT License — free to use, free to remix.

Credits to KrozT for the original version , Modified And Maintained By Eshant

🙏 Acknowledgments
OpenAI Team for the incredible APIs

Original project: Aurora AI

Eshant’s late-night motivation and infinite aura 💫 
Originally based on [Aurora AI](https://github.com/KrozT/openai-discord) by KrozT.  
Modified and maintained by Eshant.

