
gg.toast(" ✅SERVER CONNECTED🥳 ")

-- -- -- -- -- -- -- -- -- --  Modify Address Value  -- -- -- -- -- -- -- -- -- -- --

function split(szFullString, szSeparator) local nFindStartIndex = 1 local nSplitIndex = 1 local nSplitArray = {} while true do local nFindLastIndex = string.find (szFullString, szSeparator, nFindStartIndex) if not nFindLastIndex then nSplitArray[nSplitIndex] = string.sub(szFullString, nFindStartIndex, string.len (szFullString)) break end nSplitArray[nSplitIndex] = string.sub (szFullString, nFindStartIndex, nFindLastIndex - 1) nFindStartIndex = nFindLastIndex + string.len (szSeparator) nSplitIndex = nSplitIndex + 1 end return nSplitArray end function xgxc(szpy, qmxg) for x = 1, #(qmxg) do xgpy = szpy + qmxg[x]["offset"] xglx = qmxg[x]["type"] xgsz = qmxg[x]["value"] xgdj = qmxg[x]["freeze"] if xgdj == nil or xgdj == "" then gg.setValues({[1] = {address = xgpy, flags = xglx, value = xgsz}}) else gg.addListItems({[1] = {address = xgpy, flags = xglx, freeze = xgdj, value = xgsz}}) end xgsl = xgsl + 1 xgjg = true end end function xqmnb(qmnb) gg.clearResults() gg.setRanges(qmnb[1]["memory"]) gg.searchNumber(qmnb[3]["value"], qmnb[3]["type"]) if gg.getResultCount() == 0 then gg.toast(qmnb[2]["name"] .. "开启失败") else gg.refineNumber(qmnb[3]["value"], qmnb[3]["type"]) gg.refineNumber(qmnb[3]["value"], qmnb[3]["type"]) gg.refineNumber(qmnb[3]["value"], qmnb[3]["type"]) if gg.getResultCount() == 0 then gg.toast(qmnb[2]["name"] .. "开启失败") else sl = gg.getResults(999999) sz = gg.getResultCount() xgsl = 0 if sz > 999999 then sz = 999999 end for i = 1, sz do pdsz = true for v = 4, #(qmnb) do if pdsz == true then pysz = {} pysz[1] = {} pysz[1].address = sl[i].address + qmnb[v]["offset"] pysz[1].flags = qmnb[v]["type"] szpy = gg.getValues(pysz) pdpd = qmnb[v]["lv"] .. ";" .. szpy[1].value szpd = split(pdpd, ";") tzszpd = szpd[1] pyszpd = szpd[2] if tzszpd == pyszpd then pdjg = true pdsz = true else pdjg = false pdsz = false end end end if pdjg == true then szpy = sl[i].address xgxc(szpy, qmxg) end end if xgjg == true then gg.toast(qmnb[2]["name"] .. "开启成功，一共修改" .. xgsl .. "条数据") else gg.toast(qmnb[2]["name"] .. "未搜索到数据，开启失败") end end end end function SearchWrite(Search, Write, Type) gg.clearResults() gg.setVisible(false) gg.searchNumber(Search[1][1], Type) local count = gg.getResultCount() local result = gg.getResults(count) gg.clearResults() local data = {} local base = Search[1][2] if (count > 0) then for i, v in ipairs(result) do v.isUseful = true end for k=2, #Search do local tmp = {} local offset = Search[k][2] - base local num = Search[k][1] for i, v in ipairs(result) do tmp[#tmp+1] = {} tmp[#tmp].address = v.address + offset tmp[#tmp].flags = v.flags end tmp = gg.getValues(tmp) for i, v in ipairs(tmp) do if ( tostring(v.value) ~= tostring(num) ) then result[i].isUseful = false end end end for i, v in ipairs(result) do if (v.isUseful) then data[#data+1] = v.address end end if (#data > 0) then local t = {} local base = Search[1][2] for i=1, #data do for k, w in ipairs(Write) do offset = w[2] - base t[#t+1] = {} t[#t].address = data[i] + offset t[#t].flags = Type t[#t].value = w[1] if (w[3] == true) then local item = {} item[#item+1] = t[#t] item[#item].freeze = true gg.addListItems(item) end end end gg.setValues(t) gg.toast("开启成功，一共修改"..#t.."条数据") gg.addListItems(t) else gg.toast("未搜索到数据，开启失败", false) return false end else gg.toast("Not Found") return false end end

function setvalue(address,flags,value) local tt={} tt[1]={} tt[1].address=address tt[1].flags=flags tt[1].value=value gg.setValues(tt) end

-- -- -- -- -- -- -- -- -- -- Script Language -- -- -- -- -- -- -- -- -- --

HOME1 = 1
BYPDONE = 0
CMENU = 0
function HOME()
LANGHOME = gg.alert("🌐 اختر لغة السكربت \n🇬🇧 Select your language  ", "⟬ 🇬🇧 English ⟭", "⟬ عربي 🌐 ⟭")
if LANGHOME == nil then
else
if LANGHOME == 1 then
HOME2()
CMENU = 2
end
if LANGHOME == 2 then
HOME1()
CMENU = 1
end
end
PUBGMH = -1
end

-- -- -- -- -- -- -- -- -- -- Home Page -- -- -- -- -- -- -- -- -- --

on = ' [❌] '
off = ' '

antifall = off
fspeed1 = off

