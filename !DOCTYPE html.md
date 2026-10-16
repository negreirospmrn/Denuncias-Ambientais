<!DOCTYPE html>

<html lang="pt-BR" class="h-full bg-slate-50">

<head>

&#x20;   <meta charset="UTF-8">

&#x20;   <meta name="viewport" content="width=device-width, initial-scale=1.0">

&#x20;   <title>Batalhão de Policiamento Ambiental — BPAmb | Sistema de Denúncias</title>

&#x20;   <!-- Tailwind CSS CDN -->

&#x20;   <script src="https://cdn.tailwindcss.com"></script>

&#x20;   <script>

&#x20;       tailwind.config = {

&#x20;           theme: {

&#x20;               extend: {

&#x20;                   colors: {

&#x20;                       ambiental: {

&#x20;                           50: '#f0fdf4',

&#x20;                           100: '#dcfce7',

&#x20;                           600: '#16a34a',

&#x20;                           700: '#15803d',

&#x20;                           800: '#166534',

&#x20;                           900: '#14532d',

&#x20;                       }

&#x20;                   }

&#x20;               }

&#x20;           }

&#x20;       }

&#x20;   </script>

&#x20;   <!-- FontAwesome Icons -->

&#x20;   <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

</head>

<body class="h-full flex flex-col font-sans text-slate-800 antialiased">



&#x20;   <!-- CABEÇALHO INSTITUCIONAL -->

&#x20;   <header class="bg-ambiental-900 text-white shadow-md sticky top-0 z-50">

&#x20;       <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">

&#x20;           <div class="flex items-center space-x-3">

&#x20;               <div class="bg-ambiental-800 p-3 rounded-full border border-ambiental-600">

&#x20;                   <i class="fa-solid fa-shield-halved text-emerald-400 text-2xl"></i>

&#x20;               </div>

&#x20;               <div>

&#x20;                   <span class="text-xs uppercase tracking-wider text-emerald-400 font-semibold block">Polícia Militar</span>

&#x20;                   <h1 class="text-lg sm:text-xl font-bold tracking-tight">Batalhão de Policiamento Ambiental — BPAmb</h1>

&#x20;               </div>

&#x20;           </div>

&#x20;           <nav class="flex items-center space-x-3">

&#x20;               <button onclick="switchView('public')" id="nav-public" class="px-4 py-2 text-sm font-medium rounded-lg bg-ambiental-800 text-white transition hover:bg-ambiental-700">

&#x20;                   <i class="fa-solid fa-bullhorn mr-2"></i> Denúncia

&#x20;               </button>

&#x20;               <button onclick="switchView('consult')" id="nav-consult" class="px-4 py-2 text-sm font-medium rounded-lg text-slate-300 hover:text-white transition hover:bg-ambiental-800">

&#x20;                   <i class="fa-solid fa-magnifying-glass mr-2"></i> Consultar Protocolo

&#x20;               </button>

&#x20;               <button onclick="switchView('admin')" id="nav-admin" class="px-4 py-2 text-sm font-medium rounded-lg text-emerald-300 border border-emerald-600/50 hover:bg-ambiental-800 transition">

&#x20;                   <i class="fa-solid fa-lock mr-2"></i> Painel Restrito

&#x20;               </button>

&#x20;           </nav>

&#x20;       </div>

&#x20;   </header>



&#x20;   <!-- CONTEÚDO PRINCIPAL -->

&#x20;   <main class="flex-grow max-w-7xl w-full mx-auto px-4 sm:px-6 lg:px-8 py-8">



&#x20;       <!-- ================= VISTA: PÁGINA PÚBLICA / FORMULÁRIO ================= -->

&#x20;       <div id="view-public" class="space-y-8">

&#x20;           <!-- Banner de Apresentação -->

&#x20;           <div class="bg-gradient-to-r from-ambiental-800 to-ambiental-900 rounded-2xl text-white p-6 sm:p-10 shadow-lg relative overflow-hidden">

&#x20;               <div class="absolute right-0 bottom-0 opacity-10 translate-x-10 translate-y-10">

&#x20;                   <i class="fa-solid fa-tree text-9xl"></i>

&#x20;               </div>

&#x20;               <div class="max-w-3xl relative z-10 space-y-4">

&#x20;                   <span class="bg-emerald-700/60 text-emerald-200 text-xs font-semibold px-3 py-1 rounded-full uppercase tracking-wider border border-emerald-500/30">Canal Oficial de Atendimento</span>

&#x20;                   <h2 class="text-3xl sm:text-4xl font-extrabold tracking-tight">Denúncia Ambiental</h2>

&#x20;                   <p class="text-slate-200 text-base sm:text-lg leading-relaxed">

&#x20;                       Ajude a proteger o meio ambiente. Registre uma denúncia e contribua para a preservação ambiental. O sigilo das informações é garantido por lei.

&#x20;                   </p>

&#x20;                   <div class="pt-2 flex flex-wrap gap-4 text-sm text-emerald-300 font-medium">

&#x20;                       <span><i class="fa-solid fa-shield-cat mr-1.5"></i> Fauna \& Flora</span>

&#x20;                       <span><i class="fa-solid fa-water mr-1.5"></i> Recursos Hídricos</span>

&#x20;                       <span><i class="fa-solid fa-smog mr-1.5"></i> Poluição \& Resíduos</span>

&#x20;                   </div>

&#x20;               </div>

&#x20;           </div>



&#x20;           <!-- Avisos de Segurança e Recomendações -->

&#x20;           <div class="grid grid-cols-1 md:grid-cols-2 gap-6">

&#x20;               <div class="bg-amber-50 border-l-4 border-amber-500 p-5 rounded-r-xl shadow-sm">

&#x20;                   <div class="flex items-start">

&#x20;                       <div class="text-amber-600 text-xl mr-3 mt-0.5"><i class="fa-solid fa-triangle-exclamation"></i></div>

&#x20;                       <div>

&#x20;                           <h3 class="font-bold text-amber-900 text-sm uppercase tracking-wider">Aviso de Segurança</h3>

&#x20;                           <p class="text-amber-800 text-sm mt-1">

&#x20;                               <strong>Não se aproxime de suspeitos</strong> nem se coloque em risco para obter provas. A sua integridade física é prioridade.

&#x20;                           </p>

&#x20;                       </div>

&#x20;                   </div>

