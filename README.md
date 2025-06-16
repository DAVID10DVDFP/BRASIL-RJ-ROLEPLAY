# BRASIL-RJ-ROLEPLAY
O MELHOR JOGO PRA VC JOGAR 
import { useEffect, useState } from "react"; import { Card, CardContent } from "@/components/ui/card";

export default function Home() { const [serverStatus, setServerStatus] = useState("Carregando...");

useEffect(() => { // Simulação de status do servidor setTimeout(() => { setServerStatus("🟢 Online com 128 jogadores"); }, 1000); }, []);

return ( <div className="min-h-screen bg-gradient-to-b from-black via-gray-900 to-gray-800 text-white p-4"> <header className="text-center py-10"> <h1 className="text-5xl font-bold">Rio Rise RP</h1> <p className="text-lg mt-2">O mundo virtual onde sua história começa</p> </header>

<main className="grid gap-6 max-w-4xl mx-auto">
    <Card className="bg-gray-900 border-gray-700">
      <CardContent className="p-6">
        <h2 className="text-2xl font-semibold mb-2">Status do Servidor</h2>
        <p>{serverStatus}</p>
      </CardContent>
    </Card>

    <Card className="bg-gray-900 border-gray-700">
      <CardContent className="p-6">
        <h2 className="text-2xl font-semibold mb-4">Últimas Notícias</h2>
        <ul className="space-y-2">
          <li>
            <strong>[16/06/2025]</strong> Nova atualização com sistema de facções e veículos importados!
          </li>
          <li>
            <strong>[10/06/2025]</strong> Servidor 100% otimizado para mobile!
          </li>
        </ul>
      </CardContent>
    </Card>
  </main>

  <footer className="text-center text-sm text-gray-500 mt-10">
    &copy; 2025 Rio Rise RP. Todos os direitos reservados.
  </footer>
</div>

); }

