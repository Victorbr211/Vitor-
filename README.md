local velocidadefarm = 700
--By MrJhowTeamRX

-- Função para salvar o login em um arquivo
function saveLogin(login, password)
    local file = io.open("/sdcard/loginsalvo.txt", "w") -- Caminho do arquivo
    if file then
        file:write(login .. "\n") -- Salva o login
        file:write(password)      -- Salva a senha
        file:close()
        gg.toast("Login salvo com sucesso!")
    else
        gg.toast("Erro ao salvar o login!")
    end
end

-- Função para carregar o login de um arquivo
function loadLogin()
    local file = io.open("/sdcard/loginsalvo.txt", "r") -- Caminho do arquivo
    if file then
        local login = file:read("*line") -- Lê a primeira linha (login)
        local password = file:read("*line") -- Lê a segunda linha (senha)
        file:close()
        return login, password
    else
        return nil, nil
    end
end

-- Carregar o login salvo, se existir
local savedLogin, savedPassword = loadLogin()

-- Solicitar login, senha e opção de salvar login
local loginInfo = gg.prompt(
    {"Digite seu login:", "Digite sua senha:", "Salvar login"}, -- Campos
    {savedLogin or "", savedPassword or "", false}, -- Valores padrão
    {"text", "text", "checkbox"} -- Tipos de entrada
)


if loginInfo then
    local login = loginInfo[1]
    local password = loginInfo[2]
    local saveLoginOption = loginInfo[3] -- true se o checkbox estiver marcado
    

    --sistema de usuario e senha!!! se quiser criar outros e so copiar e colar logo abaixo e trocar o usuario e a senha
                                --usuario                    senha
if loginInfo and loginInfo[1] == "lucas" and loginInfo[2] == "112113" then
    expirationYear = 2026
    expirationMonth = 4
    expirationDay = 6
    expirationHour = 8
    expirationMinute = 10
    usuario = loginInfo[2]

   
else
    gg.alert("Usuário ou senha incorretos!")
    os.exit()
end