&#x20;               </div>

&#x20;               <div class="bg-emerald-50 border-l-4 border-emerald-600 p-5 rounded-r-xl shadow-sm">

&#x20;                   <div class="flex items-start">

&#x20;                       <div class="text-emerald-700 text-xl mr-3 mt-0.5"><i class="fa-solid fa-user-secret"></i></div>

&#x20;                       <div>

&#x20;                           <h3 class="font-bold text-emerald-900 text-sm uppercase tracking-wider">Anonimato Garantido</h3>

&#x20;                           <p class="text-emerald-800 text-sm mt-1">

&#x20;                               O tratamento dos dados é responsável. Você pode optar por não se identificar. Nenhuma informação pessoal será exposta publicamente.

&#x20;                           </p>

&#x20;                       </div>

&#x20;                   </div>

&#x20;               </div>

&#x20;           </div>



&#x20;           <!-- Formulário de Denúncia -->

&#x20;           <div class="bg-white rounded-2xl shadow-md border border-slate-200 overflow-hidden">

&#x20;               <div class="bg-slate-50 px-6 py-4 border-b border-slate-200 flex items-center justify-between">

&#x20;                   <h3 class="font-bold text-slate-800 flex items-center"><i class="fa-solid fa-file-pen text-ambiental-600 mr-2"></i> Preencha os Dados da Ocorrência</h3>

&#x20;                   <span class="text-xs text-slate-500">\* Campos com preenchimento obrigatório</span>

&#x20;               </div>



&#x20;               <form id="denunciaForm" onsubmit="handleFormSubmit(event)" class="p-6 sm:p-8 space-y-8">

&#x20;                   

&#x20;                   <!-- SEÇÃO A: Tipo de Ocorrência -->

&#x20;                   <div class="space-y-4">

&#x20;                       <h4 class="text-sm font-bold uppercase tracking-wider text-ambiental-800 border-b pb-2 flex items-center">

&#x20;                           <span class="bg-ambiental-100 text-ambiental-800 w-6 h-6 rounded-full inline-flex items-center justify-center text-xs mr-2">A</span>

&#x20;                           Tipo de Ocorrência

&#x20;                       </h4>

&#x20;                       

&#x20;                       <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">

&#x20;                           <div>

&#x20;                               <label class="block text-sm font-medium text-slate-700 mb-1">Tipo de Infração Ambiental \*</label>

&#x20;                               <select id="tipoInfracao" required class="w-full rounded-lg border border-slate-300 px-3 py-2 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none bg-white">

&#x20;                                   <option value="">Selecione o tipo de infração...</option>

&#x20;                                   <option value="Desmatamento">Desmatamento</option>

&#x20;                                   <option value="Queimadas">Queimadas</option>

&#x20;                                   <option value="Poluição Sonora">Poluição Sonora</option>

&#x20;                                   <option value="Poluição da Água">Poluição da Água</option>

&#x20;                                   <option value="Descarte irregular de resíduos">Descarte irregular de resíduos</option>

&#x20;                                   <option value="Maus-tratos a animais">Maus-tratos a animais</option>

&#x20;                                   <option value="Caça ou pesca ilegal">Caça ou pesca ilegal</option>

&#x20;                                   <option value="Tráfico de animais silvestres">Tráfico de animais silvestres</option>

&#x20;                                   <option value="Extração ilegal de recursos naturais">Extração ilegal de recursos naturais</option>

&#x20;                                   <option value="Outra ocorrência">Outra ocorrência</option>

&#x20;                               </select>

&#x20;                           </div>



&#x20;                           <div>

&#x20;                               <label class="block text-sm font-medium text-slate-700 mb-1">Quando Ocorre? \*</label>

&#x20;                               <select id="quandoOcorre" required class="w-full rounded-lg border border-slate-300 px-3 py-2 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none bg-white">

&#x20;                                   <option value="">Selecione a frequência/período...</option>

&#x20;                                   <option value="Neste momento (em andamento)">Neste momento (em andamento)</option>

&#x20;                                   <option value="Hoje">Hoje</option>

&#x20;                                   <option value="Em outra data">Em outra data</option>

&#x20;                                   <option value="De forma recorrente">De forma recorrente</option>

&#x20;                               </select>

&#x20;                           </div>

&#x20;                       </div>



&#x20;                       <div>

&#x20;                           <label class="block text-sm font-medium text-slate-700 mb-1">Descrição dos Fatos \*</label>

&#x20;                           <p class="text-xs text-slate-500 mb-2">Descreva com clareza o que aconteceu, características de veículos, suspeitos ou animais envolvidos.</p>

&#x20;                           <textarea id="descricaoFatos" rows="4" required placeholder="Ex: Há um caminhão descarregando entulhos e resíduos industriais próximo à margem do rio..." class="w-full rounded-lg border border-slate-300 p-3 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none"></textarea>

&#x20;                       </div>

&#x20;                   </div>



&#x20;                   <!-- SEÇÃO B: Local da Ocorrência -->

&#x20;                   <div class="space-y-4">

&#x20;                       <h4 class="text-sm font-bold uppercase tracking-wider text-ambiental-800 border-b pb-2 flex items-center">

&#x20;                           <span class="bg-ambiental-100 text-ambiental-800 w-6 h-6 rounded-full inline-flex items-center justify-center text-xs mr-2">B</span>

&#x20;                           Local da Ocorrência

&#x20;                       </h4>



&#x20;                       <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">

&#x20;                           <div>

&#x20;                               <label class="block text-sm font-medium text-slate-700 mb-1">Município \*</label>

&#x20;                               <input type="text" id="municipio" required placeholder="Ex: Natal" class="w-full rounded-lg border border-slate-300 px-3 py-2 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none">

&#x20;                           </div>

&#x20;                           <div>

&#x20;                               <label class="block text-sm font-medium text-slate-700 mb-1">Coordenadas Geográficas / Link do Mapa (Opcional)</label>

&#x20;                               <input type="text" id="coordenadas" placeholder="Ex: -5.7945, -35.2110 ou link do Google Maps" class="w-full rounded-lg border border-slate-300 px-3 py-2 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none">

&#x20;                           </div>

&#x20;                       </div>



&#x20;                       <div>

&#x20;                           <label class="block text-sm font-medium text-slate-700 mb-1">Endereço, Bairro, Povoado ou Ponto de Referência \*</label>

