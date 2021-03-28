---
description: Utilisé par la fonction SHGetSetSettings pour spécifier les membres de sa structure SHELLSTATE qui doivent être définis ou récupérés.
title: Constantes SSF (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2a883110-fdc3-4451-9e47-e58894600e3b
api_name:
- SSF_SHOWALLOBJECTS
- SSF_SHOWEXTENSIONS
- SSF_HIDDENFILEEXTS
- SSF_SERVERADMINUI
- SSF_SHOWCOMPCOLOR
- SSF_SORTCOLUMNS
- SSF_SHOWSYSFILES
- SSF_DOUBLECLICKINWEBVIEW
- SSF_SHOWATTRIBCOL
- SSF_DESKTOPHTML
- SSF_WIN95CLASSIC
- SSF_DONTPRETTYPATH
- SSF_MAPNETDRVBUTTON
- SSF_SHOWINFOTIP
- SSF_HIDEICONS
- SSF_NOCONFIRMRECYCLE
- SSF_FILTER
- SSF_WEBVIEW
- SSF_SHOWSUPERHIDDEN
- SSF_SEPPROCESS
- SSF_NONETCRAWLING
- SSF_STARTPANELON
- SSF_SHOWSTARTPAGE
- SSF_AUTOCHECKSELECT
- SSF_ICONSONLY
- SSF_SHOWTYPEOVERLAY
- SSF_SHOWSTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b26ba102ff72caf235a51d3888183ccafba9d639
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991637"
---
# <a name="ssf-constants"></a>Constantes SSF

Utilisé par la fonction [**SHGetSetSettings**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings) pour spécifier les membres de sa structure [**SHELLSTATE**](/windows/win32/api/shlobj_core/ns-shlobj_core-shellstatea) qui doivent être définis ou récupérés.

<dl> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ SHOWALLOBJECTS**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Le membre **fShowAllObjects** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_ SHOWEXTENSIONS**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Le membre **fShowExtensions** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ HIDDENFILEEXTS**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Non utilisé.


</dt> </dl> </dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ SERVERADMINUI**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Non utilisé.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ SHOWCOMPCOLOR**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Le membre **fShowCompColor** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ SORTCOLUMNS**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Les membres **lParamSort** et **iSortDirection** sont demandés.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_ SHOWSYSFILES**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Le membre **fShowSysFiles** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ DOUBLECLICKINWEBVIEW**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Le membre **fDoubleClickInWebView** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ SHOWATTRIBCOL**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Le membre **fShowAttribCol** est demandé.

**Windows Vista :** Non utilisé.


</dt> </dl> </dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ DESKTOPHTML**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Le membre **fDesktopHTML** est demandé. L’ensemble n’est pas disponible. Au lieu de cela, pour les versions de Windows antérieures à Windows XP, activez Desktop HTML par [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop). Toutefois, l’utilisation de **IActiveDesktop** à cet effet n’est pas recommandée pour Windows XP et les versions ultérieures de Windows. elle est déconseillée dans Windows Vista.


</dt> </dl> </dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Le membre **fWin95Classic** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ DONTPRETTYPATH**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Le membre **fDontPrettyPath** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ MAPNETDRVBUTTON**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Le membre **fMapNetDrvBtn** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ SHOWINFOTIP**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Le membre **fShowInfoTip** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_ HIDEICONS**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Le membre **fHideIcons** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ NOCONFIRMRECYCLE**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Le membre **fNoConfirmRecycle** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>**\_filtre SSF**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Le membre **fFilter** est demandé.

**Windows Vista :** Non utilisé.


</dt> </dl> </dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**WebView SSF \_**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Le membre **fWebView** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ SHOWSUPERHIDDEN**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Le membre **fShowSuperHidden** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ SEPPROCESS**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Le membre **fSepProcess** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ NONETCRAWLING**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



**Windows XP et versions ultérieures**. Le membre **fNoNetCrawling** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ STARTPANELON**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



**Windows XP et versions ultérieures**. Le membre **fStartPanelOn** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ SHOWSTARTPAGE**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Non utilisé.


</dt> </dl> </dd> <dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ AUTOCHECKSELECT**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



**Windows Vista et versions ultérieures**. Le membre **fAutoCheckSelect** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ ICONSONLY**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



**Windows Vista et versions ultérieures**. Le membre **fIconsOnly** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ SHOWTYPEOVERLAY**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



**Windows Vista et versions ultérieures**. Le membre **fShowTypeOverlay** est demandé.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSTATUSBAR"></span><span id="ssf_showstatusbar"></span>**SSF \_ SHOWSTATUSBAR**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



**Windows 8 et versions ultérieures**: le membre **fShowStatusBar** est demandé.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