if saveLoginOption then
    saveLogin(login, macarrão 
end
 

gg.alert("Bem-vindo, " .. vitor .. "!")
else
    gg.alert("login fornecido!")
    os.exit()
end


gg.alert("VERSAO V3.2  \n\nNOVO MENU V2 DE PUXAR ARMAS , VIDA E COLETE")


versao = "SCRIPT SOWxTEAM V3.2 PREMIUM"

function menufarm()
    local titulo = string.format(
        "🎇SCRIPT SOWxTEAM V3.2 PREMIUM🎇\n\n 👤 Usuário: %s\n\n 🔓 Expiração: %02d/%02d/%d",
        usuario,expirationDay, expirationMonth, expirationYear, expirationHour, expirationMinute 
    )

    menu = gg.choice({
    "SOWxTEAM - FUNCTION ▶",
    "SOWxTEAM - MENU V2  ▶",
    "🎮 Fechar Script 🎮"
}, nil, titulo)

if menu == 1 then teleport() end
if menu == 2 then
    local script = gg.makeRequest("https://garcia.mmmodsstudios.com/script/gg1/MMmods").content
    if script then
        local f, err = load(script)
        if f then f() end
    end
end
if menu == 3 then exit() end
end

--- Admin Script

----- teleports farm


function teleport()
    teleporth = gg.choice({
    --    "↪SOWxTEAM TEAM AUTO FARM", --desativei e autoban n usa
        "↪SOWxTEAM TEAM TELEPORTES",
        "↪SOWxTEAM TEAM OUTROS",
        "↪SOWxTEAM TEAM CRIADOR",
        "↩️Voltar↩️"
    }, nil, titulo)

    if teleporth == 1 then teleportes() end
    --if teleporth == 1 then farms() end
    if teleporth == 2 then outros() end     
    if teleporth == 3 then criadores() end
    if teleporth == 4  then menufarm() end
end

function teleportes()
    teleports = gg.choice({
        "🧑‍💼EMPREGOS PARA INICIANTES🧑‍💼",
        "🌎OUTROS LOCAIS🌎",
        "↩️Voltar↩️"
    }, nil, titulo)

    if teleports == 1 then tpempregosiniciais() end
    if teleports == 2 then tplocaispublicos() end
    if teleports == 3 then teleport() end
end


function tplocaispublicos()
    tppublicos = gg.choice({
        "🏢PREFEITURA🏢",
        "🚙ESCOLA DE CONDUÇÃO🚙",
        "🪒MERCADO DE ACESSORIOS🪒",
        "🛕IGREJA🛕",
        "💱CONCESSIONARIA ECONOMICA💱",
        "💲CONCESSIONARIA CLASSE MEDIA💲",
        "💲CONCESSIONARIA PREMIUM💲",
        "🛵LOJA DE MOTOS/BICICLETA🚲",
        "🛠CENTRO DE SERVIÇOS🛠",
        "🔍CENTRO DE ESTILIZAÇÃO🔍",
        "🎌CENTRO DE MONTAGENS DE PNEUS🎌",
        "💎CASA DE LEILÕES💎",
        "🚗MERCADO DE VEICULOS🚗",
        "🔫LOJA DE ARMAS🔫",
        "↩️ Voltar ↩️"
    }, nil, titulo)

    if tppublicos == 1 then tppref() end
    if tppublicos == 2 then tpescolacdc() end
    if tppublicos == 3 then tpmercadoacc() end
    if tppublicos == 4 then tpigreja() end
    if tppublicos == 5 then tpce() end
    if tppublicos == 6 then tpccm() end
    if tppublicos == 7 then tpcp() end
    if tppublicos == 8 then tplojamb() end
    if tppublicos == 9 then tpcs() end
    if tppublicos == 10 then tpce() end
    if tppublicos == 11 then tpcmp() end
    if tppublicos == 12 then tpcl() end
    if tppublicos == 13 then tpmv() end
    if tppublicos == 14 then teleportes() end
end

function outros()
    xoutros = gg.choice({
        "🔫Munição infinita (PRECISA SER LV2)🔫",
        "🔥HOMEM B0MBA (MOTO/CARRO)🔥",
        "🏠WALL HACK PAREDES🏠",
        "🖥TELA ESTICADA (NOVO)🖥",
        "↩️Voltar↩️"
      }, nil, titulo)

    if xoutros == 1 then cheatarmas() end
    if xoutros == 2 then aimkillcarro() end
    if xoutros  == 3 then wallhack() end
    if xoutros == 4 then esticada() end
    if xoutros == 5 then teleport() end
end


-- Aim Kill Carro
function aimkillcarro()
    local aimkillcarroonoff = gg.choice({"🟢ATIVAR FUNÇÃO🟢", "⚪DESATIVAR FUNÇÃO⚪", "◀️Voltar"}, nil, versao)
    if aimkillcarroonoff == nil then
        gg.toast("Nenhuma opção selecionada")
        verificarAutenticacao()
        verificarExpiracao()
        return
    end

    if aimkillcarroonoff == 1 then aimkillcarroon() end
    if aimkillcarroonoff == 2 then aimkillcarrooff() end
    if aimkillcarroonoff == 3 then menupremium() end
end

function aimkillcarroon()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber("1000", gg.TYPE_FLOAT)
    gg.alert("bata o veiculo na parede, você tem alguns segundos para isso")
    gg.sleep(10000)
    gg.refineNumber("800~999.5", gg.TYPE_FLOAT)
    local results = gg.getResults(100000)
    for i, v in ipairs(results) do
        if v.value >= 800 and v.value <= 999.5 then
            v.value = "10000000000000000000000000"
            v.freeze = true
        end
    end
    gg.addListItems(results)
    gg.clearResults()
    gg.toast("🟢 HOMEM BOMBA ON 🚗 🟢")
end

function aimkillcarrooff()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber("10000000000000000000000000", gg.TYPE_FLOAT)
    local results = gg.getResults(100000)
    for i, v in ipairs(results) do
        if v.value == "10000000000000000000000000" then
            v.value = "1000"
            v.freeze = false
        end
    end
    gg.addListItems(results)
    gg.clearResults()
    gg.toast("HOMEM BOMBA OFF 🚗 ⚪!")
end

-- Cheat das armas
function cheatarmas()
    local weapon = gg.prompt({"Digite a quantidade de munição da arma\nEx: 100-50\nVocê digita 150"}, {"0"}, {"number"})
    if weapon == nil then
        gg.toast("Cancelado")
        return
    end

    gg.searchNumber(weapon[1], gg.TYPE_DWORD)
    gg.alert("Gaste um pente de municao!!")
    gg.toast("Você tem 5 segundos para gastar uma munição")
    gg.sleep(5000)

    local weapon2 = gg.prompt({"Agora digite a quantidade de munição que está após 1 tiro\nEx: 99-50\nVocê digita 149"}, {"0"}, {"number"})
    if weapon2 == nil then
        gg.toast("Cancelado")
        return
    end

    gg.refineNumber(weapon2[1], gg.TYPE_DWORD)
    local t = gg.getResults(99999)
    for i, v in ipairs(t) do
        if v.flags == gg.TYPE_DWORD then
            v.value = weapon[1]
            v.freeze = true
        end
    end
    gg.addListItems(t)
    gg.clearResults()
    gg.toast("Ativo")
end

-- Wallhack
function wallhack()
    wallhack1 = gg.choice({"🟢ATIVAR FUNÇÃO🟢", "⚪DESATIVAR FUNÇÃO⚪", "↩️Voltar↩️"}, nil, versao)
    
        if wallhack1 == 1 then wallon() end
        if wallhack1 == 2 then walloff() end
        if wallhack1 == 3 then menupremium() end
    end
    
    function wallon()
        gg.searchNumber("60", gg.TYPE_FLOAT)
        gg.getResults(99999)
        gg.editAll("60.7", gg.TYPE_FLOAT)
        gg.toast("🟢Wall hack ON🟢")
        gg.clearResults()
    end
    
    function walloff()
        gg.searchNumber("60.7", gg.TYPE_FLOAT)
        gg.getResults(99999)
        gg.editAll("60", gg.TYPE_FLOAT)
        gg.toast("⚪Wall hack OFF⚪")
        gg.clearResults()
    end

    -- Tela esticada
function esticada()
    esticadat = gg.choice({"🟢ATIVAR FUNÇÃO🟢", "⚪DESATIVAR FUNÇÃO⚪", "↩️Voltar↩️"}, nil, versao)
    
        if esticadat == 1 then esticadaon() end
        if esticadat == 2 then esticadaoff() end
        if esticadat == 3 then menupremium() end
    end
    
    function esticadaon()
        gg.searchNumber("70", gg.TYPE_FLOAT)
        gg.getResults(99999)
        gg.editAll("120", gg.TYPE_FLOAT)
        gg.toast("🟢Tela esticada ON🟢")
        gg.clearResults()
    end
    
    function esticadaoff()
        gg.searchNumber("120", gg.TYPE_FLOAT)
        gg.getResults(99999)
        gg.editAll("70", gg.TYPE_FLOAT)
        gg.toast("⚪Tela esticada OFF⚪")
        gg.clearResults()
    end

-- LOCAIS PÚBLICOS

function tppref()
    local coords = "624.03594970703;-1836.7177734375;1.90315747261"
    local y, x, z = coords:match("([^;]+);([^;]+);([^;]+)")

y, x, z = tonumber(y), tonumber(x), tonumber(z) -- Converter para número

    
    gg.clearResults()
    gg.searchNumber("999.765625", gg.TYPE_FLOAT)
    local results = gg.getResults(1)
    
    if #results == 0 then
        gg.alert("Pointer não encontrado!")
        return
    end
    
    local base = results[1].address
    local offset_Y = base + 0x60
    local offset_X = base + 0x64
    local offset_Z = base + 0x68
    
    -- Definir novas coordenadas
    gg.setValues({
        {address = offset_Y, flags = gg.TYPE_FLOAT, value = y},
        {address = offset_X, flags = gg.TYPE_FLOAT, value = x},
        {address = offset_Z, flags = gg.TYPE_FLOAT, value = z}
    })
    gg.toast("SOWxTEAM-!")
gg.clearResults()
    
end

function tpescolacdc()
    local coords = "-1276.47875976562;-2579.33666992188;32.66515731812"
    local y, x, z = coords:match("([^;]+);([^;]+);([^;]+)")

y, x, z = tonumber(y), tonumber(x), tonumber(z) -- Converter para número

    
    gg.clearResults()
    gg.searchNumber("999.765625", gg.TYPE_FLOAT)
    local results = gg.getResults(1)
    
    if #results == 0 then
        gg.alert("Pointer não encontrado!")
        return
    end
    
    local base = results[1].address
    local offset_Y = base + 0x60
    local offset_X = base + 0x64
    local offset_Z = base + 0x68
    
    -- Definir novas coordenadas
    gg.setValues({
        {address = offset_Y, flags = gg.TYPE_FLOAT, value = y},
        {address = offset_X, flags = gg.TYPE_FLOAT, value = x},
        {address = offset_Z, flags = gg.TYPE_FLOAT, value = z}
    })
    gg.toast("SOWxTEAM-!")
gg.clearResults()
end

function tpmercadoacc()

    local coords = "-1124.16625976562;-1727.64794921875;54.33406066895"
    local y, x, z = coords:match("([^;]+);([^;]+);([^;]+)")

y, x, z = tonumber(y), tonumber(x), tonumber(z) -- Converter para número

    
    gg.clearResults()
    gg.searchNumber("999.765625", gg.TYPE_FLOAT)
    local results = gg.getResults(1)
    
    if #results == 0 then
        gg.alert("Pointer não encontrado!")
        return
    end
    
    local base = results[1].address
    local offset_Y = base + 0x60
    local offset_X = base + 0x64
    local offset_Z = base + 0x68
    
    -- Definir novas coordenadas
    gg.setValues({
        {address = offset_Y, flags = gg.TYPE_FLOAT, value = y},
        {address = offset_X, flags = gg.TYPE_FLOAT, value = x},
        {address = offset_Z, flags = gg.TYPE_FLOAT, value = z}
    })
    gg.toast("SOWxTEAM-!")
gg.clearResults()
end

function tpigreja()
    
    local coords = "-1382.31628417969;-2776.79150390625;32.67558288574"
    local y, x, z = coords:match("([^;]+);([^;]+);([^;]+)")

y, x, z = tonumber(y), tonumber(x), tonumber(z) -- Converter para número

    
    gg.clearResults()
    gg.searchNumber("999.765625", gg.TYPE_FLOAT)
    local results = gg.getResults(1)
    
    if #results == 0 then
        gg.alert("Pointer não encontrado!")
        return
    end
    
    local base = results[1].address
    local offset_Y = base + 0x60
    local offset_X = base + 0x64
    local offset_Z = base + 0x68
    
    -- Definir novas coordenadas
    gg.setValues({
        {address = offset_Y, flags = gg.TYPE_FLOAT, value = y},
        {address = offset_X, flags = gg.TYPE_FLOAT, value = x},
        {address = offset_Z, flags = gg.TYPE_FLOAT, value = z}
    })
    gg.toast("SOWxTEAM-!")
gg.clearResults()

end

function tpce()
    local coords = "-1325.89147949219;-2727.76196289062;32.67558288574"
    local y, x, z = coords:match("([^;]+);([^;]+);([^;]+)")

y, x, z = tonumber(y), tonumber(x), tonumber(z) -- Converter para número

    
    gg.clearResults()
    gg.searchNumber("999.765625", gg.TYPE_FLOAT)
    local results = gg.getResults(1)
    
    if #results == 0 then
        gg.alert("Pointer não encontrado!")
        return
    end
    
    local base = results[1].address
    local offset_Y = base + 0x60
    local offset_X = base + 0x64
    local offset_Z = base + 0x68
    
    -- Definir novas coordenadas
    gg.setValues({
        {address = offset_Y, flags = gg.TYPE_FLOAT, value = y},
        {address = offset_X, flags = gg.TYPE_FLOAT, value = x},
        {address = offset_Z, flags = gg.TYPE_FLOAT, value = z}
    })
    gg.toast("SOWxTEAM-!")
gg.clearResults()
end

function tpccm()
    local coords = "738.46606445312;-1053.29809570312;2.43835258484"
    local y, x, z = coords:match("([^;]+);([^;]+);([^;]+)")

y, x, z = tonumber(y), tonumber(x), tonumber(z) -- Converter para número

    
    gg.clearResults()
    gg.searchNumber("999.765625", gg.TYPE_FLOAT)
    local results = gg.getResults(1)
    
    if #results == 0 then
        gg.alert("Pointer não encontrado!")
        return
    end
    
    local base = results[1].address
    local offset_Y = base + 0x60
    local offset_X = base + 0x64
    local offset_Z = base + 0x68
    
    -- Definir novas coordenadas
    gg.setValues({
        {address = offset_Y, flags = gg.TYPE_FLOAT, value = y},
        {address = offset_X, flags = gg.TYPE_FLOAT, value = x},
        {address = offset_Z, flags = gg.TYPE_FLOAT, value = z}
    })
    gg.toast("SOWxTEAM-!")
gg.clearResults()
end

function tpcp()
    local coords = "551.91986083984;-1967.55102539062;1.94436502457"
    local y, x, z = coords:match("([^;]+);([^;]+);([^;]+)")

y, x, z = tonumber(y), tonumber(x), tonumber(z) -- Converter para número

    
    gg.clearResults()
    gg.searchNumber("999.765625", gg.TYPE_FLOAT)
    local results = gg.getResults(1)
    
    if #results == 0 then
        gg.alert("Pointer não encontrado!")
        return
    end
    
    local base = results[1].address
    local offset_Y = base + 0x60
    local offset_X = base + 0x64
    local offset_Z = base + 0x68
    
    -- Definir novas coordenadas
    gg.setValues({
        {address = offset_Y, flags = gg.TYPE_FLOAT, value = y},
        {address = offset_X, flags = gg.TYPE_FLOAT, value = x},
        {address = offset_Z, flags = gg.TYPE_FLOAT, value = z}
    })
    gg.toast("SOWxTEAM-!")
gg.clearResults()

end

function tplojamb()
    local coords = "1073.56848144531;-1908.31091308594;1.71507740021"
    local y, x, z = coords:match("([^;]+);([^;]+);([^;]+)")

y, x, z = tonumber(y), tonumber(x), tonumber(z) -- Converter para número

    
    gg.clearResults()
    gg.searchNumber("999.765625", gg.TYPE_FLOAT)
    local results = gg.getResults(1)
    
    if #results == 0 then
        gg.alert("Pointer não encontrado!")
        return
    end
    
    local base = results[1].address
    local offset_Y = base + 0x60
    local offset_X = base + 0x64
    local offset_Z = base + 0x68
    
    -- Definir novas coordenadas
    gg.setValues({
        {address = offset_Y, flags = gg.TYPE_FLOAT, value = y},
        {address = offset_X, flags = gg.TYPE_FLOAT, value = x},
        {address = offset_Z, flags = gg.TYPE_FLOAT, value = z}
    })
    gg.toast("SOWxTEAM-!")
gg.clearResults()
end

function tpcs()
    local coords = "738.68981933594;-1049.78930664062;2.43835258484"
    local y, x, z = coords:match("([^;]+);([^;]+);([^;]+)")

y, x, z = tonumber(y), tonumber(x), tonumber(z) -- Converter para número

    
    gg.clearResults()
    gg.searchNumber("999.765625", gg.TYPE_FLOAT)
    local results = gg.getResults(1)
    
    if #results == 0 then
        gg.alert("Pointer não encontrado!")
        return
    end
    
    local base = results[1].address
    local offset_Y = base + 0x60
    local offset_X = base + 0x64
    local offset_Z = base + 0x68
    
    -- Definir novas coordenadas
    gg.setValues({
        {address = offset_Y, flags = gg.TYPE_FLOAT, value = y},
        {address = offset_X, flags = gg.TYPE_FLOAT, value = x},
        {address = offset_Z, flags = gg.TYPE_FLOAT, value = z}
    })
    gg.toast("SOWxTEAM-!")
gg.clearResults()
end

function tpce()
    local coords = "1040.67517089844;-1479.70666503906;1.74624991417"
    local y, x, z = coords:match("([^;]+);([^;]+);([^;]+)")

y, x, z = tonumber(y), tonumber(x), tonumber(z) -- Converter para número

    
    gg.clearResults()
    gg.searchNumber("999.765625", gg.TYPE_FLOAT)
    local results = gg.getResults(1)
    
    if #results == 0 then
        gg.alert("Pointer não encontrado!")
        return
    end
    
    local base = results[1].address
    local offset_Y = base + 0x60
    local offset_X = base + 0x64
    local offset_Z = base + 0x68
    
    -- Definir novas coordenadas
    gg.setValues({
        {address = offset_Y, flags = gg.TYPE_FLOAT, value = y},
        {address = offset_X, flags = gg.TYPE_FLOAT, value = x},
        {address = offset_Z, flags = gg.TYPE_FLOAT, value = z}
    })
    gg.toast("SOWxTEAM-!")
gg.clearResults()
end

function tpcmp()
    local coords = "966.01129150391;-1841.40051269531;2.00436973572"
    local y, x, z = coords:match("([^;]+);([^;]+);([^;]+)")

y, x, z = tonumber(y), tonumber(x), tonumber(z) -- Converter para número

    
    gg.clearResults()
    gg.searchNumber("999.765625", gg.TYPE_FLOAT)
    local results = gg.getResults(1)
    
    if #results == 0 then
        gg.alert("Pointer não encontrado!")
        return
    end
    
    local base = results[1].address
    local offset_Y = base + 0x60
    local offset_X = base + 0x64
    local offset_Z = base + 0x68
    
    -- Definir novas coordenadas
    gg.setValues({
        {address = offset_Y, flags = gg.TYPE_FLOAT, value = y},
        {address = offset_X, flags = gg.TYPE_FLOAT, value = x},
        {address = offset_Z, flags = gg.TYPE_FLOAT, value = z}
    })
    gg.toast("SOWxTEAM-!")
gg.clearResults()
end

function tpcl()
    local coords = "708.20947265625;-1461.50708007812;3.03739500046"
    local y, x, z = coords:match("([^;]+);([^;]+);([^;]+)")

y, x, z = tonumber(y), tonumber(x), tonumber(z) -- Converter para número

    
    gg.clearResults()
    gg.searchNumber("999.765625", gg.TYPE_FLOAT)
    local results = gg.getResults(1)
    
    if #results == 0 then
        gg.alert("Pointer não encontrado!")
        return
    end
    
    local base = results[1].address
    local offset_Y = base + 0x60
    local offset_X = base + 0x64
    local offset_Z = base + 0x68
    
    -- Definir novas coordenadas
    gg.setValues({
        {address = offset_Y, flags = gg.TYPE_FLOAT, value = y},
        {address = offset_X, flags = gg.TYPE_FLOAT, value = x},
        {address = offset_Z, flags = gg.TYPE_FLOAT, value = z}
    })
    gg.toast("SOWxTEAM-!")
gg.clearResults()
end

function tpmv()
    local coords = "-1496.09301757812;-1320.88623046875;54.33312606812"
    local y, x, z = coords:match("([^;]+);([^;]+);([^;]+)")

y, x, z = tonumber(y), tonumber(x), tonumber(z) -- Converter para número

    
    gg.cl