&#x20;                           <input type="text" id="endereco" required placeholder="Ex: Próximo à ponte velha, Estrada da Costa, Bairro Pitimbu" class="w-full rounded-lg border border-slate-300 px-3 py-2 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none">

&#x20;                       </div>

&#x20;                   </div>



&#x20;                   <!-- SEÇÃO C: Evidências -->

&#x20;                   <div class="space-y-4">

&#x20;                       <h4 class="text-sm font-bold uppercase tracking-wider text-ambiental-800 border-b pb-2 flex items-center">

&#x20;                           <span class="bg-ambiental-100 text-ambiental-800 w-6 h-6 rounded-full inline-flex items-center justify-center text-xs mr-2">C</span>

&#x20;                           Evidências (Opcional)

&#x20;                       </h4>

&#x20;                       <div class="bg-slate-50 border border-dashed border-slate-300 rounded-xl p-6 text-center">

&#x20;                           <i class="fa-solid fa-cloud-arrow-up text-3xl text-slate-400 mb-2"></i>

&#x20;                           <p class="text-sm font-medium text-slate-700">Anexar fotos, vídeos ou documentos</p>

&#x20;                           <p class="text-xs text-slate-500 mt-1">Formatos permitidos: JPG, PNG, MP4, PDF (Máx. 25MB no total).</p>

&#x20;                           <input type="file" id="evidencias" multiple accept="image/\*,video/\*,.pdf" class="mt-4 text-xs text-slate-500 file:mr-4 file:py-2 file:px-4 file:rounded-full file:border-0 file:text-xs file:font-semibold file:bg-ambiental-50 file:text-ambiental-700 hover:file:bg-ambiental-100 cursor-pointer">

&#x20;                       </div>

&#x20;                   </div>



&#x20;                   <!-- SEÇÃO D: Identificação do Denunciante -->

&#x20;                   <div class="space-y-4">

&#x20;                       <h4 class="text-sm font-bold uppercase tracking-wider text-ambiental-800 border-b pb-2 flex items-center">

&#x20;                           <span class="bg-ambiental-100 text-ambiental-800 w-6 h-6 rounded-full inline-flex items-center justify-center text-xs mr-2">D</span>

&#x20;                           Identificação do Denunciante

&#x20;                       </h4>



&#x20;                       <div class="bg-emerald-50 border border-emerald-200 p-4 rounded-xl flex items-center justify-between">

&#x20;                           <div class="flex items-center space-x-3">

&#x20;                               <input type="checkbox" id="anonimoCheck" onchange="toggleAnonimo()" class="w-5 h-5 text-ambiental-600 rounded border-slate-300 focus:ring-ambiental-500">

&#x20;                               <label for="anonimoCheck" class="font-bold text-emerald-900 text-sm cursor-pointer">

&#x20;                                   <i class="fa-solid fa-user-secret mr-1"></i> Desejo fazer uma denúncia anônima

&#x20;                               </label>

&#x20;                           </div>

&#x20;                           <span class="text-xs bg-emerald-200 text-emerald-800 font-semibold px-2.5 py-1 rounded-full">Recomendado se houver risco</span>

&#x20;                       </div>



&#x20;                       <div id="identificacaoContainer" class="grid grid-cols-1 sm:grid-cols-3 gap-4 pt-2">

&#x20;                           <div>

&#x20;                               <label class="block text-sm font-medium text-slate-700 mb-1">Nome (Opcional)</label>

&#x20;                               <input type="text" id="denuncianteNome" placeholder="Seu nome completo" class="w-full rounded-lg border border-slate-300 px-3 py-2 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none">

&#x20;                           </div>

&#x20;                           <div>

&#x20;                               <label class="block text-sm font-medium text-slate-700 mb-1">Telefone / WhatsApp (Opcional)</label>

&#x20;                               <input type="text" id="denuncianteFone" placeholder="(00) 00000-0000" class="w-full rounded-lg border border-slate-300 px-3 py-2 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none">

&#x20;                           </div>

&#x20;                           <div>

&#x20;                               <label class="block text-sm font-medium text-slate-700 mb-1">E-mail (Opcional)</label>

&#x20;                               <input type="email" id="denuncianteEmail" placeholder="seu@email.com" class="w-full rounded-lg border border-slate-300 px-3 py-2 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none">

&#x20;                           </div>

&#x20;                       </div>

&#x20;                   </div>



&#x20;                   <!-- Botão de Envio -->

&#x20;                   <div class="pt-6 border-t border-slate-200 flex flex-col sm:flex-row items-center justify-between gap-4">

&#x20;                       <p class="text-xs text-slate-500">

&#x20;                           Ao enviar, você concorda que os dados fornecidos serão tratados com segurança para fins de fiscalização ambiental.

&#x20;                       </p>

&#x20;                       <button type="submit" class="w-full sm:w-auto px-8 py-3 bg-ambiental-600 hover:bg-ambiental-700 text-white font-bold rounded-xl shadow-md transition flex items-center justify-center space-x-2">

&#x20;                           <i class="fa-solid fa-paper-plane"></i>

&#x20;                           <span>Enviar Denúncia</span>

&#x20;                       </button>

&#x20;                   </div>



&#x20;               </form>

&#x20;           </div>

&#x20;       </div>



&#x20;       <!-- ================= VISTA: TELA DE CONFIRMAÇÃO DO PROTOCOLO ================= -->

&#x20;       <div id="view-confirmation" class="hidden max-w-2xl mx-auto space-y-6">

&#x20;           <div class="bg-white rounded-2xl shadow-md border border-slate-200 p-8 text-center space-y-6">

&#x20;               <div class="w-16 h-16 bg-emerald-100 text-emerald-600 rounded-full flex items-center justify-center text-3xl mx-auto shadow-inner">

&#x20;                   <i class="fa-solid fa-circle-check"></i>

&#x20;               </div>

&#x20;               <div class="space-y-2">

&#x20;                   <h2 class="text-2xl font-bold text-slate-900">Denúncia Registrada com Sucesso!</h2>

&#x20;                   <p class="text-sm text-slate-600">Sua colaboração é fundamental para a preservação ambiental do Estado.</p>

&#x20;               </div>



&#x20;               <div class="bg-slate-50 border border-slate-200 rounded-xl p-6 space-y-3">