function HOME1()
MN = gg.choice({
"🛡️ 『 انتي باند / حماية لوبي 』",
"📂 『 قائمة الول هاك وخصائص الرؤية 』",
"📂 『 قائمة خصائص الأسلحة 』",
"📂 『 قائمة خصائص السرعة 』",
"🚀 『 قفزة / طيران الجيب 』",
"🚗 『 قفزة / طيران الداسيا 』",
"🏎️ 『 قفزة / طيران البقي 』",
"⚡ 『 فلاش سبيد 』 ☠️"..fspeed1,
"☠️ 『 خلطة الملا ( تفعيل بالطيارة ) 』 ☠️",
"☠️ 『 خلطة الملا v2 ( تفعيل بالطيارة ) 』 ☠️",
"🛰️ 『 ترسيت سريع / ᴏɴ - ᴏғғ 』",
"⛔ 『 خروج 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if MN == nil then else
if MN == 1 then ABAN() end
if MN == 2 then BDY() end
if MN == 3 then WEP1() end
if MN == 4 then SPD1() end
if MN == 5 then JEEPJUMP() end
if MN == 6 then DACIAJUMP() end
if MN == 7 then BUGGYJUMP() end
if MN == 8 then FLASHS1() end
if MN == 9 then SENIORKO() end
if MN == 10 then SENIORKO2() end
if MN == 11 then DATAONOFF() end
if MN == 12 then CLOSE() end
end
PUBGMH = -1
end

function HOME2()
MN2 = gg.choice({
"🛡️ 『 ᴀɴᴛɪʙᴀɴ / ɪɴ ʟᴏᴏʙʏ 』",
"📂 『 ᴡᴀʟʟʜᴀᴄᴋ & ᴠɪꜱᴜᴀʟ ᴍᴇɴᴜ 』",
"📂 『 ᴡᴇᴀᴘᴏɴꜱ ꜰᴜɴᴄᴛɪᴏɴꜱ ᴍᴇɴᴜ 』",
"📂 『 ꜱᴘᴇᴇᴅ ꜰᴜɴᴄᴛɪᴏɴꜱ ᴍᴇɴᴜ 』",
"🚀 『 ᴊᴇᴇᴘ ᴊᴜᴍᴘɪɴɢ 』",
"🚗 『 ᴅᴀᴄɪᴀ ᴊᴜᴍᴘɪɴɢ 』",
"🏎️ 『 ʙᴜɢɢʏ ᴊᴜᴍᴘɪɴɢ 』",
"⚡ 『 ғʟᴀsʜ sᴘᴇᴇᴅ 』 ☠️"..fspeed1,
"☠️ 『 ᴏɴᴇ ᴄʟɪᴄᴋ ғᴜʟʟ ʙʀᴜᴛᴀʟ [ᴘʟᴀɴᴇ] 』 ☠️",
"☠️ 『 ᴏɴᴇ ᴄʟɪᴄᴋ ғᴜʟʟ ʙʀᴜᴛᴀʟ v2 [ᴘʟᴀɴᴇ] 』 ☠️",
"🛰️ 『 ᴅᴀᴛᴀ ᴏɴ - ᴏғғ ғᴀsᴛ 』",
"⛔ 『 ᴇ x ɪ ᴛ 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if MN2 == nil then else
if MN2 == 1 then ABAN2() end
if MN2 == 2 then BDY2() end
if MN2 == 3 then WEP2() end
if MN2 == 4 then SPD2() end
if MN2 == 5 then JEEPJUMP() end
if MN2 == 6 then DACIAJUMP() end
if MN2 == 7 then BUGGYJUMP() end
if MN2 == 8 then FLASHS1() end
if MN2 == 9 then SENIORKO() end
if MN2 == 10 then SENIORKO2() end
if MN2 == 11 then DATAONOFF() end
if MN2 == 12 then CLOSE() end
end
PUBGMH = -1
end

-- -- -- -- -- -- -- -- --   Fast Data ON/OFF   -- -- -- -- -- -- -- -- --

function DATAONOFF()
gg.clearResults()                   
gg.setRanges(gg.REGION_CODE_APP)                 
gg.searchNumber('220676386071773185', gg.TYPE_QWORD)                  
gg.getResults(69)                 
gg.editAll('220676386036121600', gg.TYPE_QWORD)          
gg.toast("📵 ɪɴᴛᴇʀɴᴇᴛ ᴅɪsᴄᴏɴɴᴇᴄᴛᴇᴅ 📵")        
gg.sleep(6000)                 
gg.editAll('220676386071773185', gg.TYPE_QWORD)                 
gg.clearResults()
gg.toast("✅ ɪɴᴛᴇʀɴᴇᴛ ᴄᴏɴɴᴇᴄᴛᴇᴅ ✅")
end

function DACIAJUMP()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("30;6;22050", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.refineNumber("30;6;22050", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.refineNumber("30;6;22050", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.refineNumber("30;6;22050", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
revert = gg.getResults(61, nil, nil, nil, nil, nil, nil, nil, nil)
gg.editAll("999", gg.TYPE_FLOAT)
gg.sleep(1000)
if revert ~= nil then gg.setValues(revert) end
gg.clearResults()
end

function BUGGYJUMP()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("0.00111111114;49.9999961853;24.99999809265", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.refineNumber("0.00111111114;49.9999961853;24.99999809265", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.refineNumber("0.00111111114;49.9999961853;24.99999809265", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.refineNumber("0.00111111114;49.9999961853;24.99999809265", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
revert = gg.getResults(61, nil, nil, nil, nil, nil, nil, nil, nil)
gg.editAll("0.04111111114", gg.TYPE_FLOAT)
gg.sleep(1000)
if revert ~= nil then gg.setValues(revert) end
gg.clearResults()
end

function JEEPJUMP()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("45;20;2500", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.refineNumber("45;20;2500", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.refineNumber("45;20;2500", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.refineNumber("45;20;2500", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
revert = gg.getResults(61, nil, nil, nil, nil, nil, nil, nil, nil)
gg.editAll("955", gg.TYPE_FLOAT)
gg.sleep(1000)
if revert ~= nil then gg.setValues(revert) end
gg.clearResults()
end

function FLYINGPLYR()
if antifall == off then
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("1024;3000", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("1024;3000", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
antif1 = gg.getResults(1000, nil, nil, nil, nil, nil, nil, nil, nil)
gg.editAll("9999999", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Parachute Antifall Activated")
antifall = on
else
gg.clearResults()
gg.setValues(antif1)
gg.clearResults()
gg.toast("Parachute Antifall Deactivated")
antifall = off
end
end

-- -- -- -- -- -- -- -- --   Freeze Memory   -- -- -- -- -- -- -- -- --

function ABAN()
TENMINMN = gg.choice({
"⚙️⁩ 『 حماية لوبي لجميع النسخ v1 ( لوبي ) 』",
"⚙️⁩ 『 حماية لوبي لجميع النسخ v2 ( لوبي ) 』",
"⚙️⁩ 『 حماية لوبي لجميع النسخ v3 ( لوبي ) 』",
"⁦➡️⁩ 『 رجوع 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if TENMINMN == nil then else
if TENMINMN == 1 then AABANGL1() end
if TENMINMN == 2 then AABANGL2() end
if TENMINMN == 3 then AABANGL3() end
if TENMINMN == 4 then HOME1() end
end
PUBGMH = -1
end

function ABAN2()
TENMIN2MN = gg.choice({
"⚙️⁩ 『 ᴀɴᴛɪʙᴀɴ ᴀʟʟ ᴠᴇʀsɪᴏɴs v1 ( ʟᴏʙʙʏ ) 』",
"⚙️⁩ 『 ᴀɴᴛɪʙᴀɴ ᴀʟʟ ᴠᴇʀsɪᴏɴs v2 ( ʟᴏʙʙʏ ) 』",
"⚙️⁩ 『 ᴀɴᴛɪʙᴀɴ ᴀʟʟ ᴠᴇʀsɪᴏɴs v3 ( ʟᴏʙʙʏ ) 』",
"⬅️ 『 ʙ ᴀ ᴄ ᴋ 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if TENMIN2MN == nil then else
if TENMIN2MN == 1 then AABANGL1() end
if TENMIN2MN == 2 then AABANGL2() end
if TENMIN2MN == 3 then AABANGL3() end
if TENMIN2MN == 4 then HOME2() end
end
PUBGMH = -1
end

function AABANGL1()
gg.alert("ᴜꜱᴇ ᴏɴʟʏ ʙʏᴘᴀꜱꜱ ᴠ1 ᴏʀ ᴠ2✅")
os.remove("src/main/java/com/google/errorprone/annotations")
os.remove("src/main/java/com/google/errorprone/annotations")
os.remove("src/main/java/com/google/errorprone/annotations/concurrent")
os.remove("third_party.java_src.error_prone.project.annotations.Google_internal")
  
  os.remove("src/main/java/com/google/errorprone/annotations")
  os.remove("src/main/java/com/google/errorprone/annotations")
  os.remove("src/main/java/com/google/errorprone/annotations/concurrent")
  os.remove("third_party.java_src.error_prone.project.annotations.Google_internal")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/cache","/storage/emulated/0/Android/a")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/cache","/storage/emulated/0/Android/b")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/cache","/storage/emulated/0/Android/c")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/cache","/storage/emulated/0/Android/d")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/cache","/storage/emulated/0/Android/e")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/cache","/storage/emulated/0/Android/f")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/cache","/storage/emulated/0/Android/g")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/cache","/storage/emulated/0/Android/h")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/cache","/storage/emulated/0/Android/i")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/cache","/storage/emulated/0/Android/j")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/cache","/storage/emulated/0/Android/k")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/cache","/storage/emulated/0/Android/l")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/cache","/storage/emulated/0/Android/m")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/cache","/storage/emulated/0/Android/n")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/storage/emulated/0/Android/o")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/storage/emulated/0/Android/p")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/storage/emulated/0/Android/q")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/storage/emulated/0/Android/r")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/storage/emulated/0/Android/s")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/storage/emulated/0/Android/t")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/storage/emulated/0/Android/u")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/storage/emulated/0/Android/v")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/storage/emulated/0/Android/w")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/storage/emulated/0/Android/x")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/storage/emulated/0/Android/y")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/storage/emulated/0/Android/z")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/storage/emulated/0/Android/aa")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/storage/emulated/0/Android/bb")
os.rename("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/storage/emulated/0/Android/cc")
os.rename("/sdcard/.backups","/sdcard/Android/.3")
os.rename("/sdcard/.backups","/sdcard/Android/.5")
os.rename("/sdcard/.backups","/sdcard/Android/.2")
os.rename("/sdcard/tencent","/sdcard/Android/.3p")
os.rename("/sdcard/tencent","/sdcard/Android/.5w")
os.rename("/sdcard/tencent","/sdcard/Android/.i2")
os.rename("/sdcard/MidasOversea","/sdcard/Android/.3k")
os.rename("/sdcard/MidasOversea","/sdcard/Android/.j5")
os.rename("/sdcard/MidasOversea","/sdcard/Android/.n2")
os.rename("/sdcard/Android/data/com.pubg.krmobileps/cache","/sdcard/Android/.g8i6")
os.rename("/sdcard/Android/data/com.pubg.krmobileps/files","/sdcard/Android/.ggj6")
os.rename("/sdcard/Android/data/com.pubg.krmobileps/parallel_intl/0/com.pubg.krmobile/cache","/sdcard/Android/.inw6")
os.rename("/sdcard/Android/data/com.pubg.krmobileps/parallel_intl/0/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Logs","/sdcard/Android/.kkgw6")
os.rename("/sdcard/Android/data/com.pubg.krmobileps/parallel_intl/0/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/GameErrorNoRecords","/sdcard/Android/.jkgw6")
os.rename("/sdcard/Android/data/com.pubg.krmobileps/parallel_intl/0/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/playerprefs.json","/sdcard/Android/.lvgw6")
os.rename("/sdcard/Android/data/com.pubg.krmobileps/parallel_intl/0/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/playerprefs.sav","/sdcard/Android/.ljgw6")
os.rename("/sdcard/Android/data/com.pubg.krmobileps/parallel_intl/0/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/ChoosingZoneId.sav","/sdcard/Android/.dhgw6")
os.rename("/storage/emulated/0/parallel_intl","/sdcard/Android/gw6")
gg.clearResults()
os.remove("src/main/java/com/google/errorprone/annotations")
os.remove("src/main/java/com/google/errorprone/annotations")
os.remove("src/main/java/com/google/errorprone/annotations/concurrent")
os.remove("third_party.java_src.error_prone.project.annotations.Google_internal")
os.remove("src/main/java/com/google/errorprone/annotations")
os.remove("src/main/java/com/google/errorprone/annotations")
os.remove("src/main/java/com/google/errorprone/annotations/concurrent")
os.remove("third_party.java_src.error_prone.project.annotations.Google_internal")
gg.clearList()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("133378;262403", gg.TYPE_DWORD)
gg.refineNumber("133378", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109633", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("133378;144387", gg.TYPE_DWORD)
gg.refineNumber("133378", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109633", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("134658;135682", gg.TYPE_DWORD)
gg.refineNumber("134658", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109633", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("134658;133378", gg.TYPE_DWORD)
gg.refineNumber("133378", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109633", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("134658;144387", gg.TYPE_DWORD)
gg.refineNumber("134658", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109633", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("134658;132098", gg.TYPE_DWORD)
gg.refineNumber("134658", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109633", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("134658;262403", gg.TYPE_DWORD)
gg.refineNumber("262403", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109633", gg.TYPE_DWORD)
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("135682;132098", gg.TYPE_DWORD)
gg.refineNumber("132098", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109633", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("135682;262403", gg.TYPE_DWORD)
gg.refineNumber("135682", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109633", gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("144387;132098", gg.TYPE_DWORD)
gg.refineNumber("144387", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109633", gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("144387;131330", gg.TYPE_DWORD)
gg.refineNumber("144387", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109633", gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("196864", gg.TYPE_DWORD)
gg.refineNumber("196864", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109633", gg.TYPE_DWORD)
gg.clearResults()
gg.clearList()
gg.setRanges(gg.REGION_CODE_APP)
gg.searchNumber("9.21956299e-41", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.refineNumber("9.21956299e-41;9.21956299e-41", 16, false, 536870912, 0, -1, 0)
gg.refineNumber("9.21956299e-41;9.21956299e-41;9.21956299e-41", 16, false, 536870912, 0, -1, 0)
gg.refineNumber("9.21956299e-41;9.21956299e-41;9.21956299e-41;9.21956299e-41", 16, false, 536870912, 0, -1, 0)
gg.getResults(100)
gg.getResults(100)
gg.clearResults()
gg.clearList()
gg.toast("80% done")
gg.clearResults()
gg.toast("90%_DONE")
gg.alert("Bypass done")
gg.clearResults()
gg.clearList()
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/GameErrorNoRecords")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AntiCheat.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/IGH5CachePluginConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/cache")
gg.clearResults() 
gg.alert(" Antiban Has Been Activated V1 ✅")
end

function AABANGL2()
gg.alert("ᴜꜱᴇ ᴏɴʟʏ ʙʏᴘᴀꜱꜱ ᴠ1 ᴏʀ ᴠ2✅")
os.remove("src/main/java/com/google/errorprone/annotations")
os.remove("src/main/java/com/google/errorprone/annotations/concurrent")
os.remove("third_party.java_src.error_prone.project.annotations.Google_internal")
os.remove("src/main/java/com/google/errorprone/annotations")
os.remove("src/main/java/com/google/errorprone/annotations/concurrent")
os.remove("third_party.java_src.error_prone.project.annotations.Google_internal")
os.remove("src/main/java/com/google/errorprone/annotations")
os.remove("src/main/java/com/google/errorprone/annotations/concurrent")
os.remove("third_party.java_src.error_prone.project.annotations.Google_internal")
gg.clearList()
gg.clearResults()
os.remove(("/data/data/com.tencent.ig/app_crashrecord/1004"))
os.remove(("/data/data/com.tencent.ig/files/__tsecache.dat"))
os.remove(("/data/data/com.tencent.ig/files/AdjustAttribution"))
os.remove(("/data/data/com.tencent.ig/files/AdjustIoActivityState"))
os.remove(("/data/data/com.tencent.ig/files/AdjustIoPackageQueue"))
os.remove(("/data/data/com.tencent.ig/files/apm_cc"))
os.remove(("/data/data/com.tencent.ig/files/AppEventsLogger.persistedevents"))
os.remove(("/data/data/com.tencent.ig/files/cache.crc.dat"))
os.remove(("/data/data/com.tencent.ig/files/gcTestConfig.txt"))
os.remove(("/data/data/com.tencent.ig/files/hawk_data_init"))
os.remove(("/data/data/com.tencent.ig/files/local_crash_lock"))
os.remove(("/data/data/com.tencent.ig/files/tersafe.update"))
os.remove(("/data/data/com.tencent.ig/files/mycpuinfo"))
os.remove(("/data/data/com.tencent.ig/files/tpnlcache.data"))
os.remove(("/data/data/com.tencent.ig/files/tss_app_915c.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss_cs_stat2.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss_uts_c2.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss.i.m.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss_tmp/config2.xml.6dab626b"))
os.remove(("/data/data/com.tencent.ig/files/tss_tmp/config3.xml"))
os.remove(("/data/data/com.tencent.ig/files/tss_tmp/mn_cache.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss_tmp/tss_emu_c2.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss_tmp/tss.ano2.dat"))
os.remove(("/storage/emulated/0/tencent/Midas/Log/com.pubg.krmobile/MidasLog.mmap"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/cacheFile.txt"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/cache/GCloud.config"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/vmpcloudconfig.json"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/login-identifier.txt"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/Epic Games/KeyValueStore.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Intermediate/SaveGames/JKGuestRegisterCnt.json"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AntiCheat.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AppBaseConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AppConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AudioPluginConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/BuildConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/CustomDeviceList.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/DeviceProfiles.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/DeviceSwitchers.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/EditorPerProjectUserSettings.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Engine.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Game.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/GameUserSettings.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Hardware.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/IGH5CachePluginConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/IMSDKConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Input.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/LogSuppression.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/MidasConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/OBHttp.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/OpenIDCommand.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/PufferDownloader.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Scalability.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/ServerSwitch.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/UAE.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Updater.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/UserCustom.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/UserSettings.ini"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Pandora/dns.txt"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/CommonSaveGame_4126599880770857.json"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/LeagueStatue.json"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/loginInfoFile.json"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/MailPhoneLogin.json"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/personalprefs_4123188938540329.json"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/personalprefs_4126599880770857.json"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/playerprefs.json"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/RecruitFilterSetting_4123188938540329.json"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/RecruitFilterSetting_4126599880770857.json"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/business_res_download_priority_table_new"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/cadge_table"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/dubber_table_ext"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/easy_buy_cfg"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/mentor_award_table"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/mentor_task_table"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/new_level_task_cover_table"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/social_authorize_config"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/upgrade_parameter"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/UpdateInfo/apollo_loglist.json"))
os.remove(("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/UpdateInfo/apollo_uuid_define.json"))
os.remove(("/data/data/com.tencent.ig/app_crashrecord/1004"))
os.remove(("/data/data/com.tencent.ig/files/__tsecache.dat"))
os.remove(("/data/data/com.tencent.ig/files/AdjustAttribution"))
os.remove(("/data/data/com.tencent.ig/files/AdjustIoActivityState"))
os.remove(("/data/data/com.tencent.ig/files/AdjustIoPackageQueue"))
os.remove(("/data/data/com.tencent.ig/files/apm_cc"))
os.remove(("/data/data/com.tencent.ig/files/AppEventsLogger.persistedevents"))
os.remove(("/data/data/com.tencent.ig/files/cache.crc.dat"))
os.remove(("/data/data/com.tencent.ig/files/gcTestConfig.txt"))
os.remove(("/data/data/com.tencent.ig/files/hawk_data_init"))
os.remove(("/data/data/com.tencent.ig/files/local_crash_lock"))
os.remove(("/data/data/com.tencent.ig/files/tersafe.update"))
os.remove(("/data/data/com.tencent.ig/files/mycpuinfo"))
os.remove(("/data/data/com.tencent.ig/files/tpnlcache.data"))
os.remove(("/data/data/com.tencent.ig/files/tss_app_915c.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss_cs_stat2.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss_uts_c2.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss.i.m.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss_tmp/config2.xml.6dab626b"))
os.remove(("/data/data/com.tencent.ig/files/tss_tmp/config3.xml"))
os.remove(("/data/data/com.tencent.ig/files/tss_tmp/mn_cache.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss_tmp/tss_emu_c2.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss_tmp/tss.ano2.dat"))
os.remove(("/storage/emulated/0/tencent/Midas/Log/com.tencent.ig/MidasLog.mmap"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/cacheFile.txt"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/cache/GCloud.config"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/vmpcloudconfig.json"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/login-identifier.txt"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/Epic Games/KeyValueStore.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Intermediate/SaveGames/JKGuestRegisterCnt.json"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AntiCheat.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AppBaseConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AppConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AudioPluginConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/BuildConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/CustomDeviceList.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/DeviceProfiles.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/DeviceSwitchers.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/EditorPerProjectUserSettings.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Engine.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Game.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/GameUserSettings.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Hardware.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/IGH5CachePluginConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/IMSDKConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Input.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/LogSuppression.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/MidasConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/OBHttp.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/OpenIDCommand.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/PufferDownloader.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Scalability.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/ServerSwitch.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/UAE.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Updater.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/UserCustom.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/UserSettings.ini"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Pandora/dns.txt"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/CommonSaveGame_4126599880770857.json"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/LeagueStatue.json"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/loginInfoFile.json"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/MailPhoneLogin.json"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/personalprefs_4123188938540329.json"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/personalprefs_4126599880770857.json"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/playerprefs.json"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/RecruitFilterSetting_4123188938540329.json"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/RecruitFilterSetting_4126599880770857.json"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/business_res_download_priority_table_new"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/cadge_table"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/dubber_table_ext"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/easy_buy_cfg"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/mentor_award_table"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/mentor_task_table"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/new_level_task_cover_table"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/social_authorize_config"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/upgrade_parameter"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/UpdateInfo/apollo_loglist.json"))
os.remove(("/storage/emulated/0/Android/data/com.tencent.ig/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/UpdateInfo/apollo_uuid_define.json"))
os.remove(("/data/data/com.tencent.ig/app_crashrecord/1004"))
os.remove(("/data/data/com.tencent.ig/files/__tsecache.dat"))
os.remove(("/data/data/com.tencent.ig/files/AdjustAttribution"))
os.remove(("/data/data/com.tencent.ig/files/AdjustIoActivityState"))
os.remove(("/data/data/com.tencent.ig/files/AdjustIoPackageQueue"))
os.remove(("/data/data/com.tencent.ig/files/apm_cc"))
os.remove(("/data/data/com.tencent.ig/files/AppEventsLogger.persistedevents"))
os.remove(("/data/data/com.tencent.ig/files/cache.crc.dat"))
os.remove(("/data/data/com.tencent.ig/files/gcTestConfig.txt"))
os.remove(("/data/data/com.tencent.ig/files/hawk_data_init"))
os.remove(("/data/data/com.tencent.ig/files/local_crash_lock"))
os.remove(("/data/data/com.tencent.ig/files/tersafe.update"))
os.remove(("/data/data/com.tencent.ig/files/mycpuinfo"))
os.remove(("/data/data/com.tencent.ig/files/tpnlcache.data"))
os.remove(("/data/data/com.tencent.ig/files/tss_app_915c.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss_cs_stat2.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss_uts_c2.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss.i.m.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss_tmp/config2.xml.6dab626b"))
os.remove(("/data/data/com.tencent.ig/files/tss_tmp/config3.xml"))
os.remove(("/data/data/com.tencent.ig/files/tss_tmp/mn_cache.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss_tmp/tss_emu_c2.dat"))
os.remove(("/data/data/com.tencent.ig/files/tss_tmp/tss.ano2.dat"))
os.remove(("/storage/emulated/0/tencent/Midas/Log/com.rekoo.pubgm/MidasLog.mmap"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/cacheFile.txt"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/cache/GCloud.config"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/vmpcloudconfig.json"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/login-identifier.txt"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/Epic Games/KeyValueStore.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Intermediate/SaveGames/JKGuestRegisterCnt.json"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AntiCheat.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AppBaseConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AppConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AudioPluginConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/BuildConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/CustomDeviceList.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/DeviceProfiles.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/DeviceSwitchers.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/EditorPerProjectUserSettings.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Engine.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Game.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/GameUserSettings.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Hardware.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/IGH5CachePluginConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/IMSDKConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Input.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/LogSuppression.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/MidasConfig.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/OBHttp.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/OpenIDCommand.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/PufferDownloader.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Scalability.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/ServerSwitch.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/UAE.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Updater.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/UserCustom.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/UserSettings.ini"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Pandora/dns.txt"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/CommonSaveGame_4126599880770857.json"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/LeagueStatue.json"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/loginInfoFile.json"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/MailPhoneLogin.json"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/personalprefs_4123188938540329.json"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/personalprefs_4126599880770857.json"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/playerprefs.json"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/RecruitFilterSetting_4123188938540329.json"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/RecruitFilterSetting_4126599880770857.json"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/business_res_download_priority_table_new"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/cadge_table"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/dubber_table_ext"))
gg.clearResults()
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/easy_buy_cfg"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/mentor_award_table"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/mentor_task_table"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/new_level_task_cover_table"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/social_authorize_config"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/upgrade_parameter"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/UpdateInfo/apollo_loglist.json"))
os.remove(("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/UpdateInfo/apollo_uuid_define.json"))
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("133634;134914", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("133634", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("131842", gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("132098;133635", gg.TYPE_DWORD)
gg.refineNumber("132098", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("131842", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("4096;135682", gg.TYPE_DWORD)
gg.refineNumber("4096", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("131842", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("131586", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("131842", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("131842;132098", gg.TYPE_DWORD)
gg.refineNumber("131842", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("131842", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("133378;134914", gg.TYPE_DWORD)
gg.refineNumber("133378", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("131842", gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("131331;133634", gg.TYPE_DWORD)
gg.refineNumber("131331", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("131842", gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("133634;134658", gg.TYPE_DWORD)
gg.refineNumber("133634", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("131842", gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("134658;134658", gg.TYPE_DWORD)
gg.refineNumber("134658", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("131842", gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("132098;133635", gg.TYPE_DWORD)
gg.refineNumber("132098", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("131842", gg.TYPE_DWORD)
gg.clearResults()
gg.clearList()
gg.clearResults()
gg.clearList()
gg.clearList()
gg.alert(" Antiban Has Been Activated V2 ✅")
gg.clearResults()
gg.clearList()
gg.clearResults()
gg.clearList()
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/GameErrorNoRecords")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AntiCheat.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/IGH5CachePluginConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/cache")
gg.clearResults() 
end

function AABANGL3()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("131330~590336;67109377;67109377", gg.TYPE_DWORD)
gg.refineNumber("131330~590336", gg.TYPE_DWORD)
gg.getResultsCount()
gg.getResults(0)
gg.editAll("67109377", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("134658", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.processResume()
gg.getResults(50000, nil, nil, nil, nil, nil, nil, nil, nil)
gg.editAll("67109377", gg.TYPE_DWORD)
revert = gg.getResults(50000, nil, nil, nil, nil, nil, nil, nil, nil)
local t = gg.getResults(50000, nil, nil, nil, nil, nil, nil, nil, nil)
for i, v in ipairs(t) do
	if v.flags == gg.TYPE_FLOAT then
		v.value = "-1"
		v.freeze = false
	end
end
gg.addListItems(t)
t = nil
gg.clearResults()
gg.processResume()
gg.clearResults()
gg.searchNumber("134914", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.processResume()
gg.getResults(50000, nil, nil, nil, nil, nil, nil, nil, nil)
gg.editAll("67109377", gg.TYPE_DWORD)
revert = gg.getResults(50000, nil, nil, nil, nil, nil, nil, nil, nil)
local t = gg.getResults(50000, nil, nil, nil, nil, nil, nil, nil, nil)
for i, v in ipairs(t) do
	if v.flags == gg.TYPE_FLOAT then
		v.value = "-1"
		v.freeze = false
	end
end
gg.addListItems(t)
t = nil
gg.clearResults()
gg.processResume()
gg.clearResults()
gg.searchNumber("133378", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.processResume()
gg.getResults(50000, nil, nil, nil, nil, nil, nil, nil, nil)
gg.editAll("67109377", gg.TYPE_DWORD)
revert = gg.getResults(50000, nil, nil, nil, nil, nil, nil, nil, nil)
local t = gg.getResults(50000, nil, nil, nil, nil, nil, nil, nil, nil)
for i, v in ipairs(t) do
	if v.flags == gg.TYPE_FLOAT then
		v.value = "-1"
		v.freeze = false
	end
end
gg.addListItems(t)
t = nil
gg.clearResults()
gg.toast("AntiShiit🔧")
gg.clearResults()
gg.processResume()
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("196,864;16,842,753::5", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("196,864", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(50)
gg.refineNumber("67109377", gg.TYPE_DWORD)
gg.getResultsCount()
gg.setRanges(gg.REGION_CODE_APP)
gg.searchNumber("2.2958874e-41", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(50000)
gg.editAll("67109377", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_CODE_APP)
gg.searchNumber("9.21956299e-41", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(50000)
gg.editAll("67109377", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("135682;144387", gg.TYPE_DWORD)
gg.refineNumber("135682", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109377", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("134658;131586", gg.TYPE_DWORD)
gg.refineNumber("134658", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109377", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("134914;131330", gg.TYPE_DWORD)
gg.refineNumber("134914", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109377", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("133378;262403", gg.TYPE_DWORD)
gg.refineNumber("133378", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109377", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("131586;131842", gg.TYPE_DWORD)
gg.refineNumber("131586", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109377", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("131842;132098", gg.TYPE_DWORD)
gg.refineNumber("131842", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109377", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("132098;133635", gg.TYPE_DWORD)
gg.refineNumber("132098", gg.TYPE_DWORD)
gg.getResults(50000)
gg.editAll("67109377", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_CODE_APP)
gg.searchNumber("13,073.3740234375", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(50000)
gg.editAll("67109377", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Wait🥂")
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("134914;131330", gg.TYPE_DWORD)
gg.refineNumber("134914", gg.TYPE_DWORD)
gg.getResults(50500)
gg.editAll("67109377", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("134658;135682", gg.TYPE_DWORD)
gg.refineNumber("134658", gg.TYPE_DWORD)
gg.getResults(50500)
gg.editAll("67109377", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("131586;131842", gg.TYPE_DWORD)
gg.refineNumber("131586", gg.TYPE_DWORD)
gg.getResults(50500)
gg.editAll("67109377", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_ALLOC)
gg.searchNumber("132098;133635", gg.TYPE_DWORD)
gg.refineNumber("132098", gg.TYPE_DWORD)
gg.getResults(50500)
gg.editAll("67109377", gg.TYPE_DWORD)
gg.toast("Waiit bro⌛")
os.remove("/data/data/com.tencent.ig/app_crashrecord/1004")
os.remove("/data/data/com.tencent.ig/files/__tsecache.dat")
os.remove("/data/data/com.tencent.ig/files/AdjustAttribution")
os.remove("/data/data/com.tencent.ig/files/AdjustIoActivityState")
os.remove("/data/data/com.tencent.ig/files/AdjustIoPackageQueue")
os.remove("/data/data/com.tencent.ig/files/apm_cc")
os.remove("/data/data/com.tencent.ig/files/AppEventsLogger.persistedevents")
os.remove("/data/data/com.tencent.ig/files/cache.crc.dat")
os.remove("/data/data/com.tencent.ig/files/gcTestConfig.txt")
os.remove("/data/data/com.tencent.ig/files/hawk_data_init")
os.remove("/data/data/com.tencent.ig/files/local_crash_lock")
os.remove("/data/data/com.tencent.ig/files/tersafe.update")
os.remove("/data/data/com.tencent.ig/files/mycpuinfo")
os.remove("/data/data/com.tencent.ig/files/tpnlcache.data")
os.remove("/data/data/com.tencent.ig/files/tss_app_915c.dat")
os.remove("/data/data/com.tencent.ig/files/tss_cs_stat2.dat")
os.remove("/data/data/com.tencent.ig/files/tss_uts_c2.dat")
os.remove("/data/data/com.tencent.ig/files/tss.i.m.dat")
os.remove("/data/data/com.tencent.ig/files/tss_tmp/config2.xml.6dab626b")
os.remove("/data/data/com.tencent.ig/files/tss_tmp/config3.xml")
os.remove("/data/data/com.tencent.ig/files/tss_tmp/mn_cache.dat")
os.remove("/data/data/com.tencent.ig/files/tss_tmp/tss_emu_c2.dat")
os.remove("/data/data/com.tencent.ig/files/tss_tmp/tss.ano2.dat")
os.remove("/storage/emulated/0/tencent/Midas/Log/com.pubg.krmobile/MidasLog.mmap")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/cacheFile.txt")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/cache/GCloud.config")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/vmpcloudconfig.json")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/login-identifier.txt")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/Epic Games/KeyValueStore.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Intermediate/SaveGames/JKGuestRegisterCnt.json")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AntiCheat.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AppBaseConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AppConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AudioPluginConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/BuildConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/CustomDeviceList.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/DeviceProfiles.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/DeviceSwitchers.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/EditorPerProjectUserSettings.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Engine.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Game.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/GameUserSettings.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Hardware.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/IGH5CachePluginConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/IMSDKConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Input.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/LogSuppression.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/MidasConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/MidasConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/OBHttp.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/OpenIDCommand.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/PufferDownloader.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Scalability.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/ServerSwitch.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/UAE.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Updater.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/UserCustom.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/UserSettings.ini")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Pandora/dns.txt")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/CommonSaveGame_4126599880770857.json")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/LeagueStatue.json")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/loginInfoFile.json")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/MailPhoneLogin.json")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/personalprefs_4123188938540329.json")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/personalprefs_4126599880770857.json")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/playerprefs.json")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/RecruitFilterSetting_4123188938540329.json")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/RecruitFilterSetting_4126599880770857.json")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/business_res_download_priority_table_new")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/cadge_table")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/dubber_table_ext")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/easy_buy_cfg")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/mentor_award_table")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/mentor_task_table")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/new_level_task_cover_table")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/social_authorize_config")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/upgrade_parameter")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/UpdateInfo/apollo_loglist.json")
os.remove("/storage/emulated/0/Android/data/com.pubg.krmobile/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/UpdateInfo/apollo_uuid_define.json")
os.remove("/data/data/com.tencent.ig/app_crashrecord/1004")
os.remove("/data/data/com.tencent.ig/files/__tsecache.dat")
os.remove("/data/data/com.tencent.ig/files/AdjustAttribution")
os.remove("/data/data/com.tencent.ig/files/AdjustIoActivityState")
os.remove("/data/data/com.tencent.ig/files/AdjustIoPackageQueue")
os.remove("/data/data/com.tencent.ig/files/apm_cc")
os.remove("/data/data/com.tencent.ig/files/AppEventsLogger.persistedevents")
os.remove("/data/data/com.tencent.ig/files/cache.crc.dat")
os.remove("/data/data/com.tencent.ig/files/gcTestConfig.txt")
os.remove("/data/data/com.tencent.ig/files/hawk_data_init")
os.remove("/data/data/com.tencent.ig/files/local_crash_lock")
os.remove("/data/data/com.tencent.ig/files/tersafe.update")
os.remove("/data/data/com.tencent.ig/files/mycpuinfo")
os.remove("/data/data/com.tencent.ig/files/tpnlcache.data")
os.remove("/data/data/com.tencent.ig/files/tss_app_915c.dat")
os.remove("/data/data/com.tencent.ig/files/tss_cs_stat2.dat")
os.remove("/data/data/com.tencent.ig/files/tss_uts_c2.dat")
os.remove("/data/data/com.tencent.ig/files/tss.i.m.dat")
os.remove("/data/data/com.tencent.ig/files/tss_tmp/config2.xml.6dab626b")
os.remove("/data/data/com.tencent.ig/files/tss_tmp/config3.xml")
os.remove("/data/data/com.tencent.ig/files/tss_tmp/mn_cache.dat")
os.remove("/data/data/com.tencent.ig/files/tss_tmp/tss_emu_c2.dat")
os.remove("/data/data/com.tencent.ig/files/tss_tmp/tss.ano2.dat")
os.remove("/storage/emulated/0/tencent/Midas/Log/com.tencent.ig/MidasLog.mmap")
os.remove("/storage/emulated/0/Android/data/com.tencent.ig/files/cacheFile.txt")
os.remove("/storage/emulated/0/Android/data/com.tencent.ig/cache/GCloud.config")
os.remove("/storage/emulated/0/Android/data/com.tencent.ig/files/vmpcloudconfig.json")
os.remove("/storage/emulated/0/Android/data/com.tencent.ig/files/login-identifier.txt")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/Epic Games/KeyValueStore.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Intermediate/SaveGames/JKGuestRegisterCnt.json")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AntiCheat.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AppBaseConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AppConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/AudioPluginConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/BuildConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/CustomDeviceList.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/DeviceProfiles.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/DeviceSwitchers.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/EditorPerProjectUserSettings.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Engine.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Game.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/GameUserSettings.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Hardware.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/IGH5CachePluginConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/IMSDKConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Input.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/LogSuppression.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/MidasConfig.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/OBHttp.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/OpenIDCommand.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/PufferDownloader.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Scalability.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/ServerSwitch.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/UAE.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/Updater.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/UserCustom.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Config/Android/UserSettings.ini")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/Pandora/dns.txt")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/CommonSaveGame_4126599880770857.json")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/LeagueStatue.json")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/loginInfoFile.json")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/MailPhoneLogin.json")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/personalprefs_4123188938540329.json")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/personalprefs_4126599880770857.json")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/playerprefs.json")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/RecruitFilterSetting_4123188938540329.json")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/SaveGames/RecruitFilterSetting_4126599880770857.json")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/business_res_download_priority_table_new")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/cadge_table")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/dubber_table_ext")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/easy_buy_cfg")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/mentor_award_table")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/mentor_task_table")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/new_level_task_cover_table")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/social_authorize_config")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/TableDatas/upgrade_parameter")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/UpdateInfo/apollo_loglist.json")
os.remove("/storage/emulated/0/Android/data/com.rekoo.pubgm/files/UE4Game/ShadowTrackerExtra/ShadowTrackerExtra/Saved/UpdateInfo/apollo_uuid_define.json")
gg.alert(" Antiban Has Been Activated V3 ✅")
end

-- -- -- -- -- -- -- --   Wallhack Menu   -- -- -- -- -- -- -- -- --

whitems = off
bsky = off
ipadv = off
antenag = off
godv = off
nfog = off

function BDY()
BDYMN = gg.choice({
"📱 『 قائمة الول هاك 』",
"🎨 『 قائمة الألوان 』",
"📍 『 انتينا 』"..antenag,
"🌱 『 إزاله العشب 』",
"🌒 『 الوضع الليلي 』",
"🎥 『 منظور آيباد 』"..ipadv,
"🌍 『 منظور من السماء 』"..godv,
"🌑 『 لون سماء أسود 』",
"🌫️ 『 إزالة الضباب من الجو 』",
"🌌 『 لون ضباب أزرق 』",
"⁦➡️⁩ 『 رجوع 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if BDYMN == nil then else
if BDYMN == 1 then WH() end
if BDYMN == 2 then CLR() end
if BDYMN == 3 then ANTEENA() end
if BDYMN == 4 then NOGRASSLOBBY() end
if BDYMN == 5 then NIGHTMODE() end
if BDYMN == 6 then IPADVIEW() end
if BDYMN == 7 then GODVIEW() end
if BDYMN == 8 then BLACKSKY() end
if BDYMN == 9 then NOFOG() end
if BDYMN == 10 then BLUEFOG() end
if BDYMN == 11 then HOME1() end
end
PUBGMH = -1
end

function BDY2()
BDYMN2 = gg.choice({
"📱 『 ᴡᴀʟʟʜᴀᴄᴋ ᴍᴇɴᴜ 』",
"🎨 『 ᴄᴏʟᴏʀ ᴍᴇɴᴜ 』",
"📍 『 ᴀɴᴛᴇɴɴᴀ 』"..antenag,
"🌱 『 ɴᴏ ɢʀᴀss 』",
"🌒 『 ɴɪɢʜᴛ ᴍᴏᴅᴇ 』",
"🎥 『 ɪᴘᴀᴅ ᴠɪᴇᴡ 』"..ipadv,
"🌍 『 ɢᴏᴅ ꜱɪᴛ ᴠɪᴇᴡ 』"..godv,
"🌑 『 ʙʟᴀᴄᴋ sᴋʏ 』",
"🌫️ 『 ʀᴇᴍᴏᴠᴇ ғᴏɢ 』",
"🌌 『 ʙʟᴜᴇ ғᴏɢ 』",
"⬅️ 『 ʙ ᴀ ᴄ ᴋ 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if BDYMN2 == nil then else
if BDYMN2 == 1 then WH2() end
if BDYMN2 == 2 then CLR2() end
if BDYMN2 == 3 then ANTEENA() end
if BDYMN2 == 4 then NOGRASSLOBBY() end
if BDYMN2 == 5 then NIGHTMODE() end
if BDYMN2 == 6 then IPADVIEW() end
if BDYMN2 == 7 then GODVIEW() end
if BDYMN2 == 8 then BLACKSKY() end
if BDYMN2 == 9 then NOFOG() end
if BDYMN2 == 10 then BLUEFOG() end
if BDYMN2 == 11 then HOME2() end
end
PUBGMH = -1
end

function GODVIEW()
if godv == off then
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("1099511900928", gg.TYPE_DOUBLE, false, gg.SIGN_EQUAL, 0, -1)
godvs1 = gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil)
gg.editAll("-5.029132178451386e+26", gg.TYPE_DOUBLE)
gg.clearResults()
gg.toast("God View Activated")
godv = on
else
gg.clearResults()
gg.setValues(godvs1)
gg.clearResults()
gg.toast("God View Deactivated")
godv = off
end
end

function ANTEENA() --1.2
if antenag == off then
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("88.50576019287F;87.27782440186F;-100.91194152832F;1F::13", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("88.50576019287F;87.27782440186F;1F", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
antenags1 = gg.getResults(6)
gg.editAll("1.96875;1.96875;999;1.96875;1.96875;999", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Antenna Activated")
antenag = on
else
gg.clearResults()
gg.setValues(antenags1)
gg.clearResults()
gg.toast("Antenna Deactivated")
antenag = off
end
end

function NOGRASSLOBBY() --1.2
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber(":Default__MaterialExpressionLandscapeGrassOutput", gg.TYPE_BYTE, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(500)
gg.editAll("0", gg.TYPE_BYTE)
gg.clearResults()
gg.toast("No Grass Activated")
end

function NIGHTMODE() --1.2
gg.clearResults()
so=gg.getRangesList('libUE4.so')[1].start
py=0x2EFA72C
setvalue(so+py,16,0)
gg.clearResults()
gg.toast("Night Mode Activated")
end

function IPADVIEW() --1.2
if ipadv == off then
gg.clearResults()
so=gg.getRangesList('libUE4.so')[1].start
py=0x381FCB0
setvalue(so+py,16,265)
gg.clearResults()
gg.toast("iPad View Activated")
ipadv = on
else
gg.clearResults()
so=gg.getRangesList('libUE4.so')[1].start
py=0x381FCB0
setvalue(so+py,16,390)
gg.clearResults()
gg.toast("iPad View Deactivated")
ipadv = off
end
end

function BLACKSKY() --1.2
gg.clearResults()
so=gg.getRangesList('libUE4.so')[1].start
py=0x3AD36A0
setvalue(so+py,4,-1222130000)
gg.clearResults()
gg.toast("Black Sky Activated")
end

function NOFOG() --1.2
gg.clearResults()
so=gg.getRangesList('libUE4.so')[1].start
py=0x2D0DA34
setvalue(so+py,16,0)
gg.clearResults()
gg.toast("No Fog Activated")
end

function BLUEFOG()
gg.clearResults()
so=gg.getRangesList('libUE4.so')[1].start
py=0x2D0DA28
setvalue(so+py,4,0)
so=gg.getRangesList('libUE4.so')[1].start
py=0x2D0DA38
setvalue(so+py,4,0)
gg.clearResults()
gg.toast("Blue Fog Activated")
end

-- -- -- -- -- -- -- -- -- --  Wallhack  -- -- -- -- -- -- -- -- -- --

whs425 = off
whs430 = off
whs625 = off
whs6252 = off
whs636 = off
whs660 = off
whs665 = off
whs675 = off
whs6752 = off
whs710 = off
whs730 = off
whs810 = off
whs820 = off
whs835 = off
whs845 = off
whs855 = off
whs865 = off
whsall = off

function WH()
WHMN = gg.choice({
"🔵 『 سناب دراغون 425 』"..whs425,
"🔴 『 سناب دراغون 430 』"..whs430,
"🔵 『 سناب دراغون 625 』"..whs625,
"🔴 『 سناب دراغون 625 v² 』"..whs6252,
"🔵 『 سناب دراغون 636 』"..whs636,
"🔴 『 سناب دراغون 660 』"..whs660,
"🔴 『 سناب دراغون 665 』"..whs665,
"🔵 『 سناب دراغون 675 』"..whs675,
"🔴 『 سناب دراغون 675 v² 』"..whs6752,
"🔵 『 سناب دراغون 710 』"..whs710,
"🔴 『 سناب دراغون 730 』"..whs730,
"🔵 『 سناب دراغون 810 』"..whs810,
"🔴 『 سناب دراغون 820 』"..whs820,
"🔵 『 سناب دراغون 835 』"..whs835,
"🔴 『 سناب دراغون 845 』"..whs845,
"🔵 『 سناب دراغون 855 』"..whs855,
"🔴 『 سناب دراغون 865 』"..whs865,
"⚫ 『 سناب دراغون جميع الأجهزة 』"..whsall,
"🛠️ 『 إصلاح التقطيع 430-835 』",
"🛠️ 『 إصلاح التقطيع 845-855 』",
"⁦➡️⁩ 『 رجوع 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if WHMN == nil then else
if WHMN == 1 then WH425() end
if WHMN == 2 then WH430() end
if WHMN == 3 then WH625() end
if WHMN == 4 then WH6252() end
if WHMN == 5 then WH636() end
if WHMN == 6 then WH660() end
if WHMN == 7 then WH665() end
if WHMN == 8 then WH675() end
if WHMN == 9 then WH6752() end
if WHMN == 10 then WH710() end
if WHMN == 11 then WH730() end
if WHMN == 12 then WH810() end
if WHMN == 13 then WH820() end
if WHMN == 14 then WH835() end
if WHMN == 15 then WH845() end
if WHMN == 16 then WH855() end
if WHMN == 17 then WH865() end
if WHMN == 18 then ALLD() end
if WHMN == 19 then FIXWH() end
if WHMN == 20 then FIXWH2() end
if WHMN == 21 then BDY() end
end
PUBGMH = -1
end

function WH2()
WHMN2 = gg.choice({
"🔵 『 sɴᴀᴘᴅʀᴀɢᴏɴ 425 』"..whs425,
"🔴 『 sɴᴀᴘᴅʀᴀɢᴏɴ 430 』"..whs430,
"🔵 『 sɴᴀᴘᴅʀᴀɢᴏɴ 625 』"..whs625,
"🔴 『 sɴᴀᴘᴅʀᴀɢᴏɴ 625 v² 』"..whs6252,
"🔵 『 sɴᴀᴘᴅʀᴀɢᴏɴ 636 』"..whs636,
"🔴 『 sɴᴀᴘᴅʀᴀɢᴏɴ 660 』"..whs660,
"🔴 『 sɴᴀᴘᴅʀᴀɢᴏɴ 665 』"..whs665,
"🔵 『 sɴᴀᴘᴅʀᴀɢᴏɴ 675 』"..whs675,
"🔴 『 sɴᴀᴘᴅʀᴀɢᴏɴ 675 v² 』"..whs6752,
"🔵 『 sɴᴀᴘᴅʀᴀɢᴏɴ 710 』"..whs710,
"🔴 『 sɴᴀᴘᴅʀᴀɢᴏɴ 730 』"..whs730,
"🔵 『 sɴᴀᴘᴅʀᴀɢᴏɴ 810 』"..whs810,
"🔴 『 sɴᴀᴘᴅʀᴀɢᴏɴ 820 』"..whs820,
"🔵 『 sɴᴀᴘᴅʀᴀɢᴏɴ 835 』"..whs835,
"🔴 『 sɴᴀᴘᴅʀᴀɢᴏɴ 845 』"..whs845,
"🔵 『 sɴᴀᴘᴅʀᴀɢᴏɴ 855 』"..whs855,
"🔴 『 sɴᴀᴘᴅʀᴀɢᴏɴ 865 』"..whs865,
"⚫ 『 sɴᴀᴘᴅʀᴀɢᴏɴ ᴀʟʟ ᴅᴇᴠɪᴄᴇs 』"..whsall,
"🛠️ 『 ғɪx ʙʟɪɴᴋ 430-835 』",
"🛠️ 『 ғɪx ʙʟɪɴᴋ 845-855 』",
"⬅️ 『 ʙ ᴀ ᴄ ᴋ 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if WHMN2 == nil then else
if WHMN2 == 1 then WH425() end
if WHMN2 == 2 then WH430() end
if WHMN2 == 3 then WH625() end
if WHMN2 == 4 then WH6252() end
if WHMN2 == 5 then WH636() end
if WHMN2 == 6 then WH660() end
if WHMN2 == 7 then WH665() end
if WHMN2 == 8 then WH675() end
if WHMN2 == 9 then WH6752() end
if WHMN2 == 10 then WH710() end
if WHMN2 == 11 then WH730() end
if WHMN2 == 12 then WH810() end
if WHMN2 == 13 then WH820() end
if WHMN2 == 14 then WH835() end
if WHMN2 == 15 then WH845() end
if WHMN2 == 16 then WH855() end
if WHMN2 == 17 then WH865() end
if WHMN2 == 18 then ALLD() end
if WHMN2 == 19 then FIXWH() end
if WHMN2 == 20 then FIXWH2() end
if WHMN2 == 21 then BDY2() end
end
PUBGMH = -1
end

function WH865()
if whs865 == off then
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("1.12020508e-19;3.76158192e-37;2.0;0.24022650719;0.69314718246::", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
wh865s1 = gg.getResults(100)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("1.25414346e-19;1.7506772e-39;2.0;1.8425141e-39;1.74488844e-39::\n", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
wh865s2 = gg.getResults(100)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("95D;2", gg.TYPE_FLOAT)
gg.searchNumber("2", gg.TYPE_FLOAT)
gg.refineAddress("9B0", gg.TYPE_FLOAT)
wh865s3 = gg.getResults(69696969)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("2.25000452995;2", gg.TYPE_FLOAT)
gg.searchNumber("2", gg.TYPE_FLOAT)
gg.refineAddress("6D0", gg.TYPE_FLOAT)
wh865s4 = gg.getResults(69696969)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 865] Activated")
CLR865()
whs865 = on
else
gg.clearResults()
gg.setValues(wh865s1)
gg.setValues(wh865s2)
gg.setValues(wh865s3)
gg.setValues(wh865s4)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 865] Deactivated")
whs865 = off
end
end

function WH665()
if whs665 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("2.0F;1.66231134e-19F;0.0F;9.21942286e-41F;7.23035964e-15F;2.37549734116F;4.40284136e-29F;2.25000905991F;3.58159416e-39F;1.66433004e10F::37", 16, false, 536870912, 0, -1)
gg.searchNumber("2", 16, false, 536870912, 0, -1)
gg.refineAddress("200")
wh665s1 = gg.getResults(25)
gg.editAll("120", 16)
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("2.0F;-1.0F;0.0F;1.0F;-127.0F;0.24022650719F;0.69314718246F;0.00999999978F;-0.0F;0.0F::37", 16, false, 536870912, 0, -1)
gg.searchNumber("2", 16, false, 536870912, 0, -1)
gg.refineAddress("930")
wh665s2 = gg.getResults(25)
gg.editAll("120", 16)
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("2", 16, false, 536870912, 0, -1)
gg.refineAddress("A8C")
wh665s3 = gg.getResults(25)
gg.editAll("120", 16)
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("2", 16, false, 536870912, 0, -1)
gg.refineAddress("B10")
wh665s4 = gg.getResults(25)
gg.editAll("120", 16)
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("2", 16, false, 536870912, 0, -1)
gg.refineAddress("588")
wh665s5 = gg.getResults(25)
gg.editAll("999", 16)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 665] Activated")
CLR()
whs665 = on
else
gg.clearResults()
gg.setValues(wh665s1)
gg.setValues(wh665s2)
gg.setValues(wh665s3)
gg.setValues(wh665s4)
gg.setValues(wh665s5)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 665] Deactivated")
whs665 = off
end
end

function FIXWH()
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("5.2806111e-40;6.50000333786;3.7615819e-37;2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(20)
gg.editAll("9999", gg.TYPE_FLOAT)
gg.setRanges(gg.REGION_BAD)
gg.searchNumber("1.1202011e-19;1.1202015e-19;3.7615819e-37;255.0;2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(20)
gg.editAll("9999", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("🛠️ Fix Blink 430-835 🛠️")
end

function FIXWH2()
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("5.2806111e-40;6.50000333786;3.7615819e-37;2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(20)
gg.editAll("9999", gg.TYPE_FLOAT)
gg.setRanges(gg.REGION_BAD)
gg.searchNumber("1.1202011e-19;1.1202015e-19;3.7615819e-37;255.0;2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(20)
gg.editAll("9999", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("🛠️ Fix Blink 845-855 🛠️")
end

function FIXSCOPE()
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("2.718519e-43F;3.7615819e-37F;2.0F;-1.0F;1.0F;-127.0F;0.00999999978F::200", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber(2, gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(3)
gg.editAll("2.001", gg.TYPE_FLOAT)
gg.searchNumber(2, gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(10)
gg.editAll("120", gg.TYPE_FLOAT)
gg.setRanges(gg.REGION_BAD)
gg.searchNumber("5.8013756e-42F;-5.5695588e-40F;2.0F::100", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(3)
gg.editAll("2.001", gg.TYPE_FLOAT)
gg.searchNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(10)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("🛠️ Fix Scope 🛠️")
end

function WH425()
if whs425 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("2.9427268e-44;2.0;3.0828566e-44;-1.0;3.2229865e-44;3.3631163e-44;3.643376e-44:97", 16, false, 536870912, 0, -1)
gg.searchNumber("2", 16, false, 536870912, 0, -1)
whs425s1 = gg.getResults(100)
gg.editAll("120", 16)
gg.clearResults()
gg.searchNumber("3.1529215e-43;2.0F;3.1669345e-43F;3.1809475e-43:49", 16, false, 536870912, 0, -1)
gg.searchNumber("2", 16, false, 536870912, 0, -1)
whs425s2 = gg.getResults(100)
gg.editAll("120", 16)
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("227;1,073,741,824;1,073,741,824;-1,082,130,432;1,073,741,824:49", 4, false, 536870912, 0, -1)
gg.searchNumber("1,073,741,824", 4, false, 536870912, 0, -1)
whs425s3 = gg.getResults(100)
gg.editAll("1,123,024,896", 4)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 425] Activated")
CLR425()
whs425 = on
else
gg.clearResults()
gg.setValues(whs425s1)
gg.setValues(whs425s2)
gg.setValues(whs425s3)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 425] Deactivated")
whs425 = off
end
end

function WH430()
if whs430 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("2;1.8947657e-40;5.8013756e-42", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs430s1 = gg.getResults(999)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.searchNumber("2.718519e-43;3.7615819e-37;2;-1;1;-127", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs430s2 = gg.getResults(999)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 430] Activated")
CLR()
whs430 = on
else
gg.clearResults()
gg.setValues(whs430s1)
gg.setValues(whs430s2)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 430] Deactivated")
whs430 = off
end
end

function WH625()
if whs625 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("135,215D;4,140D;3.7615819e-37;2::", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs625s1 = gg.getResults(10)
gg.editAll("130", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("194D;3.7615819e-37;2;-1;1;-127::", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs625s2 = gg.getResults(10)
gg.editAll("130", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 625] Activated")
CLR()
whs625 = on
else
gg.clearResults()
gg.setValues(whs625s1)
gg.setValues(whs625s2)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 625] Deactivated")
whs625 = off
end
end

function WH6252()
if whs6752 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("5.79227989e21;-5.56955884e-40;2.0;1.39125666e-19;2.0:9285", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs6752s1 = gg.getResults(50)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 625] Activated")
CLR()
whs6752 = on
else
gg.clearResults()
gg.setValues(whs6752s1)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 625] Deactivated")
whs6752 = off
end
end

function WH636()
if whs636 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("-2 147 086 191", gg.TYPE_DWORD,false, gg.SIGN_EQUAL, 0, -1)
gg.refineAddress("4C8", -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
whs636s1 = gg.getResults(1337)
gg.editAll("1168777216", gg.TYPE_DWORD)
gg.clearResults()
gg.searchNumber("-2145644352", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineAddress("7E0", -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
whs636s2 = gg.getResults(1337)
gg.editAll("1168777216", gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.searchNumber("7,41529732e-29", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
whs636s3 = gg.getResults(1337)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 636] Activated")
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("8,192D;256D;8200D", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("8200", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
whs636s4 = gg.getResults(20)
gg.editAll("6", gg.TYPE_DWORD)
gg.toast("Body Color [SnapDragon 636] Activated")
gg.clearResults()
whs636 = on
else
gg.clearResults()
gg.setValues(whs636s1)
gg.setValues(whs636s2)
gg.setValues(whs636s3)
gg.setValues(whs636s4)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 636] Deactivated")
whs636 = off
end
end

function WH660()
if whs660 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
gg.searchNumber("1.8948778e-40;4.7408166e21;2.0:93", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.processResume()
gg.refineNumber("2.0", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineAddress("504", -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
whs660s1 = gg.getResults(63825)
gg.editAll("130", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO | gg.REGION_BAD)
gg.searchNumber("3.37670946121;3.37548875809;2.0:149", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2.0", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.processResume()
gg.refineAddress("980", -1, gg.TYPE_FLOAT, gg.SIGN_EQUAL, 0, -1)
whs660s2 = gg.getResults(63825)
gg.editAll("130", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 660] Activated")
CLR()
whs660 = on
else
gg.clearResults()
gg.setValues(whs660s1)
gg.setValues(whs660s2)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 660] Deactivated")
whs660 = off
end
end

function WH675()
if whs675 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("274,677,779D;2.25000452995;2;1.6623054e-19", 16, false, 536870912, 0, -1)
gg.searchNumber("2", 16, false, 536870912, 0, -1)
whs675s1 = gg.getResults(20)
gg.editAll("130", 16)
gg.toast("25%")
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("218D;3.7615819e-37;2;-1;1", 16, false, 536870912, 0, -1)
gg.searchNumber("2", 16, false, 536870912, 0, -1)
whs675s2 = gg.getResults(10)
gg.editAll("130", 16)
gg.toast("50%")
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("95D;2;9.2194229e-41", 16, false, 536870912, 0, -1)
gg.searchNumber("2", 16, false, 536870912, 0, -1)
whs675s3 = gg.getResults(15)
gg.editAll("130", 16)
gg.toast("75%")
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("206D;3.7615819e-37;2;-1;1", 16, false, 536870912, 0, -1)
gg.searchNumber("2", 16, false, 536870912, 0, -1)
whs675s4 = gg.getResults(10)
gg.editAll("130", 16)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 675] Activated")
CLR675()
whs675 = on
else
gg.clearResults()
gg.setValues(whs675s1)
gg.setValues(whs675s2)
gg.setValues(whs675s3)
gg.setValues(whs675s4)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 675] Deactivated")
whs675 = off
end
end

function WH6752()
if whs6752 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("8.2676609e-44;1.3912565e-19f;2.0", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("8.2676609e-44;1.3912565e-19f;2.0", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs6752s1 = gg.getResults(6000)
gg.editAll("120", gg.TYPE_FLOAT)
gg.searchNumber("3.7615819e-37;1.1202056e-19;2.0", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("3.7615819e-37;1.1202056e-19;2.0", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.processResume()
whs6752s2 = gg.getResults(6000)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 675] Activated")
CLR675()
whs6752 = on
else
gg.clearResults()
gg.setValues(whs6752s1)
gg.setValues(whs6752s2)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 675] Deactivated")
whs6752 = off
end
end

function WH710()
if whs710 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("2;1.8947657e-40;5.8013756e-42", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs710s1 = gg.getResults(10)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.searchNumber("2.718519e-43;3.7615819e-37;2;-1;1;-127", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs710s2 = gg.getResults(10)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 710] Activated")
CLR()
whs710 = on
else
gg.clearResults()
gg.setValues(whs710s1)
gg.setValues(whs710s2)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 710] Deactivated")
whs710 = off
end
end

function WH810()
if whs810 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("2;1.8947657e-40;5.8013756e-42", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs810s1 = gg.getResults(10)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.searchNumber("2.718519e-43;3.7615819e-37;2;-1;1;-127", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs810s2 = gg.getResults(10)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 810] Activated")
gg.clearResults()
CLR()
whs810 = on
else
gg.clearResults()
gg.setValues(whs810s1)
gg.setValues(whs810s2)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 810] Deactivated")
whs810 = off
end
end

function WH820()
if whs820 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("2;1.8947657e-40;5.8013756e-42", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs820s1 = gg.getResults(10)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.searchNumber("2.718519e-43;3.7615819e-37;2;-1;1;-127", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs820s2 = gg.getResults(10)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 820] Activated")
gg.clearResults()
CLR()
whs820 = on
else
gg.clearResults()
gg.setValues(whs820s1)
gg.setValues(whs820s2)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 820] Deactivated")
whs820 = off
end
end

function WH835()
if whs835 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("2;1.8947657e-40;5.8013756e-42", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs835s1 = gg.getResults(10)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.searchNumber("2.718519e-43;3.7615819e-37;2;-1;1;-127", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs835s2 = gg.getResults(10)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 835] Activated")
gg.clearResults()
CLR()
whs835 = on
else
gg.clearResults()
gg.setValues(whs835s1)
gg.setValues(whs835s2)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 835] Deactivated")
whs835 = off
end
end

function WH845()
if whs845 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber('95D;2', gg.TYPE_FLOAT)
gg.searchNumber('2', gg.TYPE_FLOAT)
gg.refineAddress('9B0', gg.TYPE_FLOAT)
whs845s1 = gg.getResults(69696969)
gg.editAll('120', gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("5.1097599e21;8.2676609e-44;2.0:13", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs845s2 = gg.getResults(100)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 845] Activated")
CLR845()
whs845 = on
else
gg.clearResults()
gg.setValues(whs845s1)
gg.setValues(whs845s2)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 845] Deactivated")
whs845 = off
end
end

function WH855()
if whs855 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber('95D;2', gg.TYPE_FLOAT)
gg.searchNumber('2', gg.TYPE_FLOAT)
gg.refineAddress('9B0', gg.TYPE_FLOAT)
whs855s1 = gg.getResults(69696969)
gg.editAll('120', gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("5.1097599e21;8.2676609e-44;2.0:13", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs855s2 = gg.getResults(100)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 855] Activated")
CLR855()
whs855 = on
else
gg.clearResults()
gg.setValues(whs855s1)
gg.setValues(whs855s2)
gg.clearResults()
gg.toast("WALLHACK [SnapDragon 855] Deactivated")
whs855 = off
end
end

function WH730()
if whs730 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber('95D;2', gg.TYPE_FLOAT)
gg.searchNumber('2', gg.TYPE_FLOAT)
gg.refineAddress('9B0', gg.TYPE_FLOAT)
whs730s1 = gg.getResults(69696969)
gg.editAll('120', gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("5.1097599e21;8.2676609e-44;2.0:13", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
whs730s2 = gg.getResults(100)
gg.editAll("120", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("8200;1194344450;8201;1194379829", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("8201", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
whs730s3 = gg.getResults(100)
gg.editAll("6", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("ᴡᴀʟʟʜᴀᴄᴋ + ♎ ɢʀᴇᴇɴ ʙᴏᴅʏ Activated")
whs730 = on
else
gg.clearResults()
gg.setValues(whs730s1)
gg.setValues(whs730s2)
gg.setValues(whs730s3)
gg.clearResults()
gg.toast("ᴡᴀʟʟʜᴀᴄᴋ + ♎ ɢʀᴇᴇɴ ʙᴏᴅʏ Deactivated")
whs730 = off
end
end

function ALLD()
if whsall == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("-2 147 086 191", gg.TYPE_DWORD,false, gg.SIGN_EQUAL, 0, -1)
gg.refineAddress("4C8", -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
whsalls1 = gg.getResults(1337)
gg.editAll("1168777216", gg.TYPE_DWORD)
gg.clearResults()
gg.searchNumber("-2145644352", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineAddress("7E0", -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
whsalls2 = gg.getResults(1337)
gg.editAll("1168777216", gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.searchNumber("7,41529732e-29", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
whsalls3 = gg.getResults(1337)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("WALLHACK [All Devices] Activated")
CLR()
whsall = on
else
gg.clearResults()
gg.setValues(whsalls1)
gg.setValues(whsalls2)
gg.setValues(whsalls3)
gg.clearResults()
gg.toast("WALLHACK [All Devices] Deactivated")
whsall = off
end
end

-- -- -- -- -- -- -- -- -- --  Color Menu  SD 425 -- -- -- -- -- -- -- -- --

function CLR425()
CLRMN425 = gg.choice({
"🔴 『 لون أحمر  425 』",
"☣️ 『 لون أصفر  425 』",
"➡️ 『 رجوع 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if CLRMN425 == nil then else
if CLRMN425 == 1 then RED425() end
if CLRMN425 == 2 then YELL425() end
if CLRMN425 == 3 then CLR() end
end
PUBGMH = -1
end

function CLR4252()
CLRMN4252 = gg.choice({
"🔴 『 ʀᴇᴅ ʙᴏᴅʏ 425 』",
"☣️ 『 ʏᴇʟʟᴏᴡ ʙᴏᴅʏ 425 』",
"⬅️ 『 ʙ ᴀ ᴄ ᴋ 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if CLRMN4252 == nil then else
if CLRMN4252 == 1 then RED425() end
if CLRMN4252 == 2 then YELL425() end
if CLRMN4252 == 3 then CLR2() end
end
PUBGMH = -1
end

function RED425()
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber('"8204"', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.processResume()
gg.refineAddress('"408"', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
revert = gg.getResults(10, nil, nil, nil, nil, nil, nil, nil, nil)
gg.editAll('"96"', gg.TYPE_DWORD)
local t = gg.getResults(10, nil, nil, nil, nil, nil, nil, nil, nil)
gg.addListItems(t)
t = nil
gg.clearResults()
gg.toast("Red Body Activated")
end

function YELL425()
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber('"8204"', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.processResume()
gg.refineAddress('"408"', -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
revert = gg.getResults(10, nil, nil, nil, nil, nil, nil, nil, nil)
gg.editAll('"95"', gg.TYPE_DWORD)
local t = gg.getResults(10, nil, nil, nil, nil, nil, nil, nil, nil)
gg.addListItems(t)
t = nil
gg.clearResults()
gg.toast("Yellow Body Activated")
end

-- -- -- -- -- -- -- -- -- --  Color Menu  SD 675 -- -- -- -- -- -- -- -- --

clrwhite675 = off
clrblue675 = off
clrgreen675 = off

function CLR675()
CLRMN675 = gg.choice({
"🔴 『 لون أحمر  675 』"..clrwhite675,
"🔵 『 لون أزرق  675 』"..clrblue675,
"♎ 『 لون أخضر  675 』"..clrgreen675,
"⁦➡️⁩ 『 رجوع 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if CLRMN675 == nil then else
if CLRMN675 == 1 then WHITE675() end
if CLRMN675 == 2 then BLUE675() end
if CLRMN675 == 3 then GREEN675() end
if CLRMN675 == 4 then CLR() end
end
PUBGMH = -1
end

function CLR6752()
CLRMN6752 = gg.choice({
"🔴 『 ʀᴇᴅ ʙᴏᴅʏ 675 』"..clrwhite675,
"🔵 『 ʙʟᴜᴇ ʙᴏᴅʏ 675 』"..clrblue675,
"♎ 『 ɢʀᴇᴇɴ ʙᴏᴅʏ 675 』"..clrgreen675,
"⬅️ 『 ʙ ᴀ ᴄ ᴋ 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if CLRMN6752 == nil then else
if CLRMN6752 == 1 then WHITE675() end
if CLRMN6752 == 2 then BLUE675() end
if CLRMN6752 == 3 then GREEN675() end
if CLRMN6752 == 4 then CLR2() end
end
PUBGMH = -1
end

function GREEN675()
if clrgreen675 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("69,897;147,457;69,739", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
clrgreen675s1 = gg.getResults(10)
gg.editAll("7", gg.TYPE_DWORD)
gg.toast("Color 675 Green")
gg.clearResults()
clrgreen675 = on
else
gg.clearResults()
gg.setValues(clrgreen675s1)
gg.clearResults()
gg.toast("Color 675 Green Deactivated")
clrgreen675 = off
end
end

function WHITE675()
if clrwhite675 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("537137162;8200;1194344459:9", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("8200", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
clrwhite675s1 = gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil)
gg.editAll("7", gg.TYPE_DWORD)
gg.clearResults()
gg.toast('Red Body Activated')
clrwhite675 = on
else
gg.clearResults()
gg.setValues(clrwhite675s1)
gg.clearResults()
gg.toast("Red Body Deactivated")
clrwhite675 = off
end
end

function BLUE675()
if clrblue675 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("537137162;8200;1194344459;1194344485;8202;1194379568:25", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("8202", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
clrblue675s1 = gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil)
gg.editAll("7", gg.TYPE_DWORD)
gg.clearResults()
gg.toast('Blue Body Activated')
clrblue675 = on
else
gg.clearResults()
gg.setValues(clrblue675s1)
gg.clearResults()
gg.toast("Blue Body Deactivated")
clrblue675 = off
end
end

-- -- -- -- -- -- -- -- -- --  Color Menu  SD 845 -- -- -- -- -- -- -- -- --

clrred845 = off
clryellow845 = off
clrgreen845 = off
clrblue845 = off

function CLR845()
CLRMN845 = gg.choice({
"🔴 『 لون أحمر  845 』"..clrred845,
"☣️ 『 لون أصفر  845 』"..clryellow845,
"♎ 『 لون أخضر  845 』"..clrgreen845,
"🔵 『 لون أزرق  845 』"..clrblue845,
"⁦➡️⁩ 『 رجوع 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if CLRMN845 == nil then else
if CLRMN845 == 1 then RED845() end
if CLRMN845 == 2 then YELL845() end
if CLRMN845 == 3 then GREEN845() end
if CLRMN845 == 4 then BLUE845() end
if CLRMN845 == 5 then CLR() end
end
PUBGMH = -1
end

function CLR8452()
CLRMN8452 = gg.choice({
"🔴 『 ʀᴇᴅ ʙᴏᴅʏ 845 』"..clrred845,
"☣️ 『 ʏᴇʟʟᴏᴡ ʙᴏᴅʏ 845 』"..clryellow845,
"♎ 『 ɢʀᴇᴇɴ ʙᴏᴅʏ 845 』"..clrgreen845,
"🔵 『 ʙʟᴜᴇ ʙᴏᴅʏ 845 』"..clrblue845,
"⬅️ 『 ʙ ᴀ ᴄ ᴋ 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if CLRMN8452 == nil then else
if CLRMN8452 == 1 then RED845() end
if CLRMN8452 == 2 then YELL845() end
if CLRMN8452 == 3 then GREEN845() end
if CLRMN8452 == 4 then BLUE845() end
if CLRMN8452 == 5 then CLR2() end
end
PUBGMH = -1
end

function YELL845()
if clryellow845 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("8200;1194344459;8201;1194346792", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("8200;8201", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
clryellow845s1 = gg.getResults(100)
gg.editAll("7", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("Yellow Body Activated")
clryellow845 = on
else
gg.clearResults()
gg.setValues(clryellow845s1)
gg.clearResults()
gg.toast("Yellow Body Deactivated")
clryellow845 = off
end
end

function RED845()
if clrred845 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("8200;1194344459;8201;1194346792", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("8200", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
clrred845s1 = gg.getResults(100)
gg.editAll("8199", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("Red Color Activated")
clrred845 = on
else
gg.clearResults()
gg.setValues(clrred845s1)
gg.clearResults()
gg.toast("Red Color Deactivated")
clrred845 = off
end
end

function GREEN845()
if clrgreen845 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("8200;1194344459;8201;1194346792", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("8201", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
clrgreen845s1 = gg.getResults(100)
gg.editAll("7", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("Green Body Activated")
clrgreen845 = on
else
gg.clearResults()
gg.setValues(clrgreen845s1)
gg.clearResults()
gg.toast("Green Body Deactivated")
clrgreen845 = off
end
end

function BLUE845()
if clrblue845 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("8200;1194344459;8201;1194346792", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("8201", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
clrblue845s1 = gg.getResults(100)
gg.editAll("6", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("Blue Body Activated")
clrblue845 = on
else
gg.clearResults()
gg.setValues(clrblue845s1)
gg.clearResults()
gg.toast("Blue Body Deactivated")
clrblue845 = off
end
end

-- -- -- -- -- -- -- -- -- --  Color Menu  SD 855 -- -- -- -- -- -- -- -- --

function CLR855()
CLRMN855 = gg.choice({
"♎ 『 لون أخضر  855 』"..clrgreen845,
"☣️ 『 لون أصفر  855 』"..clryellow845,
"🔵 『 لون أزرق  855 』"..clrblue845,
"🔴 『 لون أحمر  855 』"..clrred845,
"⁦➡️⁩ 『 رجوع 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if CLRMN855 == nil then else
if CLRMN855 == 1 then GREEN845() end
if CLRMN855 == 2 then YELL845() end
if CLRMN855 == 3 then BLUE845() end
if CLRMN855 == 4 then RED845() end
if CLRMN855 == 5 then CLR() end
end
PUBGMH = -1
end

function CLR8552()
CLRMN8552 = gg.choice({
"♎ 『 ɢʀᴇᴇɴ ʙᴏᴅʏ 855 』"..clrgreen845,
"☣️ 『 ʏᴇʟʟᴏᴡ ʙᴏᴅʏ 855 』"..clryellow845,
"🔵 『 ʙʟᴜᴇ ʙᴏᴅʏ 855 』"..clrblue845,
"🔴 『 ʀᴇᴅ ʙᴏᴅʏ 855 』"..clrred845,
"⬅️ 『 ʙ ᴀ ᴄ ᴋ 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if CLRMN8552 == nil then else
if CLRMN8552 == 1 then GREEN845() end
if CLRMN8552 == 2 then YELL845() end
if CLRMN8552 == 3 then BLUE845() end
if CLRMN8552 == 4 then RED845() end
if CLRMN8552 == 5 then CLR2() end
end
PUBGMH = -1
end

-- -- -- -- -- -- -- -- -- --  Color Menu  SD 865 -- -- -- -- -- -- -- -- --

clryellow865 = off
clrgreen865 = off
clrpink865 = off
clrorange865 = off

function CLR865()
CLRMN865 = gg.choice({
"☣️ 『 لون أصفر  865 』"..clryellow865,
"♎ 『 لون أخضر  865 』"..clrgreen865,
"🧶 『 لون وردي 865 』"..clrpink865,
"🍊 『 لون برتقالي 865 』"..clrorange865,
"⁦➡️⁩ 『 رجوع 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if CLRMN865 == nil then else
if CLRMN865 == 1 then YELL865() end
if CLRMN865 == 2 then GREEN865() end
if CLRMN865 == 3 then PINK865() end
if CLRMN865 == 4 then ORANGE865() end
if CLRMN865 == 5 then CLR() end
end
PUBGMH = -1
end

function CLR8652()
CLRMN8652 = gg.choice({
"☣️ 『 ʏᴇʟʟᴏᴡ ʙᴏᴅʏ 865 』"..clryellow865,
"♎ 『 ɢʀᴇᴇɴ ʙᴏᴅʏ 865 』"..clrgreen865,
"🧶 『 ᴘɪɴᴋ ʙᴏᴅʏ 865 』"..clrpink865,
"🍊 『 ᴏʀᴀɴɢᴇ ʙᴏᴅʏ 865 』"..clrorange865,
"⬅️ 『 ʙ ᴀ ᴄ ᴋ 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if CLRMN8652 == nil then else
if CLRMN8652 == 1 then YELL865() end
if CLRMN8652 == 2 then GREEN865() end
if CLRMN8652 == 3 then PINK865() end
if CLRMN8652 == 4 then ORANGE865() end
if CLRMN8652 == 5 then CLR2() end
end
PUBGMH = -1
end

function YELL865()
if clryellow865 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("8196;1194346786;8200;1194380068", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("8200", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
clryellow865s1 = gg.getResults(100)
gg.editAll("8198", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("☣️ ʏᴇʟʟᴏᴡ ʙᴏᴅʏ 865 Activated")
clryellow865 = on
else
gg.clearResults()
gg.setValues(clryellow865s1)
gg.clearResults()
gg.toast("☣️ ʏᴇʟʟᴏᴡ ʙᴏᴅʏ 865 Deactivated")
clryellow865 = off
end
end

function GREEN865()
if clrgreen865 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("8196;1194346786;8200;1194380068", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("8200", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
clrgreen865s1 = gg.getResults(100)
gg.editAll("56", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("♎ ɢʀᴇᴇɴ ʙᴏᴅʏ 865 Activated")
clrgreen865 = on
else
gg.clearResults()
gg.setValues(clrgreen865s1)
gg.clearResults()
gg.toast("♎ ɢʀᴇᴇɴ ʙᴏᴅʏ 865 Deactivated")
clrgreen865 = off
end
end

function PINK865()
if clrpink865 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("8196;1194346786;8200;1194380068", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("8200", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
clrpink865s1 = gg.getResults(100)
gg.editAll("55", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("🧶 ᴘɪɴᴋ ʙᴏᴅʏ 865 Activated")
clrpink865 = on
else
gg.clearResults()
gg.setValues(clrpink865s1)
gg.clearResults()
gg.toast("🧶 ᴘɪɴᴋ ʙᴏᴅʏ 865 Deactivated")
clrpink865 = off
end
end

function ORANGE865()
if clrorange865 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("8196;1194346786;8200;1194380068", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("8200", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
clrorange865s1 = gg.getResults(100)
gg.editAll("31", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("🍊 ᴏʀᴀɴɢᴇ ʙᴏᴅʏ 865 Activated")
clrorange865 = on
else
gg.clearResults()
gg.setValues(clrorange865s1)
gg.clearResults()
gg.toast("🍊 ᴏʀᴀɴɢᴇ ʙᴏᴅʏ 865 Deactivated")
clrorange865 = off
end
end

-- -- -- -- -- -- -- -- -- -- --   All Colors   -- -- -- -- -- -- -- -- -- -- --

clrred625 = off
clryellow625 = off
clrred660 = off
clryellow660 = off
clrred835 = off
clryellow835 = off
clrwhiteall = off
clrblackall = off

function CLR()
CLRMN = gg.choice({
"📂 『 قائمة ألوان SD425 』",
"📂 『 قائمة ألوان SD675 』",
"📂 『 قائمة ألوان SD845 』",
"📂 『 قائمة ألوان SD855 』",
"📂 『 قائمة ألوان SD865 』",
"🔴 『 لون أحمر  625 』"..clrred625,
"☣️ 『 لون أصفر  625 』"..clryellow625,
"🔴 『 لون أحمر  660 』"..clrred660,
"☣️ 『 لون أصفر  660 』"..clryellow660,
"🔴 『 لون أحمر  835 』"..clrred835,
"☣️ 『 لون أصفر  835 』"..clryellow835,
"⚪ 『 لون أبيض لجميع الأجهزة 』"..clrwhiteall,
"⚫ 『 لون أسود لجميع الأجهزة 』",
"⁦➡️⁩ 『 رجوع 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if CLRMN == nil then else
if CLRMN == 1 then CLR425() end
if CLRMN == 2 then CLR675() end
if CLRMN == 3 then CLR845() end
if CLRMN == 4 then CLR855() end
if CLRMN == 5 then CLR865() end
if CLRMN == 6 then RED625() end
if CLRMN == 7 then YELL625() end
if CLRMN == 8 then RED660C() end
if CLRMN == 9 then YELL660() end
if CLRMN == 10 then RED835() end
if CLRMN == 11 then YELL835() end
if CLRMN == 12 then WHITEALL() end
if CLRMN == 13 then BLACKALL() end
if CLRMN == 14 then BDY() end
end
PUBGMH = -1
end

function CLR2()
CLRMN2 = gg.choice({
"📂 『 SD425 ᴄᴏʟᴏʀ ᴍᴇɴᴜ 』",
"📂 『 SD675 ᴄᴏʟᴏʀ ᴍᴇɴᴜ 』",
"📂 『 SD845 ᴄᴏʟᴏʀ ᴍᴇɴᴜ 』",
"📂 『 SD855 ᴄᴏʟᴏʀ ᴍᴇɴᴜ 』",
"📂 『 SD865 ᴄᴏʟᴏʀ ᴍᴇɴᴜ 』",
"🔴 『 ʀᴇᴅ ʙᴏᴅʏ 625 』"..clrred625,
"☣️ 『 ʏᴇʟʟᴏᴡ ʙᴏᴅʏ 625 』"..clryellow625,
"🔴 『 ʀᴇᴅ ʙᴏᴅʏ 660 』"..clrred660,
"☣️ 『 ʏᴇʟʟᴏᴡ ʙᴏᴅʏ 660 』"..clryellow660,
"🔴 『 ʀᴇᴅ ʙᴏᴅʏ 835 』"..clrred835,
"☣️ 『 ʏᴇʟʟᴏᴡ ʙᴏᴅʏ 835 』"..clryellow835,
"⚪ 『 ᴡʜɪᴛᴇ ʙᴏᴅʏ ᴀʟʟ 』"..clrwhiteall,
"⚫ 『 ʙʟᴀᴄᴋ ʙᴏᴅʏ ᴀʟʟ 』",
"⬅️ 『 ʙ ᴀ ᴄ ᴋ 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if CLRMN2 == nil then else
if CLRMN2 == 1 then CLR4252() end
if CLRMN2 == 2 then CLR6752() end
if CLRMN2 == 3 then CLR8452() end
if CLRMN2 == 4 then CLR8552() end
if CLRMN2 == 5 then CLR8652() end
if CLRMN2 == 6 then RED625() end
if CLRMN2 == 7 then YELL625() end
if CLRMN2 == 8 then RED660C() end
if CLRMN2 == 9 then YELL660() end
if CLRMN2 == 10 then RED835() end
if CLRMN2 == 11 then YELL835() end
if CLRMN2 == 12 then WHITEALL() end
if CLRMN2 == 13 then BLACKALL() end
if CLRMN2 == 14 then BDY2() end
end
PUBGMH = -1
end

function RED660C()
if clrred660 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("8,196D;8,192D;8,200D::", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("8200", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
clrred660s1 = gg.getResults(10)
gg.editAll("7", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("Red Body Activated")
clrred660 = on
else
gg.clearResults()
gg.setValues(clrred660s1)
gg.clearResults()
gg.toast("Red Body Deactivated")
clrred660 = off
end
end

function RED625()
if clrred625 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("8,196D;8,192D;8,200D::", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("8200", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
clrred625s1 = gg.getResults(10)
gg.editAll("7", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("Red Body Activated")
clrred625 = on
else
gg.clearResults()
gg.setValues(clrred625s1)
gg.clearResults()
gg.toast("Red Body Deactivated")
clrred625 = off
end
end

function YELL625()
if clryellow625 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber('1,080,033,292D;786,441D;8,200D:21::', gg.TYPE_DWORD,false, gg.SIGN_EQUAL,0,-1)
gg.searchNumber('8200', gg.TYPE_DWORD,false, gg.SIGN_EQUAL,0,-1)
clryellow625s1 = gg.getResults(10)
gg.editAll('8198', gg.TYPE_DWORD)
gg.clearResults()
gg.toast("Yellow Body Activated")
clryellow625 = on
else
gg.clearResults()
gg.setValues(clryellow625s1)
gg.clearResults()
gg.toast("Yellow Body Deactivated")
clryellow625 = off
end
end

function WHITEALL()
if clrwhiteall == off then
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("573.70306396484;0.05499718338;1::50", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("1", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
clrwhitealls1 = gg.getResults(1)
gg.editAll("999", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("White Body Activated")
clrwhiteall = on
else
gg.clearResults()
gg.setValues(clrwhitealls1)
gg.clearResults()
gg.toast("White Body Deactivated")
clrwhiteall = off
end
end

function BLACKALL() --1.2
gg.clearResults()
so=gg.getRangesList('libUE4.so')[1].start
py=0x2D96C18
setvalue(so+py,16,14)
gg.clearResults()
gg.toast("Black Body Activated")
end

function RED835()
if clrred835 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("8,196D;8,192D;8,200D::", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("8200", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
clrred835s1 = gg.getResults(10)
gg.editAll("7", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("🔴 ʀᴇᴅ ʙᴏᴅʏ 835 Activated")
clrred835 = on
else
gg.clearResults()
gg.setValues(clrred835s1)
gg.clearResults()
gg.toast("🔴 ʀᴇᴅ ʙᴏᴅʏ 835 Deactivated")
clrred835 = off
end
end

function YELL835()
if clryellow835 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber( "2;1.8947657e-40;5.8013756e-42", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber( "2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
clryellow835s1 = gg.getResults(999)
gg.editAll( "120", gg.TYPE_FLOAT)
gg.clearResults()
gg.searchNumber( "2.718519e-43;3.7615819e-37;2;-1;1;-127", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber( "2", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
clryellow835s2 = gg.getResults(999)
gg.editAll( "120", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber( "8200;96", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber( "8200", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineAddress( "098", -1, gg.TYPE_DWORD, gg.SIGN_EQUAL, 0, -1)
clryellow835s3 = gg.getResults(999)
gg.editAll( "8198", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("☣️ ʏᴇʟʟᴏᴡ ʙᴏᴅʏ 835 Activated")
clryellow835 = on
else
gg.clearResults()
gg.setValues(clryellow835s1)
gg.setValues(clryellow835s2)
gg.setValues(clryellow835s3)
gg.clearResults()
gg.toast("☣️ ʏᴇʟʟᴏᴡ ʙᴏᴅʏ 835 Deactivated")
clryellow835 = off
end
end

function YELL660()
if clryellow660 == off then
gg.clearResults()
gg.setRanges(gg.REGION_VIDEO or gg.REGION_BAD)
gg.searchNumber("536889616;8200;1194344458:9", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0) 
gg.refineNumber("8200", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0) 
clryellow660s1 = gg.getResults(2, nil, nil, nil, nil, nil, nil, nil, nil) 
gg.editAll("6", gg.TYPE_DWORD) 
gg.clearResults() 
gg.setRanges(gg.REGION_VIDEO) 
gg.searchNumber("1669398530;8200;1194380045:9", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0) 
gg.refineNumber("8200", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0) 
clryellow660s2 = gg.getResults(2, nil, nil, nil, nil, nil, nil, nil, nil) 
gg.editAll("6", gg.TYPE_DWORD) 
gg.clearResults() 
gg.toast("Yellow Body Activated")
clryellow660 = on
else
gg.clearResults()
gg.setValues(clryellow660s1)
gg.setValues(clryellow660s2)
gg.clearResults()
gg.toast("Yellow Body Deactivated")
clryellow660 = off
end
end

-- -- -- -- -- -- -- -- --   Weapons Menu   -- -- -- -- -- -- -- -- --

frontscoppp = off
sitscoppp = off
killx = off
standscoppp = off

function WEP1()
WEP1NMN = gg.choice({
"📂 『 الهيدشوت + الماجك بولت 』",
"📂 『 ثبات السلاح 』",
"💥 『 طلقة سريعة 』",
"💥 『 دمج عالي !! 』 ☠️",
"❌ 『 تأثير الضرب 🆇 』"..killx,
"💣 『 ايم بوت 』",
"🎯『 ايم لوك  』",
"⬆️ 『 فرونت سكوب 』 ☠️"..frontscoppp,
"🛐 『 سيت سكوب 』 ☠️"..sitscoppp,
"⬆️ 『 ستاند سكوب 』 ☠️"..standscoppp,
"📂 『 قائمة تكبير السكوب 』",
"⁦➡️⁩ 『 رجوع 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if WEP1NMN == nil then else
if WEP1NMN == 1 then HEADMN1() end
if WEP1NMN == 2 then NORECMN1() end
if WEP1NMN == 3 then INSTAHIT() end
if WEP1NMN == 4 then HIGHDAM() end
if WEP1NMN == 5 then KILLXON() end
if WEP1NMN == 6 then AIMBOT() end
if WEP1NMN == 7 then AIMLOCK() end
if WEP1NMN == 8 then FRONTSCOPEON() end
if WEP1NMN == 9 then SITSCOPEON() end
if WEP1NMN == 10 then STANDSCOPE() end
if WEP1NMN == 11 then SCOP1() end
if WEP1NMN == 12 then HOME1() end
end
PUBGMH = -1
end

function WEP2()
WEP2MN = gg.choice({
"📂 『 ʜᴇᴀᴅꜱʜᴏᴛ + ᴍᴀɢɪᴄ ʙᴜʟʟᴇᴛ 』",
"📂 『 ɴᴏ ʀᴇᴄᴏɪʟ 』",
"💥 『 ɪɴsᴛᴀɴᴛ ʜɪᴛ 』",
"💥 『 ʜɪɢʜ ᴅᴀᴍᴀɢᴇ !! 』 ☠️",
"❌ 『 ʜɪᴛ ᴇғғᴇᴄᴛ 🆇 』"..killx,
"💣 『 ᴀɪᴍʙᴏᴛ 』",
"🎯 『 ᴀɪᴍʟᴏᴄᴋ 』",
"⬆️ 『 ꜰʀᴏɴᴛ sᴄᴏᴘᴇ 』 ☠️"..frontscoppp,
"🛐 『 ꜱɪᴛ sᴄᴏᴘᴇ 』 ☠️"..sitscoppp,
"⬆️ 『 ꜱᴛᴀɴᴅ ꜱᴄᴏᴘᴇ 』 ☠️"..standscoppp,
"📂 『 ᴢᴏᴏᴍ sᴄᴏᴘᴇs ᴍᴇɴᴜ 』",
"⬅️ 『 ʙ ᴀ ᴄ ᴋ 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if WEP2MN == nil then else
if WEP2MN == 1 then HEADMN2() end
if WEP2MN == 2 then NORECMN2() end
if WEP2MN == 3 then INSTAHIT() end
if WEP2MN == 4 then HIGHDAM() end
if WEP2MN == 5 then KILLXON() end
if WEP2MN == 6 then AIMBOT() end
if WEP2MN == 7 then AIMLOCK() end
if WEP2MN == 8 then FRONTSCOPEON() end
if WEP2MN == 9 then SITSCOPEON() end
if WEP2MN == 10 then STANDSCOPE() end
if WEP2MN == 11 then SCOP2() end
if WEP2MN == 12 then HOME2() end
end
PUBGMH = -1
end

function INSTAHIT()
gg.clearResults()
gg.setRanges(gg.REGION_CODE_APP)
gg.searchNumber("-1,883,348,481,058,764,210", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("-1,883,348,481,058,764,210", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("-1,883,348,485,055,444,540", gg.TYPE_QWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
gg.searchNumber("-298284466;-1.304566e23F", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("-298284466", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(99)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("Instant Hit Activated!")
end

function HIGHDAM()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("16000~99999;3D;0.1;1D::40", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("16000~99999", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("500000", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber('0000B040rA;0000803FrA;0000403FrA:9', gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(3) 
gg.editAll('1,087,897,600;1,075,838,976;1,075,838,976', gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("88000;0.08600000292", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("88000", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(1401)
gg.editAll("400000", gg.TYPE_FLOAT)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("71500;0.10000000149", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("71500", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(1401)
gg.editAll("400000", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("87000;0.09600000083", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("87000", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(1401)
gg.editAll("400000", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("71500;0.109", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("71500", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(1401)
gg.editAll("400000", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("91500;0.07500000298", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("91500", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(1401)
gg.editAll("400000", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("High Damage activated!")
end

function STANDSCOPE()
if standscoppp == off then
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber('4138667321167981973', gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.sleep(140)
gg.refineNumber('4138667321167981973', gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.sleep(140)
gg.refineNumber('4138667321167981973', gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(1401)
gg.editAll('4848124999984742400', gg.TYPE_QWORD)
gg.clearResults()
gg.toast('Stand Scope activated!')
standscoppp = on
else
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber('4848124999984742400', gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.sleep(140)
gg.refineNumber('4848124999984742400', gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.sleep(140)
gg.refineNumber('4848124999984742400', gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(1401)
gg.editAll('4138667321167981973', gg.TYPE_QWORD)
gg.clearResults()
gg.toast("Stand Scope Deactivated")
standscoppp = off
end
end

function FRONTSCOPEON()
if frontscoppp == off then
gg.clearResults()
gg.setRanges(gg.REGION_C_BSS)
gg.searchNumber('3497450139768418399', gg.TYPE_QWORD)
frontscoppps1 = gg.getResults(69)
gg.editAll('9074961892185783746', gg.TYPE_QWORD)
gg.clearResults()
gg.toast('Stand Scope Front activated!')
frontscoppp = on
else
gg.clearResults()
gg.setValues(frontscoppps1)
gg.clearResults()
gg.toast("Stand Scope Front Deactivated")
frontscoppp = off
end
end

function SITSCOPEON()
if sitscoppp == off then
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("18.38787841797;0.53867292404;-3.42232513428;1.77635705e-15:13", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("18.38787841797", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
sitscoppps1 = gg.getResults(2805)
gg.editAll("130.5419921875", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast('Sit Scope activated!')
sitscoppp = on
else
gg.clearResults()
gg.setValues(sitscoppps1)
gg.clearResults()
gg.toast("Sit Scope Deactivated")
sitscoppp = off
end
end

function KILLXON()
if killx == off then
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("10;45", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("10", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("9999", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Hit Effect 🆇 Activated!")
killx = on
else
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("10;45", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("9999", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("10", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Hit Effect 🆇 Deactivated")
killx = off
end
end

function AIMBOT() --1.2
gg.clearResults()
so=gg.getRangesList('libUE4.so')[1].start
py=0x258B740
setvalue(so+py,4,0)
gg.clearResults()
gg.toast("Aimbot activated!")
end

function AIMLOCK() --1.2
gg.clearResults()
so=gg.getRangesList('libUE4.so')[1].start
py=0x258B74C
setvalue(so+py,4,0)
so=gg.getRangesList('libUE4.so')[1].start
py=0x258B880
setvalue(so+py,4,1152327680)
gg.clearResults()
gg.toast("Aimlock activated!")
end

-- -- -- -- -- -- -- -- --   Headshot Menu   -- -- -- -- -- -- -- -- --

function HEADMN1()
HEADMN1NMN = gg.choice({
"💥 『 هيدشوت %100 』 ☠️",
"💥 『 هيدشوت %95 』",
"💥 『 هيدشوت %75 』",
"💥 『 هيدشوت %50 』",
"☄️ 『 ماجك بوليت 』",
"🔥 『 ماجك بوليت v2 』",
"⁦➡️⁩ 『 رجوع 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if HEADMN1NMN == nil then else
if HEADMN1NMN == 1 then HSHOT100() end
if HEADMN1NMN == 2 then HSHOT95() end
if HEADMN1NMN == 3 then HSHOT75() end
if HEADMN1NMN == 4 then HSHOT50() end
if HEADMN1NMN == 5 then MAGICB() end
if HEADMN1NMN == 6 then MAGICB2() end
if HEADMN1NMN == 7 then WEP1() end
end
PUBGMH = -1
end

function HEADMN2()
HEADMN2NMN = gg.choice({
"💥 『 ʜᴇᴀᴅsʜᴏᴛ %100 』 ☠️",
"💥 『 ʜᴇᴀᴅsʜᴏᴛ %95 』",
"💥 『 ʜᴇᴀᴅsʜᴏᴛ %75 』",
"💥 『 ʜᴇᴀᴅsʜᴏᴛ %50 』",
"☄️ 『 ᴍᴀɢɪᴄ ʙᴜʟʟᴇᴛ 』",
"🔥 『 ᴍᴀɢɪᴄ ʙᴜʟʟᴇᴛ v2 』",
"⬅️ 『 ʙ ᴀ ᴄ ᴋ 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if HEADMN2NMN == nil then else
if HEADMN2NMN == 1 then HSHOT100() end
if HEADMN2NMN == 2 then HSHOT95() end
if HEADMN2NMN == 3 then HSHOT75() end
if HEADMN2NMN == 4 then HSHOT50() end
if HEADMN2NMN == 5 then MAGICB() end
if HEADMN2NMN == 6 then MAGICB2() end
if HEADMN2NMN == 7 then WEP2() end
end
PUBGMH = -1
end


function HSHOT100()
gg.clearResults()
gg.setVisible(false)
gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
gg.searchNumber("0.10000000149;64.50088500977", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("0.10000000149", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(50)
gg.editAll("8", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_BAD)
gg.searchNumber("-88.66608428955;26:512", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("26", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(2)
gg.editAll("-460", gg.TYPE_FLOAT)
gg.clearResults()
gg.searchNumber("-88.73961639404;28:512", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("28", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(2)
gg.editAll("-560", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("9.201618;30.5;25", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(10)
gg.editAll("250", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
gg.searchNumber("-1,883,348,481,058,764,210", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(99)
gg.editAll("-1,883,348,485,055,444,540", gg.TYPE_QWORD)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("9.201618;30.5;25", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("30.5;25", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("220", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("9.20161819458;23;25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("700", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("23;25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("23;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(2)
gg.editAll("699", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("25;23;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(3)
gg.editAll("180", gg.TYPE_FLOAT)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("9.201618;30.5;25", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(15)
gg.editAll("450", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Headshot 100% Activated")
end

function HSHOT95()
gg.clearResults()
gg.setVisible(false)
gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
gg.searchNumber("0.10000000149;64.50088500977", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("0.10000000149", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(50)
gg.editAll("8", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_BAD)
gg.searchNumber("-88.66608428955;26:512", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("26", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(2)
gg.editAll("-460", gg.TYPE_FLOAT)
gg.clearResults()
gg.searchNumber("-88.73961639404;28:512", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("28", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(2)
gg.editAll("-560", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("9.201618;30.5;25", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(10)
gg.editAll("250", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
gg.searchNumber("-1,883,348,481,058,764,210", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(99)
gg.editAll("-1,883,348,485,055,444,540", gg.TYPE_QWORD)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("9.201618;30.5;25", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("30.5;25", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("220", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("9.20161819458;23;25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("700", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("23;25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("23;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(2)
gg.editAll("699", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("25;23;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(3)
gg.editAll("180", gg.TYPE_FLOAT)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("9.201618;30.5;25", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(15)
gg.editAll("450", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Headshot 95% Activated")
end

function HSHOT75()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("-2.92050004005;-86.45761108398;-88.66608428955;16;26::17", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("26", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(2)
gg.editAll("-860", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("0.15122038126;90.48510742188;-88.73961639404;18;28::17", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("18;28::5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(2)
gg.editAll("-960", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("9.20161819458;23;25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(10)
gg.editAll("200", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Headshot 75% Activated")
end

function HSHOT50()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.setVisible(false)
gg.searchNumber("25;30.5", gg.TYPE_FLOAT)
gg.getResults(10)
gg.editAll("150", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("24;26;46.36692428589", gg.TYPE_FLOAT)
gg.refineNumber("24;26", gg.TYPE_FLOAT)
gg.refineNumber("24;26", gg.TYPE_FLOAT)
gg.getResults(50)
gg.editAll("-9999999", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Headshot 50% Activated")
end

function MAGICB()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("23;25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("200", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("15;28;16;26;8;18", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(56)
gg.editAll("-1339", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Magic Bullet Activated")
end

function MAGICB2()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("23;25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("250", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("15;28;16;26;8;18", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(56)
gg.editAll("-1339", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Magic Bullet Activated")
end

function SENIORKO()
gg.clearResults()
so=gg.getRangesList('libUE4.so')[1].start
py=0x136D4F8
setvalue(so+py,16,0)
so=gg.getRangesList('libUE4.so')[1].start
py=0x376E57C
setvalue(so+py,16,0)
so=gg.getRangesList('libUE4.so')[1].start
py=0x381CCE0
setvalue(so+py,16,0)
so=gg.getRangesList('libUE4.so')[1].start
py=0x1C113E8
setvalue(so+py,16,1.40129846e-45)
gg.clearResults()
gg.setVisible(false)
gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
gg.searchNumber("0.10000000149;64.50088500977", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("0.10000000149", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(50)
gg.editAll("8", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_BAD)
gg.searchNumber("-88.66608428955;26:512", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("26", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(2)
gg.editAll("-460", gg.TYPE_FLOAT)
gg.clearResults()
gg.searchNumber("-88.73961639404;28:512", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("28", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(2)
gg.editAll("-560", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("9.201618;30.5;25", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(10)
gg.editAll("250", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
gg.searchNumber("-298284466;-1.304566e23F", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("-298284466", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(99)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
gg.searchNumber("-1,883,348,481,058,764,210", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(99)
gg.editAll("-1,883,348,485,055,444,540", gg.TYPE_QWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
gg.searchNumber("0.10000000149;64.50088500977", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("0.10000000149", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(50)
gg.editAll("8", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("9.201618;30.5;25", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("30.5;25", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("220", gg.TYPE_FLOAT)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
gg.searchNumber("-298284466;-1.304566e23F", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("-298284466", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(99)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
gg.searchNumber("-1,883,348,481,058,764,210", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(99)
gg.editAll("-1,883,348,485,055,444,540", gg.TYPE_QWORD)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("9.20161819458;23;25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("700", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("23;25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("23;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(2)
gg.editAll("699", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("25;23;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(3)
gg.editAll("180", gg.TYPE_FLOAT)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("9.201618;30.5;25", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(15)
gg.editAll("450", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("🔥 Activated 🔥")
end

function SENIORKO2()
gg.clearResults()
so=gg.getRangesList('libUE4.so')[1].start
py=0x136D4F8
setvalue(so+py,16,0)
so=gg.getRangesList('libUE4.so')[1].start
py=0x376E57C
setvalue(so+py,16,0)
so=gg.getRangesList('libUE4.so')[1].start
py=0x381CCE0
setvalue(so+py,16,0)
so=gg.getRangesList('libUE4.so')[1].start
py=0x1C113E8
setvalue(so+py,16,1.40129846e-45)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(10)
gg.editAll("250", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("15;28;16;26;8;18", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(56)
gg.editAll("-1339", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("16000~99999;3D;0.1;1D::40", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("16000~99999", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("500000", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("0000B040rA;0000803FrA;0000403FrA:9", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(3)
gg.editAll("1,087,897,600;1,075,838,976;1,075,838,976", gg.TYPE_DWORD)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("88000;0.08600000292", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("88000", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(1401)
gg.editAll("400000", gg.TYPE_FLOAT)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("71500;0.10000000149", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("71500", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(1401)
gg.editAll("400000", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("87000;0.09600000083", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("87000", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(1401)
gg.editAll("400000", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("71500;0.109", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("71500", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(1401)
gg.editAll("400000", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("91500;0.07500000298", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("91500", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(1401)
gg.editAll("400000", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("25;30.5", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(10)
gg.editAll("189", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("15;28;16;26;8;18", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(56)
gg.editAll("-1339", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
gg.searchNumber("-298284466;-1.304566e23F", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("-298284466", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(99)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_C_DATA | gg.REGION_CODE_APP)
gg.searchNumber("-298284466;-1.304566e23F", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("-298284466", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(99)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("10;45", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("10", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("9999", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("🔥 Activated 🔥")
end

-- -- -- -- -- -- -- -- --   No Recoil Menu   -- -- -- -- -- -- -- -- --

function NORECMN1()
NORECMN1NMN = gg.multiChoice({
"🎯 『 ثبات سلاح %100 』",
"🕸 『 ثبات سلاح 』",
"🕸 『 ثبات سلاح v2 』",
"⚙️ 『 منع إهتزاز السلاح 』",
"💢 『 تصغير مؤشر التصويب 』",
"⁦➡️⁩ 『 رجوع 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if NORECMN1NMN == nil then else
if NORECMN1NMN [1] == true then NOREC100() end
if NORECMN1NMN [2] == true then LESSREC1() end
if NORECMN1NMN [3] == true then LESSREC2() end
if NORECMN1NMN [4] == true then NOSHAKE() end
if NORECMN1NMN [5] == true then SMALLCROSS() end
if NORECMN1NMN [6] == true then WEP1() end
end
PUBGMH = -1
end

function NORECMN2()
NORECMN2NMN = gg.multiChoice({
"🎯 『 ɴᴏ ʀᴇᴄᴏɪʟ 100% 』(ɴᴏᴛ ᴜꜱᴇ)",
"🕸 『 ʟᴇss ʀᴇᴄᴏɪʟ 』(ᴜꜱᴇ ᴏɴʟʏ)",
"🕸 『 ʟᴇss ʀᴇᴄᴏɪʟ v2 』(ᴜꜱᴇ ᴏɴʟʏ)",
"⚙️ 『 ᴀɴᴛɪ sʜᴀᴋᴇ 』",
"💢 『 sᴍᴀʟʟ ᴄʀᴏssʜᴀɪʀ 』",
"⬅️ 『 ʙ ᴀ ᴄ ᴋ 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if NORECMN2NMN == nil then else
if NORECMN2NMN [1] == true then NOREC100() end
if NORECMN2NMN [2] == true then LESSREC1() end
if NORECMN2NMN [3] == true then LESSREC2() end
if NORECMN2NMN [4] == true then NOSHAKE() end
if NORECMN2NMN [5] == true then SMALLCROSS() end
if NORECMN2NMN [6] == true then WEP2() end
end
PUBGMH = -1
end

function NOREC100() --1.2
gg.clearResults()
so=gg.getRangesList('libUE4.so')[1].start
py=0x136D4F8
setvalue(so+py,16,0)
so=gg.getRangesList('libUE4.so')[1].start
py=0x376E57C
setvalue(so+py,16,0)
so=gg.getRangesList('libUE4.so')[1].start
py=0x381CCE0
setvalue(so+py,16,0)
so=gg.getRangesList('libUE4.so')[1].start
py=0x1C113E8
setvalue(so+py,16,1.40129846e-45)
gg.clearResults()
gg.toast("No Recoil Activated")
end

function LESSREC1() --1.2
gg.clearResults()
gg.setRanges(gg.REGION_C_DATA)
gg.searchNumber("-2.2673448e24;-1.36203639e28", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("-1.36203639e28", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(99)
gg.editAll("0", gg.TYPE_FLOAT)
gg.toast("No Recoil Activated")
end

function LESSREC2() --1.2
gg.clearResults()
gg.setRanges(gg.REGION_C_DATA)
gg.searchNumber("-309056968;-298841599;-309061065", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("-298841599", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(5)
gg.editAll("0", gg.TYPE_DWORD)
gg.clearResults()
gg.toast("Less Recoil Activated v2")
gg.clearResults()
end

function NOSHAKE() --1.2
gg.clearResults()
so=gg.getRangesList('libUE4.so')[1].start
py=0x376E57C
setvalue(so+py,16,0)
so=gg.getRangesList('libUE4.so')[1].start
py=0x381CCE0
setvalue(so+py,16,0)
gg.clearResults()
gg.toast("Anti Shake Activated")
end

function SMALLCROSS() --1.2
gg.clearResults()
so=gg.getRangesList('libUE4.so')[1].start
py=0x1C113E8
setvalue(so+py,16,1.40129846e-45)
gg.clearResults()
gg.toast("Small Crosshair Activated")
end


-- -- -- -- -- -- -- -- --   Zoom Scope Menu   -- -- -- -- -- -- -- -- --

zoomx4 = off
zoomx8 = off
zoomx15 = off

function SCOP1()
SCOP1NMN = gg.choice({
"🔭 『 تكبير الريد دوت / هولو x4 』"..zoomx4,
"🔭 『 تكبير الريد دوت / هولو x8 』"..zoomx8,
"🔭 『 تكبير الريد دوت / هولو x15 』"..zoomx15,
"⁦➡️⁩ 『 رجوع 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if SCOP1NMN == nil then else
if SCOP1NMN == 1 then ZOOM4() end
if SCOP1NMN == 2 then ZOOM8() end
if SCOP1NMN == 3 then ZOOM15() end
if SCOP1NMN == 4 then WEP1() end
end
PUBGMH = -1
end

function SCOP2()
SCOP2NMN = gg.choice({
"🔭 『 ʀᴇᴅ ᴅᴏᴛ / ʜᴏʟᴏ ᴢᴏᴏᴍ 4x 』"..zoomx4,
"🔭 『 ʀᴇᴅ ᴅᴏᴛ / ʜᴏʟᴏ ᴢᴏᴏᴍ 8x 』"..zoomx8,
"🔭 『 ʀᴇᴅ ᴅᴏᴛ / ʜᴏʟᴏ ᴢᴏᴏᴍ 15x 』"..zoomx15,
"⬅️ 『 ʙ ᴀ ᴄ ᴋ 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if SCOP2NMN == nil then else
if SCOP2NMN == 1 then ZOOM4() end
if SCOP2NMN == 2 then ZOOM8() end
if SCOP2NMN == 3 then ZOOM15() end
if SCOP2NMN == 4 then WEP2() end
end
PUBGMH = -1
end

function ZOOM4()
if zoomx4 == off then
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("60;55;1.9618179e-44\000", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("55", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(300)
gg.editAll("20", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast('Zoom 4x ✔ activated!')
zoomx4 = on
else
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("60;20;1.9618179e-44\000", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("20", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(300)
gg.editAll("55", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Zoom 4x ✔ Deactivated")
zoomx4 = off
end
end

function ZOOM8()
if zoomx8 == off then
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("60;55;1.9618179e-44\000", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("55", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(300)
gg.editAll("15", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast('Zoom 8x ✔ activated!')
zoomx8 = on
else
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("60;15;1.9618179e-44\000", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("15", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(300)
gg.editAll("55", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Zoom 8x ✔ Deactivated")
zoomx8 = off
end
end

function ZOOM15()
if zoomx15 == off then
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("60;55;1.9618179e-44\000", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("55", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(300)
gg.editAll("9", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast('Zoom 15x ✔ activated!')
zoomx15 = on
else
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("60;9;1.9618179e-44\000", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("9", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(300)
gg.editAll("55", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Zoom 15x ✔ Deactivated")
zoomx15 = off
end
end

-- -- -- -- -- -- -- -- --   Speed Menu   -- -- -- -- -- -- -- -- --

fjump = off
fspeed2 = off
speedjeep = off
speeddacia = off
microspd = off

function SPD1()
SPD1NMN = gg.choice({
"🤾 『 قفزة أمامية 』 ☠️"..fjump,
"🛢 『 سرعة جيب + بانزين لاينتهي 』",
"⚡ 『 فلاش سبيد 』 ☠️"..fspeed1,
"⚡ 『 فلاش سبيد v2 』 ☠️"..fspeed2,
"🔧 『 إصلاح التقطيع 』",
"💥 『 إصلاح دمج الأسلحة 』",
"💀 『 سبيد نوك 』",
"🏃 『 سرعة لاعب خفيفة 』 ☠️"..microspd,
"☂️ 『 نزول برشوت سريع ᴘᴄ 』",
"☂️ 『 نزول برشوت مسافات بعيدة 』",
"?? 『 تسريع الجيب 』"..speedjeep,
"🚗 『 تسريع الداسيا 』"..speeddacia,
"⁦➡️⁩ 『 رجوع 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if SPD1NMN == nil then else
if SPD1NMN == 1 then FRONTJUMPON() end
if SPD1NMN == 2 then UNLIMITEDFUEL() end
if SPD1NMN == 3 then FLASHS1() end
if SPD1NMN == 4 then FLASHNEW1() end
if SPD1NMN == 5 then FIXFLASH() end
if SPD1NMN == 6 then FIXDMG() end
if SPD1NMN == 7 then KNOCKSPEED() end
if SPD1NMN == 8 then SPEEDON() end
if SPD1NMN == 9 then FASTPARA() end
if SPD1NMN == 10 then FASTPARA2() end
if SPD1NMN == 11 then JEEPS() end
if SPD1NMN == 12 then DACIA() end
if SPD1NMN == 13 then HOME1() end
end
PUBGMH = -1
end

function SPD2()
SPD2NMN = gg.choice({
"🤾 『 ғʀᴏɴᴛ ᴊᴜᴍᴘ 』 ☠️"..fjump,
"🛢 『 ᴜɴʟɪᴍɪᴛᴇᴅ ғᴜᴇʟ + sᴘᴇᴇᴅ ᴊᴇᴇᴘ 』",
"⚡ 『 ғʟᴀsʜ sᴘᴇᴇᴅ 』 ☠️"..fspeed1,
"⚡ 『 ғʟᴀsʜ sᴘᴇᴇᴅ v2 』 ☠️"..fspeed2,
"🔧 『 ғɪx ʟᴀɢ 』",
"?? 『 ғɪx ᴅᴀᴍᴀɢᴇ 』",
"💀 『 sᴘᴇᴇᴅ ᴋɴᴏᴄᴋ 』",
"🏃 『 ᴍɪᴄʀᴏ sᴘᴇᴇᴅ 』 ☠️"..microspd,
"☂️ 『 ғᴀsᴛ ᴘᴀʀᴀᴄʜᴜᴛᴇ ᴘᴄ 』",
"☂️ 『 ғᴀsᴛ ᴘᴀʀᴀᴄʜᴜᴛᴇ ʟᴏɴɢ ʀᴀɴɢᴇ 』",
"🚙 『 sᴘᴇᴇᴅ ᴊᴇᴇᴘ 』"..speedjeep,
"🚗 『 sᴘᴇᴇᴅ ᴅᴀᴄɪᴀ 』"..speeddacia,
"⬅️ 『 ʙ ᴀ ᴄ ᴋ 』",
  }, nil, "╔─━━━━━━━━░░ 👑 ░░━━━━━━━━─╗\nTG - @MODXPRO \n DEV: @MODXASHIS╚─━━━━━━━━░░  ★ ░░━━━━━━━━─╝")
if SPD2NMN == nil then else
if SPD2NMN == 1 then FRONTJUMPON() end
if SPD2NMN == 2 then UNLIMITEDFUEL() end
if SPD2NMN == 3 then FLASHS1() end
if SPD2NMN == 4 then FLASHNEW1() end
if SPD2NMN == 5 then FIXFLASH() end
if SPD2NMN == 6 then FIXDMG() end
if SPD2NMN == 7 then KNOCKSPEED() end
if SPD2NMN == 8 then SPEEDON() end
if SPD2NMN == 9 then FASTPARA() end
if SPD2NMN == 10 then FASTPARA2() end
if SPD2NMN == 11 then JEEPS() end
if SPD2NMN == 12 then DACIA() end
if SPD2NMN == 13 then HOME2() end
end
PUBGMH = -1
end

function FRONTJUMPON()
if fjump == off then
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("7.0064923e-45F;0.6~1;1065353216D;100F;1065353216D;2500000000F;0.10000000149F;88F::", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("7.0064923e-45F;0.6~1;1065353216D;100F;1065353216D;2500000000F;0.10000000149F;88F::", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("0.6~1", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("0.6~1", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
sjumpff1 = gg.getResults(2500)
gg.editAll("3.5241295", gg.TYPE_FLOAT)
gg.editAll("3.5241295", gg.TYPE_FLOAT)
gg.clearResults()
gg.searchNumber("300;0;0.05000000075;2;25::17", gg.TYPE_FLOAT, false)
gg.searchNumber("300;0;0.05000000075;2;25::17", gg.TYPE_FLOAT, false)
gg.refineNumber("0.05000000075", gg.TYPE_FLOAT, false)
gg.refineNumber("0.05000000075", gg.TYPE_FLOAT, false)
sjumpff2 = gg.getResults(2400)
gg.editAll("2.1241295", gg.TYPE_FLOAT)
gg.editAll("2.1241295", gg.TYPE_FLOAT)
gg.clearResults()
gg.clearResults()
gg.setRanges(gg.REGION_CODE_APP)
gg.searchNumber("-6.1526231e27;-1.0070975e28::", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("-6.1526231e27", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
sjumpff3 = gg.getResults(1)
gg.editAll("0", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Front Jump Activated!")
fjump = on
else
gg.clearResults()
gg.setValues(sjumpff1)
gg.setValues(sjumpff2)
gg.setValues(sjumpff3)
gg.clearResults()
gg.toast("Front Jump Deactivated")
fjump = off
end
end

function UNLIMITEDFUEL()
gg.clearResults()
gg.setRanges(32)
gg.searchNumber("0.647058857", 16, false, 536870912, 0, -1)
gg.getResults(30)
gg.editAll("-180", 16)
gg.clearResults()
gg.toast("Unlimited Fuel + Speed Jeep Activated!")
end

function FLASHS1()
if fspeed1 == off then
gg.clearResults()
gg.setVisible(false)
gg.setRanges(gg.REGION_C_DATA|gg.REGION_CODE_APP)
gg.searchNumber("-6.03221444e26;-1.3078764e28;-3.74440972e28;-1.86389771e-20;-1.11445016e28;-9.39921508e20;-1.8331477e27:33", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("-1.86389771e-20", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
fspeed1s1 = gg.getResults(100)
gg.editAll("0", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast('Flash Speed Activated!')
fspeed1 = on
else
gg.clearResults()
gg.setValues(fspeed1s1)
gg.clearResults()
gg.toast("Flash Speed Deactivated")
fspeed1 = off
end
end

function FLASHNEW1()
if fspeed2 == off then
gg.clearResults()
gg.setRanges(gg.REGION_CODE_APP)
gg.searchNumber("1,873,498,234,778,812,417", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("1,873,498,234,778,812,417", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("1,873,498,234,778,812,417", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
fspeed2s1 = gg.getResults(1401)
gg.editAll("1,873,498,234,778,812,416", gg.TYPE_QWORD)
gg.clearResults()
gg.setRanges(gg.REGION_CODE_APP)
gg.searchNumber("403,635,275,035,574,273", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("403,635,275,035,574,273", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("403,635,275,035,574,273", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
fspeed2s2 = gg.getResults(100)
gg.editAll("403,635,275,035,574,272", gg.TYPE_QWORD)
gg.clearResults()
gg.setRanges(gg.REGION_CODE_APP)
gg.searchNumber("-2,044,616,634,647,180,784", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("-2,044,616,634,647,180,784", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("-2,044,616,634,647,180,784", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
fspeed2s3 = gg.getResults(1401)
gg.editAll("-2,044,616,634,647,180,800", gg.TYPE_QWORD)
gg.clearResults()
gg.setRanges(gg.REGION_CODE_APP)
gg.searchNumber("-1296744149883614555", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("-1296744149883614555", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
gg.refineNumber("-1296744149883614555", gg.TYPE_QWORD, false, gg.SIGN_EQUAL, 0, -1)
fspeed2s4 = gg.getResults(1401)
gg.editAll("-1296744153870237696", gg.TYPE_QWORD)
gg.clearResults()
gg.toast('Flash Speed Activated!')
fspeed2 = on
else
gg.clearResults()
gg.setValues(fspeed2s1)
gg.setValues(fspeed2s2)
gg.setValues(fspeed2s3)
gg.setValues(fspeed2s4)
gg.clearResults()
gg.toast("Flash Speed Deactivated")
fspeed2 = off
end
end

function FIXFLASH()
gg.clearResults()
gg.setRanges(gg.REGION_C_DATA|gg.REGION_CODE_APP)
gg.searchNumber("-6.1526231e27;-1.0070975e28::",gg.TYPE_FLOAT,false,gg.SIGN_EQUAL,0,-1)
gg.searchNumber("-6.1526231e27",gg.TYPE_FLOAT,false,gg.SIGN_EQUAL,0,-1)
gg.getResults(1)
gg.editAll("0",gg.TYPE_FLOAT)
gg.clearResults()
gg.toast('Fix Lag Activated!')
end

function FIXDMG()
gg.clearResults()
gg.setRanges(32)
gg.searchNumber("50000~100000;0;1;5D~100D::13", 16, false, 536870912, 0, -1)
if gg.getResultCount() == 0 then
gg.toast("قم بالتفعيل مرة ثانية")
else
gg.searchNumber("50000~100000", 16, false, 536870912, 0, -1)
RFSSMG1 = gg.getResults(210)
gg.editAll("32465", 16)
gg.clearResults()
gg.toast("تم إصلاح دمج الأسلحة")
end 
gg.clearResults()
end

function KNOCKSPEED()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("0;7.0064923e-45;1;100;1;2,500,000,000.0;0.10000000149;88", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("1", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("1.7", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Knock Speed Activated")
end

function SPEEDON()
if microspd == off then
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("1;1;1;0.0001;20;0.0005;0.4::50", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("1", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(300)
gg.editAll("1.06", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast('Medium Speed activated!')
microspd = on
else
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("1.06;1.06;1.06;0.0001;20;0.0005;0.4::50", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("1.06", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(300)
gg.editAll("1", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast('Medium Speed deactivated!')
microspd = off
end
end

function FASTPARA()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("200;200;1;1::13", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("1", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResultCount()
gg.getResults(21)
gg.editAll("4412", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Fast Parachute activated!")
end

function FASTPARA2()
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("0.75;150;1", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("1", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("30", gg.TYPE_FLOAT)
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber("0.75;150;30", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber("0.75", gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.getResults(100)
gg.editAll("0", gg.TYPE_FLOAT)
gg.clearResults()
gg.toast("Fast Parachute activated!")
gg.clearResults()
end

function JEEPS()
if speedjeep == off then
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber('0.647058857;0.30000001192;0.94117647409::9', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber('0.647058857;0.30000001192::5', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber('0.647058857;0.30000001192::5', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber('0.647058857;0.30000001192::5', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
speedjeeps1 = gg.getResults(50)
gg.editAll('50.241295', gg.TYPE_FLOAT)
gg.clearResults()
gg.toast('Jeep Speed activated!')
speedjeep = on
else
gg.clearResults()
gg.setValues(speedjeeps1)
gg.clearResults()
gg.toast("Jeep Speed Deactivated")
speedjeep = off
end
end

function DACIA()
if speeddacia == off then
gg.clearResults()
gg.setRanges(gg.REGION_ANONYMOUS)
gg.searchNumber('1000;10;4D;4D;50;5;2;0.03::', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber('0.03', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber('0.03', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
gg.searchNumber('0.03', gg.TYPE_FLOAT, false, gg.SIGN_EQUAL, 0, -1)
speeddacias1 = gg.getResults(280)
gg.editAll('-0.23', gg.TYPE_FLOAT)
gg.clearResults()
gg.toast('Speed Dacia activated!')
speeddacia = on
else
gg.clearResults()
gg.setValues(speeddacias1)
gg.clearResults()
gg.toast("Speed Dacia Deactivated")
speeddacia = off
end
end

-- -- -- -- -- -- -- -- -- -- --   Close   -- -- -- -- -- -- -- -- -- -- --

function CLOSE()
print (" ")
print(" 🥰ᴛʜᴀɴᴋs ғᴏʀ ᴜsɪɴɢ ᴏᴜʀ ᴠɪᴘ🥰 ")
print (" ")
print (" 🚫MODXPRO PUBG HACKS🚫 ")
gg.skipRestoreState()
gg.setVisible(true)
os.exit()
end
while true do
  if gg.isVisible(true) then
PUBGMH = 1
gg.setVisible(false)
  end
if PUBGMH == 1 and CMENU == 0 then
HOME()
  end
  if PUBGMH == 1 and CMENU == 1 then
HOME1()
  end
  if PUBGMH == 1 and CMENU == 2 then
HOME2()
  end
end
