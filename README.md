--warning guys don't use this decrypt Script gives you 10 year ban in lobby goto modxpro telegram Channel and use original gg from my Telegram @MODXPRO


 
  gg.alert('👑SCRIPT BY MODXPRO👑')
  HOME = 1
  function HOME()
    MN = gg.choice({
      '╔[🇮🇳] BYPASS LOBBY [GL/KR/VN/TW]\n',
      '╔[🇮🇳] MENU WALLHACK\n╚[ᴛʀᴀɪɴɪɴɢ/ɢᴀᴍᴇ]\n',
      '╔[🇮🇳] MENU HACK╚[LOBBY]\n',
      '☠️ON/OFF DATA ZONA 1&2\n',
      '╔[🇮🇳] EXIT\n╚[𝙴𝚇𝙸𝚃 𝙵𝚁𝙾𝙼 𝚂𝙲𝚁𝙸𝙿𝚃]\n'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏 𝐕𝐈𝐏 MODXPRO👑🇮🇳➤ 📅 %A, %d %B %Y %H:%M%p')))
    if MN == nil then
    else
      if MN == 1 then
        BYPASS()
      end
      if MN == 2 then
        WALLHACK()
      end
      if MN == 3 then
        HACK()
      end
      if MN == 4 then
        ON()
      end
      if MN == 5 then
        CLOSE()
      end
    end
    PUBGM = -1
  end
  
  function BYPASS()
    KUN = gg.choice({
      '👉 BYPASS PUBG GLOBAL 🇮🇳',
      '👉 BYPASS PUBG KR/VN/TW🇮🇳',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 MODXPRO👑🇮🇳\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if KUN == nil then
    else
      if KUN == 1 then
        GL()
      end
      if KUN == 2 then
        KR()
      end
      if KUN == 2 then
        HOME()
      end
    end
    PUBGM = -1
  end
  
  function GL()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('70658~590336;67109377;67109633', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('70658~590336', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    for i, i in ipairs((gg.getResults(99999))) do
      gg.getResults(99999)[i].flags = 4
      gg.getResults(99999)[i].value = '67109633'
      gg.getResults(99999)[i].freeze = true
    end
    gg.addListItems((gg.getResults(99999)))
    gg.clearList()
    gg.clearResults()
    gg.clearResults()
    gg.setVisible(false)
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('196,864;16,842,753::5', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    if gg.getResultCount() == 0 then
      gg.alert('🚫 Bypass Values Not Found🚫\n Restart The Game And Try Again \nPlease Make sure Game is 32bit')
      gg.processKill()
      os.exit()
    else
      gg.searchNumber('196,864', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
      n = gg.getResultCount()
      jz = gg.getResults(n)
      for i = 1, n do
        gg.addListItems({
          [1] = {
            address = jz[i].address - 92,
            flags = 4,
            freeze = true,
            value = 67109633
          }
        })
        gg.addListItems({
          [1] = {
            address = jz[i].address + 84,
            flags = 4,
            freeze = true,
            value = 67109633
          }
        })
        gg.addListItems({
          [1] = {
            address = jz[i].address + 88,
            flags = 4,
            freeze = true,
            value = 67109633
          }
        })
        gg.addListItems({
          [1] = {
            address = jz[i].address + 92,
            flags = 4,
            freeze = true,
            value = 67109633
          }
        })
        gg.addListItems({
          [1] = {
            address = jz[i].address + 240,
            flags = 4,
            freeze = true,
            value = 67109633
          }
        })
        gg.addListItems({
          [1] = {
            address = jz[i].address + 244,
            flags = 4,
            freeze = true,
            value = 67109633
          }
        })
        gg.addListItems({
          [1] = {
            address = jz[i].address + 248,
            flags = 4,
            freeze = true,
            value = 67109633
          }
        })
      end
    end
    gg.setVisible(false)
    gg.clearResults()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.setVisible(false)
    gg.searchNumber('196,864;16,842,753::5', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResultsCount()
    gg.clearList()
    gg.clearResults()
    gg.setRanges(gg.REGION_CODE_APP)
    gg.setVisible(false)
    gg.searchNumber('2.2958874e-41', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_CODE_APP)
    gg.setVisible(false)
    gg.searchNumber('9.21956299e-41', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.setVisible(false)
    gg.searchNumber('135682;144387', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('135682', gg.TYPE_DWORD)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.setVisible(false)
    gg.searchNumber('134658;131586', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('134658', gg.TYPE_DWORD)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.setVisible(false)
    gg.searchNumber('134914;131330', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('134914', gg.TYPE_DWORD)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.setVisible(false)
    gg.searchNumber('133378;262403', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('133378', gg.TYPE_DWORD)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.setVisible(false)
    gg.searchNumber('131586;131842', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('131586', gg.TYPE_DWORD)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.setVisible(false)
    gg.searchNumber('131842;132098', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('131842', gg.TYPE_DWORD)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.setVisible(false)
    gg.searchNumber('132098;133635', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('132098', gg.TYPE_DWORD)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_CODE_APP)
    gg.setVisible(false)
    gg.searchNumber('13,073.3740234375', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.clearList()
    gg.alert('❑ Bypass Succesfull')
  end
  
  function KR()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('196,864;16,842,753::5', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResultCount()
    gg.clearList()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('65795~590336;67109377;67109633;67109633', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('65795~590336', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.getResults(99999)
    gg.editAll('67109633', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_CODE_APP)
    gg.searchNumber('2.2958874e-41', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_CODE_APP)
    gg.searchNumber('9.21956299e-41', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('135682;144387', gg.TYPE_DWORD)
    gg.refineNumber('135682', gg.TYPE_DWORD)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('134658;131586', gg.TYPE_DWORD)
    gg.refineNumber('134658', gg.TYPE_DWORD)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('134914;131330', gg.TYPE_DWORD)
    gg.refineNumber('134914', gg.TYPE_DWORD)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('133378;262403', gg.TYPE_DWORD)
    gg.refineNumber('133378', gg.TYPE_DWORD)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('131586;131842', gg.TYPE_DWORD)
    gg.refineNumber('131586', gg.TYPE_DWORD)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('131842;132098', gg.TYPE_DWORD)
    gg.refineNumber('131842', gg.TYPE_DWORD)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('132098;133635', gg.TYPE_DWORD)
    gg.refineNumber('132098', gg.TYPE_DWORD)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_CODE_APP)
    gg.searchNumber('13,073.3740234375', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(50000)
    gg.editAll('67109633', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.alert('❑ Bypass Succesfull')
  end
  
  function WALLHACK()
    MN1 = gg.choice({
      '🇮🇳 WALLHACK & COLOR\n╰➥  SNAPDRAGON',
      '🇮🇳 WALLHACK & COLOR\n╰➥  OTHER DEVICE',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if MN1 == nil then
    else
      if MN1 == 1 then
        SNAPWHM()
      end
      if MN1 == 2 then
        OTHERWH()
      end
      if MN1 == 3 then
        HOME()
      end
    end
    PUBGM = -1
  end
  
  function SNAPWHM()
    WALL11 = gg.multiChoice({
      '🇮🇳 SNAPDRAGON 400\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 410\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 415\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 425\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 430\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 435\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 439\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 450\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 600\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 615\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 616\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 625\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 636\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 660\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 665\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 675 \n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 710\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 712\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 720\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 820\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 835\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 845\n╰➥ Wh & Color Body',
      '🇮🇳 SNAPDRAGON 855\n╰➥ Wh & Color Body',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if WALL11 == nil then
    else
      if WALL11[1] == true then
        WHC400()
      end
      if WALL11[2] == true then
        WHC410()
      end
      if WALL11[3] == true then
        WHC415()
      end
      if WALL11[4] == true then
        WHC425()
      end
      if WALL11[5] == true then
        WHC430()
      end
      if WALL11[6] == true then
        WHC435()
      end
      if WALL11[7] == true then
        WHC439()
      end
      if WALL11[8] == true then
        WHC450()
      end
      if WALL11[9] == true then
        WHC600()
      end
      if WALL11[10] == true then
        WHC615()
      end
      if WALL11[11] == true then
        WHC616()
      end
      if WALL11[12] == true then
        WHC625()
      end
      if WALL11[13] == true then
        WHC636()
      end
      if WALL11[14] == true then
        WHC660()
      end
      if WALL11[15] == true then
        WHC665()
      end
      if WALL11[16] == true then
        WHC675()
      end
      if WALL11[17] == true then
        WHC710()
      end
      if WALL11[18] == true then
        WHC712()
      end
      if WALL11[19] == true then
        WHC720()
      end
      if WALL11[20] == true then
        WHC820()
      end
      if WALL11[21] == true then
        WHC835()
      end
      if WALL11[22] == true then
        WHC845()
      end
      if WALL11[23] == true then
        WHC855()
      end
      if WALL11[24] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function WHC400()
    CL400 = gg.multiChoice({
      '🇮🇳 COLOR GREEN BODY\n╰➥  Snapdragon 400',
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 400',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO [TELIR ASIN]👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL400 == nil then
    else
      if CL400[1] == true then
        C4001()
      end
      if CL400[2] == true then
        C4002()
      end
      if CL400[3] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C4001()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('228;1,073,741,824;1,073,741,824;229;-1,082,130,432:29', 4, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('1,073,741,824', 4, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('1,123,024,896', 4)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.3631163e-44;2.0;3.5032462e-44;-1.0;3.643376e-44;3.7835059e-44;-1.0;3.9236357e-44;4.0637655e-44;1.0;-127.0:129', 16, false, 536870912, 0, -1)
    gg.searchNumber('2', 16, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', 16)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('8,201;8,202;538,968,081:29', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('8202', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(1)
    gg.editAll('8', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C4002()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('228;1,073,741,824;1,073,741,824;229;-1,082,130,432:29', 4, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('1,073,741,824', 4, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('1,123,024,896', 4)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.3631163e-44;2.0;3.5032462e-44;-1.0;3.643376e-44;3.7835059e-44;-1.0;3.9236357e-44;4.0637655e-44;1.0;-127.0:129', 16, false, 536870912, 0, -1)
    gg.searchNumber('2', 16, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', 16)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.searchNumber('8,200;1,194,344,481;8,201:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(15)
    gg.editAll('8', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WHC410()
    CL410 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 410',
      '🇮🇳 COLOR RED YELLOW BODY\n╰➥  Snapdragon 410',
      '<I{•----» 𝐁𝐀𝐂?? «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL410 == nil then
    else
      if CL410[1] == true then
        C4101()
      end
      if CL410[2] == true then
        C4102()
      end
      if CL410[3] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C4101()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.1949605e-43;3.1809475e-43;2.0;3.2089735e-43', 16, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', 16, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('150', 16)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('8204;8205;1,194,344,451', 4, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('8204', 4, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('15', 4)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1,669,693,440;8205', 4, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('8205', 4, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('8204', 4)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('856128', 4, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(4)
    gg.editAll('856118', 4)
    gg.clearResults()
    gg.searchNumber('196610;1280;196608:25', 4, false, gg.S8GN_EQUAL, 0, -1)
    gg.searchNumber('196608', 4, false)
    gg.getResults(10)
    gg.editAll('9999', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C4102()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.1949605e-43;3.1809475e-43;2.0;3.2089735e-43', 16, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', 16, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('150', 16)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('8204;8205;1,194,344,451', 4, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('8204', 4, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('15', 4)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1,669,693,440;8205', 4, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('8205', 4, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('8204', 4)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.searchNumber('8,200;1,194,344,481;8,201:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(15)
    gg.editAll('8', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WHC415()
    CL415 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 415',
      '🇮🇳 COLOR RED YELLOW BODY\n╰➥  Snapdragon 415',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL415 == nil then
    else
      if CL415[1] == true then
        C4151()
      end
      if CL415[2] == true then
        C4152()
      end
      if CL415[3] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C4151()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('228;1,073,741,824;1,073,741,824;229;-1,082,130,432:29', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('1,073,741,824', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('1,123,024,896', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.3631163e-44;2.0;3.5032462e-44;-1.0;3.643376e-44;3.7835059e-44;-1.0;3.9236357e-44;4.0637655e-44;1.0;-127.0:129', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.1809475e-43;3.1949605e-43;2.0;3.2089735e-43:53', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.14906474e-41;1.14920487e-41', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(69)
    gg.editAll('1.14892461e-41', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C4152()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('228;1,073,741,824;1,073,741,824;229;-1,082,130,432:29', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('1,073,741,824', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('1,123,024,896', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.3631163e-44;2.0;3.5032462e-44;-1.0;3.643376e-44;3.7835059e-44;-1.0;3.9236357e-44;4.0637655e-44;1.0;-127.0:129', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.1809475e-43;3.1949605e-43;2.0;3.2089735e-43:53', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.searchNumber('8,200;1,194,344,481;8,201:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(15)
    gg.editAll('8', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WHC425()
    CL425 = gg.multiChoice({
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 425',
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 425',
      '🇮🇳 COLOR GREEN BODY\n╰➥  Snapdragon 425',
      '🇮🇳 COLOR MIX YELLOW BODY\n╰➥  Snapdragon 425',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL425 == nil then
    else
      if CL425[1] == true then
        C4251()
      end
      if CL425[2] == true then
        C4252()
      end
      if CL425[3] == true then
        C4253()
      end
      if CL425[4] == true then
        C4254()
      end
      if CL425[5] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C4251()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(4)
    gg.searchNumber('3.1949605e-43;2.0;3.2089735e-43:25', 16, false, 536870912, 0, -1)
    gg.searchNumber('2', 16, false, 536870912, 0, -1)
    gg.getResults(100)
    gg.editAll('70', 16)
    gg.toast('WH AKTIF')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1073742854;8200:5', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(10)
    gg.editAll('11', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1,073,742,849;8,200:5', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(10)
    gg.editAll('11', gg.TYPE_DWORD)
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C4252()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(4)
    gg.searchNumber('3.1949605e-43;2.0;3.2089735e-43:25', 16, false, 536870912, 0, -1)
    gg.searchNumber('2', 16, false, 536870912, 0, -1)
    gg.getResults(100)
    gg.editAll('70', 16)
    gg.toast('WH AKTIF')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1,073,742,854;8,204:5', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8204', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(10)
    gg.editAll('74', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C4253()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2.9427268e-44;2.0;3.0828566e-44;-1.0;3.2229865e-44;3.3631163e-44;3.643376e-44:97', 16, false, 536870912, 0, -1)
    gg.searchNumber('2', 16, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', 16)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.1529215e-43;2.0F;3.1669345e-43F;3.1809475e-43:49', 16, false, 536870912, 0, -1)
    gg.searchNumber('2', 16, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', 16)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('227;1,073,741,824;1,073,741,824;-1,082,130,432;1,073,741,824:49', 4, false, 536870912, 0, -1)
    gg.searchNumber('1,073,741,824', 4, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('1,123,024,896', 4)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('856,128', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResultsCount()
    gg.getResults(3)
    gg.editAll('856095', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('196,610;1,280;196,608::25', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('196608', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(5)
    gg.editAll('9999', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C4254()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2.9427268e-44;2.0;3.0828566e-44;-1.0;3.2229865e-44;3.3631163e-44;3.643376e-44:97', 16, false, 536870912, 0, -1)
    gg.searchNumber('2', 16, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', 16)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.1529215e-43;2.0F;3.1669345e-43F;3.1809475e-43:49', 16, false, 536870912, 0, -1)
    gg.searchNumber('2', 16, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', 16)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('227;1,073,741,824;1,073,741,824;-1,082,130,432;1,073,741,824:49', 4, false, 536870912, 0, -1)
    gg.searchNumber('1,073,741,824', 4, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('1,123,024,896', 4)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('856128', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(4)
    gg.editAll('99', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('200761;92;8204;856124;108;196610:409', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8204', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    revert = gg.getResults(1000, nil, nil, nil, nil, nil, nil, nil, nil)
    gg.editAll('1', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WHC430()
    CL430 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 430',
      '🇮🇳 COLOR RED YELLOW BODY\n╰➥  Snapdragon 430',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL430 == nil then
    else
      if CL430[1] == true then
        C4301()
      end
      if CL430[2] == true then
        C4302()
      end
      if CL430[3] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C4301()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('5.8013756e-42F;-5.5695588e-40F;2.0F::100', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2.718519e-43F;3.7615819e-37F;2.0F;-1.0F;-127.0F::520', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(20)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('4,141D;4.7408155e21;-5.5693206e-40;4.814603e21;3.7615819e-37;2:', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(4)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.14906474e-41;1.14920487e-41', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(69)
    gg.editAll('1.14892461e-41', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C4302()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('5.8013756e-42F;-5.5695588e-40F;2.0F::100', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2.718519e-43F;3.7615819e-37F;2.0F;-1.0F;-127.0F::520', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(20)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('4,141D;4.7408155e21;-5.5693206e-40;4.814603e21;3.7615819e-37;2:', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(4)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(131072)
    gg.searchNumber('8,196D;8,192D;8,200D::', 4, false, 536870912, 0, -1)
    gg.searchNumber('8200', 4, false, 536870912, 0, -1)
    gg.getResults(10)
    gg.editAll('7', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WHC435()
    CL435 = gg.multiChoice({
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 435',
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 435',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 ??MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL435 == nil then
    else
      if CL435[1] == true then
        C4351()
      end
      if CL435[2] == true then
        C4352()
      end
      if CL435[3] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C4351()
    gg.toast('👑MODXPRO👑 🇮🇳')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.2229865e-43F;2.0F;-1.0F;-1.0F;2.0F:145', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(360)
    gg.editAll('150', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('27;15;26;23;1,073,741,824;24;-1,082,130,432:61', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('1,073,741,824', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('1,123,024,896', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2;3.7615819e-37;4.814603e21;4.7408149e21', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(20)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2;3.7615819e-37;1.3912552e-19;4.9252829e21', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(20)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2.718519e-43F;3.7615819e-37F;2.0F;-1.0F;1.0F;-127.0F;0.00999999978F::200', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(20)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(131072)
    gg.searchNumber('8,196D;8,192D;8,200D::', 4, false, 536870912, 0, -1)
    gg.searchNumber('8200', 4, false, 536870912, 0, -1)
    gg.getResults(10)
    gg.editAll('7', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C4352()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.2229865e-43F;2.0F;-1.0F;-1.0F;2.0F:145', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(360)
    gg.editAll('150', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('27;15;26;23;1,073,741,824;24;-1,082,130,432:61', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('1,073,741,824', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('1,123,024,896', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2;3.7615819e-37;4.814603e21;4.7408149e21', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(20)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2;3.7615819e-37;1.3912552e-19;4.9252829e21', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(20)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2.718519e-43F;3.7615819e-37F;2.0F;-1.0F;1.0F;-127.0F;0.00999999978F::200', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(20)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.14906474e-41;1.14920487e-41', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(69)
    gg.editAll('1.14892461e-41', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WHC439()
    CL439 = gg.multiChoice({
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 439',
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 439',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL439 == nil then
    else
      if CL439[1] == true then
        C4391()
      end
      if CL439[2] == true then
        C4392()
      end
      if CL439[3] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C4391()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_BAD)
    gg.searchNumber('4,140D;4.7408166e21F;4.7223665e21;0D;0D;0D;0D;0D;0D;-0.0F;2.0F', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_BAD)
    gg.searchNumber('2.718519e-43;2.0F;-1.0F;1.0F;-127F;0.24022650719F;-0.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.setRanges(131072)
    gg.searchNumber('8,196D;8,192D;8,200D::', 4, false, 536870912, 0, -1)
    gg.searchNumber('8200', 4, false, 536870912, 0, -1)
    gg.getResults(10)
    gg.editAll('7', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C4392()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_BAD)
    gg.searchNumber('4,140D;4.7408166e21F;4.7223665e21;0D;0D;0D;0D;0D;0D;-0.0F;2.0F', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_BAD)
    gg.searchNumber('2.718519e-43;2.0F;-1.0F;1.0F;-127F;0.24022650719F;-0.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.14906474e-41;1.14920487e-41', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(69)
    gg.editAll('1.14892461e-41', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WHC450()
    CL450 = gg.multiChoice({
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 450',
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 450',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL450 == nil then
    else
      if CL450[1] == true then
        C4501()
      end
      if CL450[2] == true then
        C4502()
      end
      if CL450[3] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C4501()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('135,215D;4,140D;3.7615819e-37;2::', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(10)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('194D;3.7615819e-37;2;-1;1;-127::', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(10)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.1202013e-19;1.1202017e-19;2::', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(1)
    gg.editAll('9999', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2.718519e-43F;3.7615819e-37F;2.0F;0.00999999978F::200', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber(2, gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('150', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('5.8013756e-42F;-5.5695588e-40F;2.0F::100', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber(2, gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('150', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('4.7961574e21;3.7615819e-37;2::', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber(2, gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('150', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.setRanges(131072)
    gg.searchNumber('8,196D;8,192D;8,200D::', 4, false, 536870912, 0, -1)
    gg.searchNumber('8200', 4, false, 536870912, 0, -1)
    gg.getResults(10)
    gg.editAll('7', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C4502()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('135,215D;4,140D;3.7615819e-37;2::', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(10)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('194D;3.7615819e-37;2;-1;1;-127::', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(10)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.1202013e-19;1.1202017e-19;2::', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(1)
    gg.editAll('9999', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2.718519e-43F;3.7615819e-37F;2.0F;0.00999999978F::200', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber(2, gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('150', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('5.8013756e-42F;-5.5695588e-40F;2.0F::100', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber(2, gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('150', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('4.7961574e21;3.7615819e-37;2::', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber(2, gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('150', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.14906474e-41;1.14920487e-41', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(69)
    gg.editAll('1.14892461e-41', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WHC600()
    CL600 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 600',
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 600',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL600 == nil then
    else
      if CL600[1] == true then
        C6001()
      end
      if CL600[2] == true then
        C6002()
      end
      if CL600[3] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C6001()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('4,140D;4.7408166e21F;4.7223665e21;0D;0D;0D;0D;0D;0D;-0.0F;2.0F', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2.718519e-43;2.0F;-1.0F;1.0F;-127F;0.24022650719F;-0.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.14906474e-41;1.14920487e-41', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(69)
    gg.editAll('1.14892461e-41', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6002()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('4,140D;4.7408166e21F;4.7223665e21;0D;0D;0D;0D;0D;0D;-0.0F;2.0F', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2.718519e-43;2.0F;-1.0F;1.0F;-127F;0.24022650719F;-0.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.setRanges(131072)
    gg.searchNumber('8,196D;8,192D;8,200D::', 4, false, 536870912, 0, -1)
    gg.searchNumber('8200', 4, false, 536870912, 0, -1)
    gg.getResults(10)
    gg.editAll('7', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WHC615()
    CL615 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 615',
      '🇮🇳 COLOR GREEN BODY\n╰➥  Snapdragon 615',
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 615',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL615 == nil then
    else
      if CL615[1] == true then
        C6151()
      end
      if CL615[2] == true then
        C6152()
      end
      if CL615[3] == true then
        C6153()
      end
      if CL615[4] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C6151()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.2229865e-43;2.0;-1.0;-1.0;2.0:145', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('122', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.3631163e-44;2.0;3.5032462e-44;-1.0;3.643376e-44;3.7835059e-44;-1.0;3.9236357e-44;4.0637655e-44;1.0;-127.0:129', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.1809475e-43;3.1949605e-43;2.0;3.2089735e-43:53', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1D;2D;91D:25', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('1;2;91', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(5)
    gg.editAll('5', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6152()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.2229865e-43;2.0;-1.0;-1.0;2.0:145', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('122', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.3631163e-44;2.0;3.5032462e-44;-1.0;3.643376e-44;3.7835059e-44;-1.0;3.9236357e-44;4.0637655e-44;1.0;-127.0:129', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.1809475e-43;3.1949605e-43;2.0;3.2089735e-43:53', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('8.201D;8.202D;538.968.081D:29', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('8201;8202;538968081', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(5)
    gg.editAll('8', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6153()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.2229865e-43;2.0;-1.0;-1.0;2.0:145', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('122', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.3631163e-44;2.0;3.5032462e-44;-1.0;3.643376e-44;3.7835059e-44;-1.0;3.9236357e-44;4.0637655e-44;1.0;-127.0:129', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.1809475e-43;3.1949605e-43;2.0;3.2089735e-43:53', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.setRanges(131072)
    gg.searchNumber('8,196D;8,192D;8,200D::', 4, false, 536870912, 0, -1)
    gg.searchNumber('8200', 4, false, 536870912, 0, -1)
    gg.getResults(10)
    gg.editAll('7', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WHC616()
    CL616 = gg.multiChoice({
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 616',
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 616',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL616 == nil then
    else
      if CL616[1] == true then
        C6161()
      end
      if CL616[2] == true then
        C6162()
      end
      if CL616[3] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C6161()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('4,140D;4.7408166e21F;4.7223665e21;0D;0D;0D;0D;0D;0D;-0.0F;2.0F', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2.718519e-43;2.0F;-1.0F;1.0F;-127F;0.24022650719F;-0.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.setRanges(131072)
    gg.searchNumber('8,196D;8,192D;8,200D::', 4, false, 536870912, 0, -1)
    gg.searchNumber('8200', 4, false, 536870912, 0, -1)
    gg.getResults(10)
    gg.editAll('7', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6162()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('4,140D;4.7408166e21F;4.7223665e21;0D;0D;0D;0D;0D;0D;-0.0F;2.0F', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2.718519e-43;2.0F;-1.0F;1.0F;-127F;0.24022650719F;-0.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(30)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.14906474e-41;1.14920487e-41', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(69)
    gg.editAll('1.14892461e-41', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WHC625()
    CL625 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 625',
      '🇮🇳 COLOR BLUE LORENG\n╰➥  Snapdragon 625',
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 625',
      '🇮🇳 COLOR RED YELLOW\n╰➥  Snapdragon 625',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL625 == nil then
    else
      if CL625[1] == true then
        C6251()
      end
      if CL625[2] == true then
        C6252()
      end
      if CL625[3] == true then
        C6253()
      end
      if CL625[4] == true then
        C6254()
      end
      if CL625[5] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C6251()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('8200D;1194380048D', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('6', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6252()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('768;32769;-2134900717', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('32769', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('10', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('0;32770;-2134900716', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('32770', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('5', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133071;8200;1194380048:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('0E8', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6253()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('8200D;1194380048D', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6254()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_BAD)
    gg.searchNumber('200761;92;8204;856124;108;196610:409', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8204', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(1000, nil, nil, nil, nil, nil, nil, nil, nil)
    gg.editAll('99', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('AKTIF BOR')
  end
  
  function WHC636()
    CL636 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 636',
      '🇮🇳 COLOR GREEN\n╰➥  Snapdragon 636',
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 636',
      '🇮🇳 COLOR BLUE BODY\n╰➥  Snapdragon 636',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL636 == nil then
    else
      if CL636[1] == true then
        C6361()
      end
      if CL636[2] == true then
        C6362()
      end
      if CL636[3] == true then
        C6363()
      end
      if CL636[4] == true then
        C6364()
      end
      if CL636[5] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C6361()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('537133071;8200;1194380048:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('0E8', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('6', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6362()
    gg.toast('👑MODXPRO👑 🇮🇳')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('768;32769;-2134900717', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('32769', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('10', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('0;32770;-2134900716', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('32770', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('5', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133071;8200;1194380048:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('0E8', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6363()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133071;8200;1194380048:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('0E8', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('6', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6364()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.setRanges(gg.REGION_BAD)
    gg.processResume()
    gg.searchNumber('Revo_D({53,127,216,36,121,193,26,104,230,254,83,170,7,76,150,223,56,138,211,35,120,202,26,150,179,2,103,172,246,63,153,226,51,134,217,39,166,190,21,99,199,12,85,159,248,69,145,233,50,133,218,86,115,194,39,108,179,255,81,183,251,72,152})', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    revert = gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil)
    gg.editAll('Revo_D({52,132})', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.searchNumber('Revo_D({52,127,214,33,116,195,21,103,179,54,78,165,245,87,156,226,47,130,211,33,115,193,22,103,230,254,82,170,7,76,147,223,49,151,220,30,114,191,17,119,187,2,81,170})', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    revert = gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil)
    gg.editAll('Revo_D({52,132})', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.searchNumber('Revo_D({57,131,209,33,133,204,24,103,185,21,86,164,247,73,153,234,57,134,217,53,124,201,19,97,177,21,91,162,242,69,148})', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    revert = gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil)
    gg.editAll('Revo_D({52})', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ HAVE FUN!👍')
    gg.setVisible(false)
  end
  
  function WHC660()
    CL660 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 660',
      '🇮🇳 COLOR GRENN BODY\n╰➥  Snapdragon 660',
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 660',
      '🇮🇳 COLOR RED YELLOW BODY\n╰➥  Snapdragon 660',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL660 == nil then
    else
      if CL660[1] == true then
        C6601()
      end
      if CL660[2] == true then
        C6602()
      end
      if CL660[3] == true then
        C6603()
      end
      if CL660[4] == true then
        C6604()
      end
      if CL660[5] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C6601()
    gg.toast('??MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('537133071;8200;1194380048:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('0E8', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('6', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6602()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('768;32769;-2134900717', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('32769', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('10', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('0;32770;-2134900716', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('32770', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('5', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133071;8200;1194380048:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('0E8', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6603()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133071;8200;1194380048:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('0E8', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('6', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6604()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.searchNumber('8,200;1,194,344,481;8,201:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(15)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(131072)
    gg.searchNumber('8,196D;8,192D;8,200D::', 4, false, 536870912, 0, -1)
    gg.searchNumber('8200', 4, false, 536870912, 0, -1)
    gg.getResults(10)
    gg.editAll('7', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
    gg.setVisible(false)
  end
  
  function WHC665()
    CL665 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 665',
      '🇮🇳 COLOR GRENN BODY\n╰➥  Snapdragon 665',
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 665',
      '🇮🇳 COLOR RED YELLOW BODY\n╰➥  Snapdragon 665',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL665 == nil then
    else
      if CL665[1] == true then
        C6651()
      end
      if CL665[2] == true then
        C6652()
      end
      if CL665[3] == true then
        C6653()
      end
      if CL665[4] == true then
        C6654()
      end
      if CL665[5] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C6651()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.searchNumber('"8200;1194344475;8201"', 4, false, 536870912, 0, -1)
    gg.processResume()
    gg.refineNumber('"8200;8201"', 4, false, 536870912, 0, -1)
    gg.processResume()
    gg.getResults(10, nil, nil, nil, nil, nil, nil, nil, nil)
    gg.editAll('"7"', 4)
    gg.processResume()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C662()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('768;32769;-2134900717', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('32769', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('10', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('0;32770;-2134900716', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('32770', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('5', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133071;8200;1194380048:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('0E8', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6653()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133071;8200;1194380048:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('0E8', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('6', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6654()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.searchNumber('8,200;1,194,344,481;8,201:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(15)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(131072)
    gg.searchNumber('8,196D;8,192D;8,200D::', 4, false, 536870912, 0, -1)
    gg.searchNumber('8200', 4, false, 536870912, 0, -1)
    gg.getResults(10)
    gg.editAll('7', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
    gg.setVisible(false)
  end
  
  function WHC675()
    CL675 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 675',
      '🇮🇳 COLOR GRENN BODY\n╰➥  Snapdragon 675',
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 675',
      '🇮🇳 COLOR RED YELLOW BODY\n╰➥  Snapdragon 675',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ ?? %A, %d %B %Y %H:%M%p')))
    if CL675 == nil then
    else
      if CL675[1] == true then
        C6751()
      end
      if CL675[2] == true then
        C6752()
      end
      if CL675[3] == true then
        C6753()
      end
      if CL675[4] == true then
        C674()
      end
      if CL675[5] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C6751()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133071;8200;1194380048:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('0E8', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6752()
    gg.toast('👑MODXPRO👑 🇮🇳')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('768;32769;-2134900717', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('32769', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('10', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('0;32770;-2134900716', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('32770', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('5', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133071;8200;1194380048:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('0E8', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C6753()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133071;8200;1194380048:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('0E8', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('6', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C674()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('1.8948778e-40;4.7408166e21;2.0:93', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('504', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('3.37670946121;3.37548875809;2.0:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('980', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('130', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.searchNumber('8,200;1,194,344,481;8,201:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(15)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(131072)
    gg.searchNumber('8,196D;8,192D;8,200D::', 4, false, 536870912, 0, -1)
    gg.searchNumber('8200', 4, false, 536870912, 0, -1)
    gg.getResults(10)
    gg.editAll('7', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
    gg.setVisible(false)
  end
  
  function WHC710()
    CL710 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 710',
      '🇮🇳 COLOR GRENN BODY\n╰➥  Snapdragon 710',
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 710',
      '🇮🇳 COLOR RED YELLOW BODY\n╰➥  Snapdragon 710',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL710 == nil then
    else
      if CL710[1] == true then
        C7101()
      end
      if CL710[2] == true then
        C7102()
      end
      if CL710[3] == true then
        C7103()
      end
      if CL710[4] == true then
        C7104()
      end
      if CL710[5] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C7101()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133066;8200;1194344459;8201:13', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C7102()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133066;8200;1194344459;8201:13', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C7103()
    gg.toast('👑MODXPRO??')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133071;8200;1194380048:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('0E8', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('6', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C7104()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.searchNumber('8,200;1,194,344,481;8,201:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(15)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(131072)
    gg.searchNumber('8,196D;8,192D;8,200D::', 4, false, 536870912, 0, -1)
    gg.searchNumber('8200', 4, false, 536870912, 0, -1)
    gg.getResults(10)
    gg.editAll('7', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
    gg.setVisible(false)
  end
  
  function WHC712()
    CL712 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 712',
      '🇮🇳 COLOR GRENN BODY\n╰➥  Snapdragon 712',
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 712',
      '🇮🇳 COLOR RED YELLOW BODY\n╰➥  Snapdragon 712',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒??𝐑??𝐏𝐓 𝐕𝐈𝐏 𝐏𝐔𝐁𝐋𝐈𝐂 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL712 == nil then
    else
      if CL712[1] == true then
        C7121()
      end
      if CL712[2] == true then
        C7122()
      end
      if CL712[3] == true then
        C7123()
      end
      if CL712[4] == true then
        C7124()
      end
      if CL712[5] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C7121()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133066;8200;1194344459;8201:13', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C7122()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133066;8200;1194344459;8201:13', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C7123()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.14906474e-41;1.14920487e-41', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(69)
    gg.editAll('1.14892461e-41', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C7124()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑 🇮🇳')
    gg.clearResults()
    gg.searchNumber('8,200;1,194,344,481;8,201:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(15)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(131072)
    gg.searchNumber('8,196D;8,192D;8,200D::', 4, false, 536870912, 0, -1)
    gg.searchNumber('8200', 4, false, 536870912, 0, -1)
    gg.getResults(10)
    gg.editAll('7', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
    gg.setVisible(false)
  end
  
  function WHC720()
    CL720 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 720',
      '🇮🇳 COLOR GRENN BODY\n╰➥  Snapdragon 720',
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 720',
      '🇮🇳 COLOR RED YELLOW BODY\n╰➥  Snapdragon 720',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏  👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL720 == nil then
    else
      if CL720[1] == true then
        C7201()
      end
      if CL720[2] == true then
        C7202()
      end
      if CL720[3] == true then
        C7203()
      end
      if CL720[4] == true then
        C7204()
      end
      if CL720[5] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C7201()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133066;8200;1194344459;8201:13', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C7202()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133066;8200;1194344459;8201:13', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C7203()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.14906474e-41;1.14920487e-41', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(69)
    gg.editAll('1.14892461e-41', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('ACTIVE ✓ ??HAVE FUN!👍')
  end
  
  function C7204()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO??')
    gg.clearResults()
    gg.searchNumber('8,200;1,194,344,481;8,201:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(15)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(131072)
    gg.searchNumber('8,196D;8,192D;8,200D::', 4, false, 536870912, 0, -1)
    gg.searchNumber('8200', 4, false, 536870912, 0, -1)
    gg.getResults(10)
    gg.editAll('7', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
    gg.setVisible(false)
  end
  
  function WHC820()
    CL820 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 820',
      '🇮🇳 COLOR GRENN BODY\n╰➥  Snapdragon 820',
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 820',
      '🇮🇳 COLOR RED YELLOW BODY\n╰➥  Snapdragon 820',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏  👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL820 == nil then
    else
      if CL820[1] == true then
        C8201()
      end
      if CL820[2] == true then
        C8202()
      end
      if CL820[3] == true then
        C8203()
      end
      if CL820[4] == true then
        C8204()
      end
      if CL820[5] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C8201()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('537133066;8200;1194344459;8201:13', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.getResults(63825)
    gg.editAll('6;7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C8202()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133066;8200;1194344459;8201:13', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C8203()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C8204()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.searchNumber('8,200;1,194,344,481;8,201:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(15)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(131072)
    gg.searchNumber('8,196D;8,192D;8,200D::', 4, false, 536870912, 0, -1)
    gg.searchNumber('8200', 4, false, 536870912, 0, -1)
    gg.getResults(10)
    gg.editAll('7', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
    gg.setVisible(false)
  end
  
  function WHC835()
    CL835 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 835',
      '🇮🇳 COLOR GRENN BODY\n╰➥  Snapdragon 835',
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 835',
      '🇮🇳 COLOR RED YELLOW BODY\n╰➥  Snapdragon 835',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏  👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL835 == nil then
    else
      if CL835[1] == true then
        C8351()
      end
      if CL835[2] == true then
        C8352()
      end
      if CL835[3] == true then
        C8353()
      end
      if CL835[4] == true then
        C8354()
      end
      if CL835[5] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C8351()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133066;8200;1194344459;8201:13', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C8352()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.14906474e-41;1.14920487e-41', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(69)
    gg.editAll('1.14892461e-41', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C8353()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(15)
    gg.editAll('6', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C8354()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.searchNumber('8,200;1,194,344,481;8,201:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(15)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(131072)
    gg.searchNumber('8,196D;8,192D;8,200D::', 4, false, 536870912, 0, -1)
    gg.searchNumber('8200', 4, false, 536870912, 0, -1)
    gg.getResults(10)
    gg.editAll('7', 4)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
    gg.setVisible(false)
  end
  
  function WHC845()
  CL845 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 845',
      '🇮🇳 COLOR GRENN BODY\n╰➥  Snapdragon 845',
      '🇮🇳 COLOR RED YELLOW BODY\n╰➥  Snapdragon 845',
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 845',
      '🇮?? COLOR BLUE BODY\n╰➥  Snapdragon 845',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏  👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL845 == nil then
    else
      if CL845[1] == true then
        C8451()
      end
      if CL845[2] == true then
        C8452()
      end
      if CL845[3] == true then
        C8453()
      end
      if CL845[4] == true then
        C8454()
      end
      if CL845[5] == true then
        C8455()
      end
      if CL845[6] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C8451()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('537133066;8200;1194344459;8201:13', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.getResults(63825)
    gg.editAll('6;7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C8452()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133066;8200;1194344459;8201:13', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C8453()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('1.14906474e-41;1.14920487e-41', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(69)
    gg.editAll('1.14892461e-41', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C8454()
    gg.toast('??MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('537133066;8200;1194344459;8201:13', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.getResults(63825)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C8455()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.searchNumber('1,194,344,481;8,201:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(15)
    gg.editAll('8199', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WHC855()
    CL855 = gg.multiChoice({
      '🇮🇳 COLOR YELLOW BODY\n╰➥  Snapdragon 855',
      '🇮🇳 COLOR GRENN BODY\n╰➥  Snapdragon 855',
      '🇮🇳 COLOR GREEN YELLOW\n╰➥  Snapdragon 855',
      '🇮🇳 COLOR RED BODY\n╰➥  Snapdragon 855',
      '🇮🇳 COLOR BLUE BODY\n╰➥  Snapdragon 855',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if CL855 == nil then
    else
      if CL855[1] == true then
        C8551()
      end
      if CL855[2] == true then
        C8552()
      end
      if CL855[3] == true then
        C8553()
      end
      if CL855[4] == true then
        C8554()
      end
      if CL855[5] == true then
        C8555()
      end
      if CL855[6] == true then
        HOME()
      end
      PUBGM = -1
    end
  end
  
  function C8551()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('537133066;8200;1194344459;8201:13', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.getResults(63825)
    gg.editAll('6;7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C8552()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.setRanges(gg.REGION_VIDEO)
    gg.searchNumber('8200;8201:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('100', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(550292)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C8553()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.setRanges(gg.REGION_VIDEO)
    gg.searchNumber('8200;8201:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('100', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(550292)
    gg.editAll('7', gg.TYPE_DWORD)
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
    gg.searchNumber('537133066;8200;1194344459;8201:13', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.refineNumber('8200;8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.getResults(63825)
    gg.editAll('6;7', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function C8554()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('5.1097599e21;8.2676609e-44;2.0:13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('200', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
    gg.searchNumber('2.0;0.69314718246;0.00999999978:29', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('2.0', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineAddress('9B0', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(63825)
    gg.editAll('120', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.searchNumber('1,194,344,481;8,201:5', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('8201', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(15)
    gg.editAll('6', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function OTHERWH()
    MN3 = gg.multiChoice({
      '🇮🇳 EXYNOS 850\n╰➥ Wh & Color Body',
      '🇮🇳 EXYNOS 7570\n╰➥ Wh & Color Body',
      '🇮🇳 EXYNOS 7870\n╰➥ Wh & Color Body',
      '🇮🇳 KIRIN 650\n╰➥ Wh & Color Body',
      '🇮🇳 KIRIN 655\n╰➥ Wh & Color Body',
      '🇮🇳 KIRIN 658\n╰➥ Wh & Color Body',
      '🇮🇳 KIRIN 710\n╰➥ Wh & Color Body',
      '🇮🇳 G90T\n╰➥ Wh & Color Body',
      '🇮🇳 MEDIATEK P10\n╰➥ Wh & Color Body',
      '🇮🇳 MEDIATEK P22\n╰➥ Wh & Color Body',
      '🇮🇳 MEDIATEK P35\n╰➥ Wh & Color Body',
      '🇮🇳 MEDIATEK P60\n╰➥ Wh & Color Body',
      '🇮🇳 MEDIATEK P70\n╰➥ Wh & Color Body',
      '🇮🇳 MEDIATEK X20\n╰➥ Wh & Color Body',
      '🇮🇳 MEDIATEK X25\n╰➥ Wh & Color Body',
      '🇮🇳 EXYNOS RED\n╰➥ Wh & Color Body',
      '🇮🇳 EXYNOS WHITE\n╰➥ Wh & Color Body',
      '🇮🇳 KIRIN GREN\n╰➥ Wh & Color Body',
      '🇮🇳 KIRIN  RED\n╰➥ Wh & Color Body',
      '🇮🇳 KIRIN WHITE\n╰➥ Wh & Color Body',
      '🇮🇳 KIRIN YELLOW\n╰➥ Wh & Color Body',
      '🇮🇳 MEDIATEK GREEN\n╰➥ Wh & Color Body',
      '🇮🇳MEDIATEK RED\n╰➥ Wh & Color Body',
      '🇮🇳 MEDIATEK BLUE\n╰➥ Wh & Color Body',
      '🇮🇳 MEDIATEK WHITE\n╰➥ Wh & Color Body',
      '🇮🇳 MEDIATEK P22 GREEN\n╰➥ Wh & Color Body',
      '🇮🇳 MEDIATEK P22 YELLOW\n╰➥ Wh & Color Body',
      '🇮🇳 MEDIATEK P60 BLUE\n╰➥ Wh & Color Body',
      '🇮🇳 MEDIATEK P60 RED\n╰➥ Wh & Color Body',
      '🇮🇳 MEDIATEK P60 YELLOW\n╰➥ Wh & Color Body',
      '<I{•----» 𝐁𝐀𝐂𝐊 «----•}I>'
    }, nil, (os.date('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO??\n╔➤ 📅 %A, %d %B %Y %H:%M%p')))
    if MN3 == nil then
    else
      if MN3[1] == true then
        WE7420()
      end
      if MN3[2] == true then
        WE7570()
      end
      if MN3[3] == true then
        WE7870()
      end
      if MN3[4] == true then
        KIRIN650()
      end
      if MN3[5] == true then
        KIRIN655()
      end
      if MN3[6] == true then
        KIRIN658()
      end
      if MN3[7] == true then
        KIRIN710()
      end
      if MN3[8] == true then
        KIRIN970()
      end
      if MN3[9] == true then
        WMP10()
      end
      if MN3[10] == true then
        WMP22()
      end
      if MN3[11] == true then
        WMP23()
      end
      if MN3[12] == true then
        WMP60()
      end
      if MN3[13] == true then
        WMP70()
      end
      if MN3[14] == true then
        WMX20()
      end
      if MN3[15] == true then
        WMX25()
      end
      if MN3[16] == true then
        CER()
      end
      if MN3[17] == true then
        CEW()
      end
      if MN3[18] == true then
        CKG()
      end
      if MN3[19] == true then
        CKR()
      end
      if MN3[20] == true then
        CKW()
      end
      if MN3[21] == true then
        CKY()
      end
      if MN3[22] == true then
        CMG()
      end
      if MN3[23] == true then
        CMR()
      end
      if MN3[24] == true then
        CMY()
      end
      if MN3[25] == true then
        CMW()
      end
      if MN3[26] == true then
        CMP22G()
      end
      if MN3[27] == true then
        CMP22Y()
      end
      if MN3[28] == true then
        CMP60B()
      end
      if MN3[29] == true then
        CMP60R()
      end
      if MN3[30] == true then
        CMP60Y()
      end
      if MN3[31] == true then
        HOME()
      end
    end
    PUBGM = -1
  end
  
  function WE7420()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(4)
    gg.searchNumber('360;0;0;0;-640;1;1;1;0;0;0;0;1;360;640;0.5;0;0;0;0.5;1;1;0;0;0;0;0;1;1;1;1;1,098618e-48:373', 16)
    gg.searchNumber('0.5', 16)
    gg.getResults(10)
    gg.editAll('50', 16)
    gg.addListItems({})
    gg.toast('Wallhack Exynos 7420 ')
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.clearResults()
    gg.searchNumber('224D;128D;224D;14D;40D;64D;64D;12D;140D;16D;156D;32D;168D:533', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('40', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(786)
    gg.editAll('40;102', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WE7570()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('360;0;0;0;-640;1;1;1;0;0;0;0;1;360;640;0.5;0;0;0;0.5;1;1;0;0;0;0;0;1;1;1;1;1,098618e-48:373', gg.TYPE_FLOAT)
    gg.searchNumber('0.5', gg.TYPE_FLOAT)
    t = gg.getResults(10)
    gg.editAll('50', gg.TYPE_FLOAT)
    t[1].value = '50'
    t[2].value = '50'
    t[3].value = '50'
    t[4].value = '50'
    t[5].value = '50'
    t[6].value = '50'
    t[1].freeze = true
    t[2].freeze = true
    t[3].freeze = true
    t[4].freeze = true
    t[5].freeze = true
    t[6].freeze = true
    print('addListItems: ', gg.addListItems(t))
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WE7870()
    gg.toast('👑MODXPRO👑')
    gg.searchNumber('0.5;0;1;2', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('0.5', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    revert = gg.getResults(99999, nil, nil, nil, nil, nil, nil, nil, nil)
    gg.editAll('2', gg.TYPE_FLOAT)
    gg.refineNumber('0.5', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    revert = gg.getResults(99999, nil, nil, nil, nil, nil, nil, nil, nil)
    gg.editAll('1', gg.TYPE_FLOAT)
    gg.refineNumber('0.5', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.addListItems((gg.getResults(99999, nil, nil, nil, nil, nil, nil, nil, nil)))
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function KIRIN650()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.searchNumber('8.4077908e-45;4.2038954e-45;1.5694543e-43;1.4012985e-45;2.8025969e-45;268.0;480.0;0.5:149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('0.5', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    revert = gg.getResults(1000, nil, nil, nil, nil, nil, nil, nil, nil)
    for i, i in ipairs((gg.getResults(1000, nil, nil, nil, nil, nil, nil, nil, nil))) do
      if i.flags == gg.TYPE_FLOAT then
        i.value = '1'
        i.freeze = true
      end
    end
    gg.addListItems((gg.getResults(1000, nil, nil, nil, nil, nil, nil, nil, nil)))
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function KIRIN658()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('0.5;1.4012985e-45;1.4012985e-45;3.8115318e-43;2.8025969e-45;2.2958874e-41:125', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('0.5', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    revert = gg.getResults(10, nil, nil, nil, nil, nil, nil, nil, nil)
    for i, i in ipairs((gg.getResults(10, nil, nil, nil, nil, nil, nil, nil, nil))) do
      if i.flags == gg.TYPE_FLOAT then
        i.value = '20'
        i.freeze = true
      end
    end
    gg.addListItems((gg.getResults(10, nil, nil, nil, nil, nil, nil, nil, nil)))
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function KIRIN710()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.searchNumber('1.8367379e-40;4.5917748e-40;4.2038954e-45;1.4012985e-45;1.793662e-43;1.4012985e-45;2.8025969e-45;1.1210388e-44;0.5:281', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('0.5', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    revert = gg.getResults(1, nil, nil, nil, nil, nil, nil, nil, nil)
    for i, i in ipairs((gg.getResults(1, nil, nil, nil, nil, nil, nil, nil, nil))) do
      if i.flags == gg.TYPE_FLOAT then
      end
    end
    gg.addListItems((gg.getResults(1, nil, nil, nil, nil, nil, nil, nil, nil)))
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function KIRIN970()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('8;16;32;48;40::169', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('40', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(10)
    gg.editAll('38', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WMP10()
    gg.toast('👑MODXPRO👑')
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('7.70714155e-44;5.15677835e-43;0.5', gg.TYPE_FLOAT, false, gg.SIGN_FUZZY_EQUAL, 0, -1)
    gg.searchNumber('0.5', gg.TYPE_FLOAT, false, gg.SIGN_FUZZY_EQUAL, 0, -1)
    var = gg.getResults(20)
    gg.editAll('120', gg.TYPE_FLOAT)
    var = gg.getResults(100)
    gg.addListItems(var)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WMP22()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('3', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
    gg.processResume()
    gg.refineAddress('B8', -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1, 0)
    revert = gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil)
    for i, i in ipairs((gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil))) do
      if i.flags == gg.TYPE_FLOAT then
      end
    end
    gg.addListItems((gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil)))
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WMP23()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('1.560;720;2;1.000;2.000;5;3;4:777', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('3', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    var = gg.getResults(6)
    gg.editAll('140', gg.TYPE_FLOAT)
    var = gg.getResults(100)
    gg.addListItems(var)
    gg.clearResults()
    gg.toast('Wallhack Mediatek P35')
  end
  
  function WMP60()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('5.1567783e-43;3.5873241e-43;3.2229865e-44;0.5', gg.TYPE_FLOAT, false, gg.SIGN_FUZZY_EQUAL, 0, -1)
    gg.searchNumber('0.5', gg.TYPE_FLOAT, false, gg.SIGN_FUZZY_EQUAL, 0, -1)
    var = gg.getResults(20)
    gg.editAll('2', gg.TYPE_FLOAT)
    var = gg.getResults(100)
    gg.addListItems(var)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WMP70()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('1.793662e-43;3.5873241e-43;1.1210388e-44;0.5', gg.TYPE_FLOAT, false, gg.SIGN_FUZZY_EQUAL, 0, -1)
    gg.searchNumber('0.5', gg.TYPE_FLOAT, false, gg.SIGN_FUZZY_EQUAL, 0, -1)
    revert = gg.getResults(20)
    gg.editAll('2', gg.TYPE_FLOAT)
    revert = gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil)
    for i, i in ipairs((gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil))) do
      if i.flags == gg.TYPE_FLOAT then
      end
    end
    gg.addListItems((gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil)))
    gg.toast('Done')
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WMX20()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('0.5;360;640;1;1;1;-640;360::', gg.POINTER_WRITABLE, false, gg.SIGN_FUZZY_EQUAL, 0, -1)
    gg.searchNumber('0.5', gg.POINTER_WRITABLE, false, gg.SIGN_FUZZY_EQUAL, 0, -1)
    var = gg.getResults(20)
    gg.editAll('0', gg.POINTER_WRITABLE)
    var = gg.getResults(100)
    gg.addListItems(var)
    gg.clearResults()
    gg.clearResults()
    gg.searchNumber('56;64;48::35', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('56', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('47', gg.TYPE_DWORD)
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function WMX25()
    gg.toast('👑MODXPRO👑')
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('640.0;360;0.5;0;640;360;0.5;12000;0.27913400531;0.56855899096::', gg.POINTER_WRITABLE, false, gg.SIGN_FUZZY_EQUAL, 0, -1)
    gg.searchNumber('0.5', gg.POINTER_WRITABLE, false, gg.SIGN_FUZZY_EQUAL, 0, -1)
    var = gg.getResults(20)
    gg.editAll('2', gg.POINTER_WRITABLE)
    var = gg.getResults(100)
    gg.addListItems(var)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function CER()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('24;802824704;32;2::21', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('24', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(5)
    gg.editAll('22', gg.TYPE_DWORD)
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function CEW()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_ANONYMOUS)
    gg.searchNumber('573.70306396484;0.05499718338;1::50', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('1', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(1)
    gg.editAll('999', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function CKG()
    gg.toast('👑MODXPRO👑 🇮🇳')
    gg.clearResults()
    gg.searchNumber('24;802824704;32;2:21', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('24', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil)
    gg.editAll('20', gg.TYPE_DWORD)
    gg.processResume()
    gg.clearResults()
    gg.toast('👑MODXPRO👑')
  end
  
  function CKR()
    gg.clearResults()
    gg.searchNumber('24;802824704;32;2::21', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineNumber('24', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil)
    gg.editAll('22', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function CKW()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('40D;32D;16D;2D::37', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('40', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('42', gg.TYPE_DWORD)
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function CKY()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('16;32;40;48;40:41', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('40', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(10)
    gg.editAll('36', gg.TYPE_DWORD)
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function CMG()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('16;32;40;48;40:41', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('40', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(10)
    gg.editAll('36', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ ??HAVE FUN!👍')
  end
  
  function CMR()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('56', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('DC', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.getResults(999, nil, nil, nil, nil, nil, nil, nil, nil)
    gg.editAll('32', gg.TYPE_DWORD)
    gg.processResume()
    gg.clearResults()
    gg.setVisible(false)
    gg.toast('Color Mediatek P35 Red Transparan Active')
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function CMY()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('16;32;40;48;40:41', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('40', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(10)
    gg.editAll('36', gg.TYPE_DWORD)
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function CMW()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('802,824,192;48;937,041,920;40;736,370,688;32;802,824,192;48;802,824,192;16;802,824,192;2;2::', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('40', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('28', gg.TYPE_DWORD)
    gg.toast('Colour Mediatek Blue activated!')
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function CMP22G()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('56', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.refineAddress('DC', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
    gg.processResume()
    gg.getResults(999, nil, nil, nil, nil, nil, nil, nil, nil)
    gg.editAll('65', gg.TYPE_DWORD)
    gg.processResume()
    gg.clearResults()
    gg.setVisible(false)
    gg.toast('Color Mediatek Heillo P22 Green')
  end
  
  function CMP22Y()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('65D;32D;34D;35D;70D;36D;72D;38D;86D;40D;41D;43D;44D;118D;45D;60D:569', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('65', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(5)
    gg.editAll('61', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('52D;81D;56D;9D;1D;57D;10D;58D;11D;12D;67D;87D;88D;97D;100D;144D;146D;25D;157D;26D;158D;27D;60D;61D;29D;62D;64D;31D:469', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('56', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(3)
    gg.editAll('41', gg.TYPE_DWORD)
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('39D;96D;41D;99D;42D;43D;44D;55D;148D;56D;57D;58D;59D;60D;61D;62D;9D;63D;65D;67D;68D:581', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('55', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(3)
    gg.editAll('33', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('Color Mediatek Heillo P22 Yellow')
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function CMP60B()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(4)
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('802,824,192;48;937,041,920;40;736,370,688;32;802,824,192;48;802,824,192;16;802,824,192;2;2::', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('40', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('28', gg.TYPE_DWORD)
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function CMP60R()
    gg.toast('👑MODXPRO👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('1.68155816e-44F;1.62092562e-12F;3162688022693019688Q;1.62092562e-12F;2.24207754e-44F:241', gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('3162688022693019688', gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
    revert = gg.getResults(25, nil, nil, nil, nil, nil, nil, nil, nil)
    gg.editAll('38', gg.TYPE_QWORD)
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function CMP60Y()
    gg.toast('👑MODXPRO 👑')
    gg.clearResults()
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.setRanges(gg.REGION_C_ALLOC)
    gg.searchNumber('802,824,192;48;937,041,920;40;736,370,688;32;802,824,192;48;802,824,192;16;802,824,192;2;2::', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('40', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('36', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('ACTIVE ✓ 😆HAVE FUN!👍')
  end
  
  function HACK()
    MN4 = gg.multiChoice({
      'LESS RECOIL [LOBBY]',
      'ANTENA [GAME]',
      'MAGICE BULLET [GAME]',
      'VIEW IPAD [GAME/LOBBY]',
      'AIM LOCK[LOBBY]',
      '🔙 ʙᴀᴄᴋ'
    }, nil, os.date('VIP SCRIPT BY 👑MODXPRO👑\n╔➤ 📅 %A, %d %B %Y %H:%M%p'))
    if MN4 == nil then
    else
      if MN4[1] == true then
        LESS()
      end
      if MN4[2] == true then
        sped()
      end
      if MN4[3] == true then
        MAGIC()
      end
      if MN4[4] == true then
        VIEW()
      end
      if MN4[5] == true then
        LOCK()
      end
     if MN4[6] == true then
     FLYINGPLYR()
     end
        if MN4[7] == true then
        HOME()
      end
    end
    PUBGMH = -1
  end
  
  function LESS()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_DATA)
    gg.searchNumber('-309056968;-298841599;-309061065', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('-298841599', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(5)
    gg.editAll('0', gg.TYPE_DWORD)
    gg.clearResults()
    gg.toast('Less Recoil')
  end
  
  function sped()
    gg.clearResults()
    gg.setRanges(gg.REGION_ANONYMOUS)
    gg.searchNumber('88.50576019287F;87.27782440186F;-100.91194152832F;1F::13', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('88.50576019287F;87.27782440186F;1F', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(6)
    gg.editAll('1.96875;1.96875;999;1.96875;1.96875;999', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('Antena')
  end
  
  function MAGIC()
    gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
    gg.searchNumber('0.10000000149;64.50088500977', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.refineNumber('0.10000000149', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(50)
    gg.editAll('8', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.clearResults()
    gg.setRanges(gg.REGION_ANONYMOUS)
    gg.searchNumber('9.201618;30.5;25', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('30.5;25', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('220', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
    gg.searchNumber('-298284466;-1.304566e23F', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('-298284466', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(99)
    gg.editAll('0', gg.TYPE_DWORD)
    gg.clearResults()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
    gg.searchNumber('-1,883,348,481,058,764,210', gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(99)
    gg.editAll('-1,883,348,485,055,444,540', gg.TYPE_QWORD)
    gg.clearResults()
    gg.toast('MAGIC BULLET ON')
  end
  
  function VIEW()
    so = gg.getRangesList('libUE4.so')[1].start
    py = 58850480
    setvalue(so + py, 16, 254.70928955078)
    gg.toast('VIEW IPAD')
  end
  
  function LOCK()
    gg.clearResults()
    gg.setRanges(gg.REGION_C_DATA)
    gg.searchNumber('360;0.0001;1478828288', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.searchNumber('0.0001', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(100)
    gg.editAll('9999', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.setRanges(gg.REGION_CODE_APP)
    gg.searchNumber('2015175168', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
    gg.getResults(6)
    gg.editAll('0', gg.TYPE_FLOAT)
    gg.clearResults()
    gg.toast('AIM BOT AKTIF')
  end
  
  function ON()
    gg.clearResults()
    gg.setRanges(gg.REGION_CODE_APP)
    gg.searchNumber('220676386071773185', gg.TYPE_QWORD)
    gg.getResults(69)
    gg.editAll('220676386036121600', gg.TYPE_QWORD)
    gg.toast('📵 ɪɴᴛᴇʀɴᴇᴛ ᴅɪsᴄᴏɴɴᴇᴄᴛᴇᴅ 📵')
    gg.sleep(6000)
    gg.editAll('220676386071773185', gg.TYPE_QWORD)
    gg.clearResults()
    gg.toast('✅ ɪɴᴛᴇʀɴᴇᴛ ᴄᴏɴɴᴇᴄᴛᴇᴅ ✅')
  end
  
  
function FLYINGPLYR()
    if antifall == off then
      gg.clearResults()
      gg.setRanges(gg.REGION_ANONYMOUS)
      gg.searchNumber('1024;3000', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
      gg.refineNumber('1024;3000', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
      antif1 = gg.getResults(1000, nil, nil, nil, nil, nil, nil, nil, nil)
      gg.editAll('9999999', gg.TYPE_FLOAT)
      gg.clearResults()
      gg.toast('Parachute Antifall Activated')
      antifall = on
    else
      gg.clearResults()
      gg.setValues(antif1)
      gg.clearResults()
      gg.toast('Parachute Antifall Deactivated')
      antifall = off
    end
  end
  
  
  function CLOSE()
    print('𝐒𝐂𝐑𝐈𝐏𝐓 𝐕𝐈𝐏 👑MODXPRO👑\n')
    os.exit()
  end
  
  while true do
    Time = os.date('%G-%m-%d | Waktu: %H:%M:%S')
    if gg.isVisible(true) then
      gg.setVisible(false)
      HOME()
    end
    if PUBGMH == 1 then
      HOME()
    end
  end