&#x20;                   <span class="text-xs uppercase tracking-wider text-slate-500 font-semibold block">Número de Protocolo Único</span>

&#x20;                   <div id="protocoloGerado" class="text-2xl sm:text-3xl font-mono font-bold text-ambiental-800 tracking-wider">BPA-2026-98421</div>

&#x20;                   <div class="text-xs text-slate-500" id="dataRegistroGerado">Data do registro: 16/10/2026 às 12:00</div>

&#x20;               </div>



&#x20;               <div class="bg-amber-50 border border-amber-200 rounded-xl p-4 text-left text-xs text-amber-800 space-y-1">

&#x20;                   <p class="font-bold"><i class="fa-solid fa-triangle-exclamation mr-1"></i> Aviso Importante:</p>

&#x20;                   <p>Este sistema não promete atendimento imediato nem afirma que a denúncia já foi investigada. O protocolo serve para acompanhamento interno e checagem de status.</p>

&#x20;               </div>



&#x20;               <div class="flex flex-wrap gap-3 justify-center pt-2">

&#x20;                   <button onclick="copiarProtocolo()" class="px-4 py-2 bg-slate-100 hover:bg-slate-200 text-slate-700 text-sm font-medium rounded-lg transition">

&#x20;                       <i class="fa-solid fa-copy mr-1.5"></i> Copiar Protocolo

&#x20;                   </button>

&#x20;                   <button onclick="window.print()" class="px-4 py-2 bg-slate-100 hover:bg-slate-200 text-slate-700 text-sm font-medium rounded-lg transition">

&#x20;                       <i class="fa-solid fa-print mr-1.5"></i> Imprimir Comprovante

&#x20;                   </button>

&#x20;                   <button onclick="switchView('public')" class="px-6 py-2 bg-ambiental-600 hover:bg-ambiental-700 text-white text-sm font-medium rounded-lg transition">

&#x20;                       Nova Denúncia

&#x20;                   </button>

&#x20;               </div>

&#x20;           </div>

&#x20;       </div>



&#x20;       <!-- ================= VISTA: CONSULTAR PROTOCOLO ================= -->

&#x20;       <div id="view-consult" class="hidden max-w-xl mx-auto space-y-6">

&#x20;           <div class="bg-white rounded-2xl shadow-md border border-slate-200 p-8 space-y-6">

&#x20;               <div class="text-center space-y-2">

&#x20;                   <div class="w-14 h-14 bg-ambiental-100 text-ambiental-800 rounded-full flex items-center justify-center text-2xl mx-auto">

&#x20;                       <i class="fa-solid fa-magnifying-glass"></i>

&#x20;                   </div>

&#x20;                   <h2 class="text-2xl font-bold text-slate-900">Consultar Situação</h2>

&#x20;                   <p class="text-sm text-slate-600">Digite o número de protocolo fornecido no momento do registro.</p>

&#x20;               </div>



&#x20;               <div class="flex gap-2">

&#x20;                   <input type="text" id="inputConsulta" placeholder="Ex: BPA-2026-XXXXX" class="flex-grow rounded-lg border border-slate-300 px-4 py-2.5 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none uppercase font-mono">

&#x20;                   <button onclick="realizarConsulta()" class="px-5 py-2.5 bg-ambiental-600 hover:bg-ambiental-700 text-white font-medium rounded-lg transition text-sm">

&#x20;                       Pesquisar

&#x20;                   </button>

&#x20;               </div>



&#x20;               <div id="resultadoConsulta" class="hidden pt-4 border-t border-slate-200 space-y-4">

&#x20;                   <!-- Preenchido via JS -->

&#x20;               </div>

&#x20;           </div>

&#x20;       </div>



&#x20;       <!-- ================= VISTA: PAINEL ADMINISTRATIVO RESTRITO ================= -->

&#x20;       <div id="view-admin" class="hidden space-y-6">

&#x20;           

&#x20;           <!-- Login State -->

&#x20;           <div id="admin-login-box" class="max-w-md mx-auto bg-white rounded-2xl shadow-md border border-slate-200 p-8 space-y-6">

&#x20;               <div class="text-center space-y-2">

&#x20;                   <div class="w-14 h-14 bg-slate-900 text-emerald-400 rounded-full flex items-center justify-center text-2xl mx-auto">

&#x20;                       <i class="fa-solid fa-lock"></i>

&#x20;                   </div>

&#x20;                   <h2 class="text-2xl font-bold text-slate-900">Área Restrita - BPAmb</h2>

&#x20;                   <p class="text-sm text-slate-600">Acesso exclusivo para policiais e analistas autorizados.</p>

&#x20;               </div>



&#x20;               <form onsubmit="handleAdminLogin(event)" class="space-y-4">

&#x20;                   <div>

&#x20;                       <label class="block text-sm font-medium text-slate-700 mb-1">Identificação / Matrícula</label>

&#x20;                       <input type="text" id="adminUser" required placeholder="Ex: PM-123456" class="w-full rounded-lg border border-slate-300 px-3 py-2 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none">

&#x20;                   </div>

&#x20;                   <div>

&#x20;                       <label class="block text-sm font-medium text-slate-700 mb-1">Senha de Acesso</label>

&#x20;                       <input type="password" id="adminPass" required placeholder="••••••••" class="w-full rounded-lg border border-slate-300 px-3 py-2 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none">

&#x20;                   </div>

&#x20;                   <button type="submit" class="w-full py-3 bg-slate-900 hover:bg-slate-800 text-white font-bold rounded-xl shadow-md transition text-sm">

&#x20;                       Entrar no Sistema

&#x20;                   </button>

&#x20;                   <p class="text-xs text-center text-slate-400">Ambiente seguro com registro de acessos (Audit Log).</p>

&#x20;               </form>

&#x20;           </div>



&#x20;           <!-- Dashboard State -->

&#x20;           <div id="admin-dashboard" class="hidden space-y-6">

&#x20;               <div class="flex flex-col sm:flex-row items-start sm:items-center justify-between bg-white p-6 rounded-2xl shadow-sm border border-slate-200 gap-4">

&#x20;                   <div>

&#x20;                       <h2 class="text-xl font-bold text-slate-900">Painel de Gestão de Denúncias</h2>

&#x20;                       <p class="text-xs text-slate-500 mt-1">Usuário autenticado: <span class="font-semibold text-ambiental-700">Sgt. PM Oliveira (Mat: 4819-2)</span> | Nível: Administrador</p>

&#x20;                   </div>

&#x20;                   <button onclick="logoutAdmin()" class="px-4 py-2 bg-red-50 hover:bg-red-100 text-red-700 rounded-lg text-xs font-semibold transition border border-red-200">

&#x20;                       <i class="fa-solid fa-right-from-bracket mr-1"></i> Sair do Painel

&#x20;                   </button>

&#x20;               </div>



&#x20;               <!-- Filtros e Pesquisa -->

&#x20;               <div class="bg-white p-4 rounded-xl shadow-sm border border-slate-200 grid grid-cols-1 sm:grid-cols-4 gap-3">

&#x20;                   <input type="text" id="filtroProtocolo" placeholder="Buscar por protocolo..." oninput="renderizarTabelaAdmin()" class="rounded-lg border border-slate-300 px-3 py-2 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none">

&#x20;                   <input type="text" id="filtroMunicipio" placeholder="Filtrar por município..." oninput="renderizarTabelaAdmin()" class="rounded-lg border border-slate-300 px-3 py-2 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none">

&#x20;                   <select id="filtroStatus" onchange="renderizarTabelaAdmin()" class="rounded-lg border border-slate-300 px-3 py-2 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none bg-white">

&#x20;                       <option value="">Todos os Status</option>

&#x20;                       <option value="Recebida">Recebida</option>

&#x20;                       <option value="Em análise">Em análise</option>

&#x20;                       <option value="Encaminhada">Encaminhada</option>

&#x20;                       <option value="Em atendimento">Em atendimento</option>

&#x20;                       <option value="Concluída">Concluída</option>

&#x20;                   </select>

&#x20;                   <button onclick="limparFiltrosAdmin()" class="px-4 py-2 bg-slate-100 hover:bg-slate-200 text-slate-700 rounded-lg text-sm font-medium transition">

&#x20;                       Limpar Filtros

&#x20;                   </button>

&#x20;               </div>



&#x20;               <!-- Listagem de Denúncias -->

&#x20;               <div class="bg-white rounded-2xl shadow-md border border-slate-200 overflow-hidden">

&#x20;                   <div class="overflow-x-auto">

&#x20;                       <table class="w-full text-left border-collapse text-sm">

&#x20;                           <thead class="bg-slate-50 text-slate-600 uppercase text-xs tracking-wider border-b border-slate-200">

&#x20;                               <tr>

&#x20;                                   <th class="p-4">Protocolo / Data</th>

&#x20;                                   <th class="p-4">Infração / Município</th>

&#x20;                                   <th class="p-4">Status</th>

&#x20;                                   <th class="p-4">Denunciante</th>

&#x20;                                   <th class="p-4 text-right">Ações</th>

&#x20;                               </tr>

&#x20;                           </thead>

&#x20;                           <tbody id="adminTableBody" class="divide-y divide-slate-200">

&#x20;                               <!-- Preenchido via JS -->

&#x20;                           </tbody>

&#x20;                       </table>

&#x20;                   </div>

&#x20;               </div>

&#x20;           </div>



&#x20;       </div>



&#x20;   </main>



&#x20;   <!-- MODAL DE DETALHES DA DENÚNCIA (ADMIN) -->

&#x20;   <div id="modalDetalhes" class="hidden fixed inset-0 bg-slate-900/50 z-50 flex items-center justify-center p-4 overflow-y-auto">

&#x20;       <div class="bg-white rounded-2xl max-w-2xl w-full p-6 shadow-xl space-y-6 my-8">

&#x20;           <div class="flex items-center justify-between border-b pb-4">

&#x20;               <h3 class="font-bold text-lg text-slate-900" id="modalProtocoloTitulo">Detalhes da Ocorrência</h3>

&#x20;               <button onclick="fecharModal()" class="text-slate-400 hover:text-slate-600 text-xl"><i class="fa-solid fa-xmark"></i></button>

&#x20;           </div>

&#x20;           

&#x20;           <div class="space-y-4 text-sm text-slate-700 max-h-\[60vh] overflow-y-auto pr-2">

&#x20;               <div class="grid grid-cols-2 gap-4 bg-slate-50 p-4 rounded-xl">

&#x20;                   <div><strong>Tipo:</strong> <span id="modalTipo">-</span></div>

&#x20;                   <div><strong>Data/Hora:</strong> <span id="modalData">-</span></div>

&#x20;                   <div><strong>Município:</strong> <span id="modalMunicipio">-</span></div>

&#x20;                   <div><strong>Endereço:</strong> <span id="modalEndereco">-</span></div>

&#x20;               </div>



&#x20;               <div>

&#x20;                   <strong class="block text-slate-900 mb-1">Descrição dos Fatos:</strong>

&#x20;                   <p id="modalDescricao" class="bg-slate-50 p-3 rounded-lg text-slate-600 whitespace-pre-wrap">-</p>

&#x20;               </div>



&#x20;               <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">

&#x20;                   <div>

&#x20;                       <label class="block font-medium text-slate-900 mb-1">Alterar Status</label>

&#x20;                       <select id="modalStatusSelect" class="w-full rounded-lg border border-slate-300 p-2 text-sm bg-white">

&#x20;                           <option value="Recebida">Recebida</option>

&#x20;                           <option value="Em análise">Em análise</option>

&#x20;                           <option value="Encaminhada">Encaminhada</option>

&#x20;                           <option value="Em atendimento">Em atendimento</option>

&#x20;                           <option value="Concluída">Concluída</option>

&#x20;                       </select>

&#x20;                   </div>

&#x20;                   <div>

&#x20;                       <strong class="block font-medium text-slate-900 mb-1">Evidências Anexadas</strong>

&#x20;                       <span id="modalEvidencias" class="text-slate-600">Nenhum arquivo enviado</span>

&#x20;                   </div>

&#x20;               </div>



&#x20;               <div>

&#x20;                   <label class="block font-medium text-slate-900 mb-1">Observações Internas (Restritas à Polícia)</label>

&#x20;                   <textarea id="modalObsInternas" rows="3" placeholder="Insira anotações de diligências ou encaminhamentos..." class="w-full rounded-lg border border-slate-300 p-3 text-sm focus:ring-2 focus:ring-ambiental-600 focus:outline-none"></textarea>

&#x20;               </div>

&#x20;           </div>



&#x20;           <div class="flex justify-end space-x-3 pt-4 border-t">

&#x20;               <button onclick="fecharModal()" class="px-4 py-2 bg-slate-100 hover:bg-slate-200 text-slate-700 font-medium rounded-lg text-sm">Cancelar</button>

&#x20;               <button onclick="salvarAlteracoesAdmin()" class="px-6 py-2 bg-ambiental-600 hover:bg-ambiental-700 text-white font-bold rounded-lg text-sm">Salvar Alterações</button>

&#x20;           </div>

&#x20;       </div>

&#x20;   </div>



&#x20;   <!-- RODAPÉ -->

&#x20;   <footer class="bg-slate-900 text-slate-400 py-8 border-t border-slate-800 mt-12">

&#x20;       <div class="max-w-7xl mx-auto px-4 text-center space-y-4 text-xs">

&#x20;           <p class="font-medium text-slate-300">Batalhão de Policiamento Ambiental — BPAmb | Polícia Militar do Estado</p>

&#x20;           <p>Sistema seguro desenvolvido para recebimento de denúncias ambientais. Proteção de dados em conformidade com a legislação vigente.</p>

&#x20;           <p class="text-slate-500">© 2026 BPAmb. Todos os direitos reservados.</p>

&#x20;       </div>

&#x20;   </footer>



&#x20;   <!-- SCRIPT DE FUNCIONAMENTO -->

&#x20;   <script>

&#x20;       // Banco de dados simulado em memória (localStorage) com dados fictícios iniciais para demonstração

&#x20;       let denuncias = JSON.parse(localStorage.getItem('bpamb\_denuncias')) || \[

&#x20;           {

&#x20;               id: 'BPA-2026-84920',

&#x20;               data: '15/10/2026 14:30',

&#x20;               tipoInfracao: 'Desmatamento',

&#x20;               quandoOcorre: 'Em outra data',

&#x20;               descricao: 'Supressão de vegetação nativa com uso de trator em área de preservação permanente.',

&#x20;               municipio: 'Extremoz',

&#x20;               endereco: 'Próximo à lagoa central, Estrada de Pitangui',

&#x20;               coordenadas: '-5.7012, -35.2841',

&#x20;               evidencias: 'foto\_vegetacao.jpg',

&#x20;               anonimo: true,

&#x20;               denunciante: { nome: '', fone: '', email: '' },

&#x20;               status: 'Em análise',

&#x20;               obsInternas: 'Viatura enviada para checagem preliminar de coordenadas.',

&#x20;               historico: \[{ data: '15/10/2026 15:00', usuario: 'Sgt. Silva', acao: 'Status alterado para Em análise' }]

&#x20;           },

&#x20;           {

&#x20;               id: 'BPA-2026-39210',

&#x20;               data: '16/10/2026 09:15',

&#x20;               tipoInfracao: 'Poluição Sonora',

&#x20;               quandoOcorre: 'Neste momento (em andamento)',

&#x20;               descricao: 'Som automotivo em volume extremamente alto em área residencial próxima a parque ecológico.',

&#x20;               municipio: 'Natal',

&#x20;               endereco: 'Av. Engenheiro Roberto Freire, Ponta Negra',

&#x20;               coordenadas: '',

&#x20;               evidencias: '',

&#x20;               anonimo: false,

&#x20;               denunciante: { nome: 'Carlos Eduardo', fone: '(84) 99888-7766', email: 'carlos@email.com' },

&#x20;               status: 'Recebida',

&#x20;               obsInternas: '',

&#x20;               historico: \[{ data: '16/10/2026 09:15', usuario: 'Sistema', acao: 'Registro gerado' }]

&#x20;           }

&#x20;       ];



&#x20;       let currentModalIndex = null;

&#x20;       let isAdminLoggedIn = false;



&#x20;       function salvarStorage() {

&#x20;           localStorage.setItem('bpamb\_denuncias', JSON.stringify(denuncias));

&#x20;       }



&#x20;       // Navegação entre abas

&#x20;       function switchView(view) {

&#x20;           document.getElementById('view-public').classList.add('hidden');

&#x20;           document.getElementById('view-confirmation').classList.add('hidden');

&#x20;           document.getElementById('view-consult').classList.add('hidden');

&#x20;           document.getElementById('view-admin').classList.add('hidden');



&#x20;           // Reset nav colors

&#x20;           document.getElementById('nav-public').className = "px-4 py-2 text-sm font-medium rounded-lg text-slate-300 hover:text-white transition hover:bg-ambiental-800";

&#x20;           document.getElementById('nav-consult').className = "px-4 py-2 text-sm font-medium rounded-lg text-slate-300 hover:text-white transition hover:bg-ambiental-800";

&#x20;           document.getElementById('nav-admin').className = "px-4 py-2 text-sm font-medium rounded-lg text-emerald-300 border border-emerald-600/50 hover:bg-ambiental-800 transition";



&#x20;           if (view === 'public') {

&#x20;               document.getElementById('view-public').classList.remove('hidden');

&#x20;               document.getElementById('nav-public').className = "px-4 py-2 text-sm font-medium rounded-lg bg-ambiental-800 text-white transition";

&#x20;           } else if (view === 'consult') {

&#x20;               document.getElementById('view-consult').classList.remove('hidden');

&#x20;               document.getElementById('nav-consult').className = "px-4 py-2 text-sm font-medium rounded-lg bg-ambiental-800 text-white transition";

&#x20;           } else if (view === 'admin') {

&#x20;               document.getElementById('view-admin').classList.remove('hidden');

&#x20;               document.getElementById('nav-admin').className = "px-4 py-2 text-sm font-medium rounded-lg bg-emerald-700 text-white transition";

&#x20;               checkAdminState();

&#x20;           }

&#x20;           window.scrollTo({ top: 0, behavior: 'smooth' });

&#x20;       }



&#x20;       // Alternar campos de identificação ao marcar anonimato

&#x20;       function toggleAnonimo() {

&#x20;           const isAnon = document.getElementById('anonimoCheck').checked;

&#x20;           const container = document.getElementById('identificacaoContainer');

&#x20;           if (isAnon) {

&#x20;               container.style.opacity = '0.4';

&#x20;               document.getElementById('denuncianteNome').value = '';

&#x20;               document.getElementById('denuncianteFone').value = '';

&#x20;               document.getElementById('denuncianteEmail').value = '';

&#x20;               document.getElementById('denuncianteNome').disabled = true;

&#x20;               document.getElementById('denuncianteFone').disabled = true;

&#x20;               document.getElementById('denuncianteEmail').disabled = true;

&#x20;           } else {

&#x20;               container.style.opacity = '1';

&#x20;               document.getElementById('denuncianteNome').disabled = false;

&#x20;               document.getElementById('denuncianteFone').disabled = false;

&#x20;               document.getElementById('denuncianteEmail').disabled = false;

&#x20;           }

&#x20;       }



&#x20;       // Envio do Formulário Público

&#x20;       function handleFormSubmit(e) {

&#x20;           e.preventDefault();



&#x20;           const randomNum = Math.floor(10000 + Math.random() \* 90000);

&#x20;           const protocoloID = `BPA-2026-${randomNum}`;

&#x20;           const agora = new Date().toLocaleString('pt-BR');



&#x20;           const novaDenuncia = {

&#x20;               id: protocoloID,

&#x20;               data: agora,

&#x20;               tipoInfracao: document.getElementById('tipoInfracao').value,

&#x20;               quandoOcorre: document.getElementById('quandoOcorre').value,

&#x20;               descricao: document.getElementById('descricaoFatos').value,

&#x20;               municipio: document.getElementById('municipio').value,

&#x20;               endereco: document.getElementById('endereco').value,

&#x20;               coordenadas: document.getElementById('coordenadas').value,

&#x20;               evidencias: document.getElementById('evidencias').files.length > 0 ? document.getElementById('evidencias').files\[0].name : '',

&#x20;               anonimo: document.getElementById('anonimoCheck').checked,

&#x20;               denunciante: {

&#x20;                   nome: document.getElementById('denuncianteNome').value,

&#x20;                   fone: document.getElementById('denuncianteFone').value,

&#x20;                   email: document.getElementById('denuncianteEmail').value

&#x20;               },

&#x20;               status: 'Recebida',

&#x20;               obsInternas: '',

&#x20;               historico: \[{ data: agora, usuario: 'Sistema', acao: 'Denúncia registrada com sucesso' }]

&#x20;           };



&#x20;           denuncias.unshift(novaDenuncia);

&#x20;           salvarStorage();



&#x20;           // Exibir tela de confirmação

&#x20;           document.getElementById('protocoloGerado').innerText = protocoloID;

&#x20;           document.getElementById('dataRegistroGerado').innerText = `Data do registro: ${agora}`;

&#x20;           

&#x20;           document.getElementById('view-public').classList.add('hidden');

&#x20;           document.getElementById('view-confirmation').classList.remove('hidden');

&#x20;           document.getElementById('denunciaForm').reset();

&#x20;           window.scrollTo({ top: 0, behavior: 'smooth' });

&#x20;       }



&#x20;       function copiarProtocolo() {

&#x20;           const proto = document.getElementById('protocoloGerado').innerText;

&#x20;           navigator.clipboard.writeText(proto);

&#x20;           alert('Número de protocolo copiado para a área de transferência!');

&#x20;       }



&#x20;       // Consulta de Protocolo pelo Cidadão

&#x20;       function realizarConsulta() {

&#x20;           const termo = document.getElementById('inputConsulta').value.trim().toUpperCase();

&#x20;           const resultadoDiv = document.getElementById('resultadoConsulta');

&#x20;           

&#x20;           if (!termo) {

&#x20;               alert('Digite um número de protocolo válido.');

&#x20;               return;

&#x20;           }



&#x20;           const encontrada = denuncias.find(d => d.id.toUpperCase() === termo);

&#x20;           resultadoDiv.classList.remove('hidden');



&#x20;           if (encontrada) {

&#x20;               let badgeColor = 'bg-blue-100 text-blue-800';

&#x20;               if (encontrada.status === 'Em análise') badgeColor = 'bg-amber-100 text-amber-800';

&#x20;               if (encontrada.status === 'Em atendimento') badgeColor = 'bg-purple-100 text-purple-800';

&#x20;               if (encontrada.status === 'Concluída') badgeColor = 'bg-emerald-100 text-emerald-800';



&#x20;               resultadoDiv.innerHTML = `

&#x20;                   <div class="bg-slate-50 border border-slate-200 rounded-xl p-5 space-y-3">

&#x20;                       <div class="flex items-center justify-between">

&#x20;                           <span class="font-mono font-bold text-ambiental-800 text-lg">${encontrada.id}</span>

&#x20;                           <span class="px-3 py-1 rounded-full text-xs font-semibold ${badgeColor}">${encontrada.status}</span>

&#x20;                       </div>

&#x20;                       <div class="text-xs text-slate-600 space-y-1">

&#x20;                           <p><strong>Tipo:</strong> ${encontrada.tipoInfracao}</p>

&#x20;                           <p><strong>Município:</strong> ${encontrada.municipio} - ${encontrada.endereco}</p>

&#x20;                           <p><strong>Data do Registro:</strong> ${encontrada.data}</p>

&#x20;                       </div>

&#x20;                   </div>

&#x20;               `;

&#x20;           } else {

&#x20;               resultadoDiv.innerHTML = `

&#x20;                   <div class="bg-red-50 border border-red-200 rounded-xl p-4 text-center text-red-700 text-xs">

&#x20;                       Nenhuma denúncia encontrada com o protocolo <strong>${termo}</strong>. Verifique o número digitado.

&#x20;                   </div>

&#x20;               `;

&#x20;           }

&#x20;       }



&#x20;       // Lógica do Painel Administrativo

&#x20;       function handleAdminLogin(e) {

&#x20;           e.preventDefault();

&#x20;           const user = document.getElementById('adminUser').value;

&#x20;           const pass = document.getElementById('adminPass').value;



&#x20;           // Demonstração de credencial segura

&#x20;           if (user \&\& pass.length >= 4) {

&#x20;               isAdminLoggedIn = true;

&#x20;               checkAdminState();

&#x20;           } else {

&#x20;               alert('Credenciais inválidas.');

&#x20;           }

&#x20;       }



&#x20;       function checkAdminState() {

&#x20;           if (isAdminLoggedIn) {

&#x20;               document.getElementById('admin-login-box').classList.add('hidden');

&#x20;               document.getElementById('admin-dashboard').classList.remove('hidden');

&#x20;               renderizarTabelaAdmin();

&#x20;           } else {

&#x20;               document.getElementById('admin-login-box').classList.remove('hidden');

&#x20;               document.getElementById('admin-dashboard').classList.add('hidden');

&#x20;           }

&#x20;       }



&#x20;       function logoutAdmin() {

&#x20;           isAdminLoggedIn = false;

&#x20;           checkAdminState();

&#x20;       }



&#x20;       function renderizarTabelaAdmin() {

&#x20;           const tbody = document.getElementById('adminTableBody');

&#x20;           const filtroProto = document.getElementById('filtroProtocolo').value.toLowerCase();

&#x20;           const filtroMuni = document.getElementById('filtroMunicipio').value.toLowerCase();

&#x20;           const filtroStat = document.getElementById('filtroStatus').value;



&#x20;           tbody.innerHTML = '';



&#x20;           const filtradas = denuncias.filter(d => {

&#x20;               const matchProto = d.id.toLowerCase().includes(filtroProto);

&#x20;               const matchMuni = d.municipio.toLowerCase().includes(filtroMuni);

&#x20;               const matchStat = filtroStat === '' || d.status === filtroStat;

&#x20;               return matchProto \&\& matchMuni \&\& matchStat;

&#x20;           });



&#x20;           if (filtradas.length === 0) {

&#x20;               tbody.innerHTML = `<tr><td colspan="5" class="p-6 text-center text-slate-400">Nenhuma denúncia encontrada com os filtros aplicados.</td></tr>`;

&#x20;               return;

&#x20;           }



&#x20;           filtradas.forEach((d, index) => {

&#x20;               const originalIndex = denuncias.findIndex(item => item.id === d.id);

&#x20;               let badgeColor = 'bg-blue-100 text-blue-800';

&#x20;               if (d.status === 'Em análise') badgeColor = 'bg-amber-100 text-amber-800';

&#x20;               if (d.status === 'Encaminhada') badgeColor = 'bg-indigo-100 text-indigo-800';

&#x20;               if (d.status === 'Em atendimento') badgeColor = 'bg-purple-100 text-purple-800';

&#x20;               if (d.status === 'Concluída') badgeColor = 'bg-emerald-100 text-emerald-800';



&#x20;               tbody.innerHTML += `

&#x20;                   <tr class="hover:bg-slate-50 transition border-b border-slate-100">

&#x20;                       <td class="p-4">

&#x20;                           <span class="font-mono font-bold text-slate-900 block">${d.id}</span>

&#x20;                           <span class="text-xs text-slate-400">${d.data}</span>

&#x20;                       </td>

&#x20;                       <td class="p-4">

&#x20;                           <span class="font-medium text-slate-800 block">${d.tipoInfracao}</span>

&#x20;                           <span class="text-xs text-slate-500">${d.municipio}</span>

&#x20;                       </td>

&#x20;                       <td class="p-4">

&#x20;                           <span class="px-2.5 py-1 rounded-full text-xs font-semibold ${badgeColor}">${d.status}</span>

&#x20;                       </td>

&#x20;                       <td class="p-4 text-xs text-slate-600">

&#x20;                           ${d.anonimo ? '<span class="text-emerald-700 font-semibold"><i class="fa-solid fa-user-secret mr-1"></i> Anônimo</span>' : (d.denunciante.nome || 'Identificado')}

&#x20;                       </td>

&#x20;                       <td class="p-4 text-right">

&#x20;                           <button onclick="abrirModal(${originalIndex})" class="px-3 py-1.5 bg-ambiental-50 hover:bg-ambiental-100 text-ambiental-700 rounded-lg text-xs font-semibold transition border border-ambiental-200">

&#x20;                               <i class="fa-solid fa-eye mr-1"></i> Analisar

&#x20;                           </button>

&#x20;                       </td>

&#x20;                   </tr>

&#x20;               `;

&#x20;           });

&#x20;       }



&#x20;       function limparFiltrosAdmin() {

&#x20;           document.getElementById('filtroProtocolo').value = '';

&#x20;           document.getElementById('filtroMunicipio').value = '';

&#x20;           document.getElementById('filtroStatus').value = '';

&#x20;           renderizarTabelaAdmin();

&#x20;       }



&#x20;       function abrirModal(index) {

&#x20;           currentModalIndex = index;

&#x20;           const d = denuncias\[index];



&#x20;           document.getElementById('modalProtocoloTitulo').innerText = `Detalhes da Ocorrência: ${d.id}`;

&#x20;           document.getElementById('modalTipo').innerText = d.tipoInfracao;

&#x20;           document.getElementById('modalData').innerText = d.data;

&#x20;           document.getElementById('modalMunicipio').innerText = d.municipio;

&#x20;           document.getElementById('modalEndereco').innerText = `${d.endereco} ${d.coordenadas ? '(' + d.coordenadas + ')' : ''}`;

&#x20;           document.getElementById('modalDescricao').innerText = d.descricao;

&#x20;           document.getElementById('modalStatusSelect').value = d.status;

&#x20;           document.getElementById('modalObsInternas').value = d.obsInternas || '';

&#x20;           document.getElementById('modalEvidencias').innerText = d.evidencias ? d.evidencias : 'Nenhum arquivo enviado';



&#x20;           document.getElementById('modalDetalhes').classList.remove('hidden');

&#x20;       }



&#x20;       function fecharModal() {

&#x20;           document.getElementById('modalDetalhes').classList.add('hidden');

&#x20;           currentModalIndex = null;

&#x20;       }



&#x20;       function salvarAlteracoesAdmin() {

&#x20;           if (currentModalIndex !== null) {

&#x20;               const novoStatus = document.getElementById('modalStatusSelect').value;

&#x20;               const novasObs = document.getElementById('modalObsInternas').value;

&#x20;               

&#x20;               denuncias\[currentModalIndex].status = novoStatus;

&#x20;               denuncias\[currentModalIndex].obsInternas = novasObs;

&#x20;               

&#x20;               salvarStorage();

&#x20;               renderizarTabelaAdmin();

&#x20;               fecharModal();

&#x20;               alert('Alterações salvas com sucesso!');

&#x20;           }

&#x20;       }

&#x20;   </script>

</body>

</html>

