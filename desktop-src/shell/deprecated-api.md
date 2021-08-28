---
description: Les API suivantes sont déconseillées ou remplacées par des API plus récentes.
title: API Shell dépréciées
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 30B02395-8407-4B70-A70F-F0DEE20D8ACC
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 04b3a575f2d65a1527393f33b8d56ed98377a36a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477635"
---
# <a name="deprecated-shell-apis"></a>API Shell dépréciées

\[Les [**FOLDERSETDATA**](/windows/win32/api/shdeprecated/ns-shdeprecated-foldersetdata) peuvent être modifiés ou non disponibles dans les versions ultérieures du système d’exploitation ou du produit.\]

\[cette fonction est disponible par le biais de Windows XP avec Service Pack 2 (SP2) et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows. \]

\[cette fonction est disponible dans Windows 2000 et par le biais de Windows XP Service Pack 2 (SP2). il n’est plus disponible à partir de Windows Vista.\]

\[cette fonction est disponible via Windows XP avec SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[[**CharLowerWrapW**](charlowerwrapw.md) peut être utilisé dans Windows XP. Elle n’est peut-être pas disponible dans les versions ultérieures. Vous devez utiliser [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) à la place.\]

\[[**CharUpperBuffWrapW**](charupperbuffwrapw.md) peut être utilisé dans Windows XP. Elle n’est peut-être pas disponible dans les versions ultérieures. Vous devez utiliser [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) à la place.\]

\[[**CompareStringWrapW**](comparestringwrapw.md) peut être utilisé dans Windows XP. Elle ne sera pas disponible dans les versions ultérieures. Vous devez utiliser [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) à la place.\]

\[cette fonction est disponible par le biais de Windows XP et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction est disponible via Windows XP avec SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction n’est pas disponible à partir de Windows Vista.\]

\[Cette fonction est déconseillée et peut être modifiée ou non disponible dans les versions ultérieures.\]

\[[**Dad \_ le défilement**](/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_autoscroll) automatique est disponible dans Windows 2000 et Windows XP. Il peut être modifié ou non disponible dans les versions ultérieures.\]

\[[**Dad \_ DragEnterEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_dragenterex) est disponible dans Windows 2000 et Windows XP. Il peut être modifié ou non disponible dans les versions ultérieures. Utilisez [**ImageList \_ DragEnter**](/windows/win32/api/commctrl/nf-commctrl-imagelist_dragenter) à la place. \]

\[[**Dad \_ DragEnterEx2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_dragenterex2) est disponible dans Windows 2000 et Windows XP. Il peut être modifié ou non disponible dans les versions ultérieures. Utilisez [**ImageList \_ DragEnter**](/windows/win32/api/commctrl/nf-commctrl-imagelist_dragenter) à la place.\]

\[[**Dad \_ DragLeave**](/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_dragleave) est disponible dans Windows 2000 et Windows XP. Il peut être modifié ou non disponible dans les versions ultérieures. Utilisez [**ImageList \_ DragLeave**](/windows/win32/api/commctrl/nf-commctrl-imagelist_dragleave) à la place.\]

\[[**Dad \_ DragMove**](/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_dragmove) est disponible dans Windows 2000 et Windows XP. Il peut être modifié ou non disponible dans les versions ultérieures. Utilisez [**ImageList \_ DragMove**](/windows/win32/api/commctrl/nf-commctrl-imagelist_dragmove) à la place. \]

\[[**Dad \_ SetDragImage**](/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_setdragimage) est disponible dans Windows 2000 et Windows XP. Il peut être modifié ou non disponible dans les versions ultérieures. Utilisez [**ImageList \_ BeginDrag**](/windows/win32/api/commctrl/nf-commctrl-imagelist_begindrag) à la place.\]

\[[**Dad \_ ShowDragImage**](/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_showdragimage) est disponible dans Windows 2000 et Windows XP. Il peut être modifié ou non disponible dans les versions ultérieures. Utilisez [**ImageList \_ DragShowNolock**](/windows/win32/api/commctrl/nf-commctrl-imagelist_dragshownolock) à la place. \]

\[Cette fonction est conservée uniquement à des fins de compatibilité descendante. Utilisez [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) à la place.\]

\[cette fonction est disponible via Windows XP avec SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows. \]

\[cette fonction est disponible sur Windows XP avec SP2 via Windows Vista. Il peut être modifié ou non disponible dans les versions ultérieures de Windows. À la place, les applications clientes doivent utiliser [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) pour présenter un environnement utilisateur qui permet de télécharger et d’échanger des fichiers en toute sécurité via des pièces jointes de messagerie électronique et de messagerie.\]

\[[**FindResourceWrapW**](findresourcewrapw.md) peut être utilisé dans Windows XP. Elle n’est peut-être pas disponible dans les versions ultérieures. Vous devez utiliser [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) à la place.\]

\[[**GetDateFormatWrapW**](getdateformatwrapw.md) peut être utilisé dans Windows XP. Elle ne sera pas disponible dans les versions ultérieures. Vous devez utiliser [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) à la place.\]

\[cette fonction est disponible via Windows XP SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[[**GetTimeFormatWrapW**](gettimeformatwrapw.md) peut être utilisé dans Windows XP. Elle n’est peut-être pas disponible dans les versions ultérieures. Vous devez utiliser [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) à la place.\]

\[[**GUIDFromString**](guidfromstring.md) est disponible via Windows XP avec SP2 ou Windows Vista. Il peut être modifié ou non disponible dans les versions ultérieures. Les applications doivent utiliser [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) ou [**échec iidfromstring**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) à la place de cette fonction.\]

\[cette fonction est disponible via Windows XP SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[[**IsCharAlphaNumericWrapW**](ischaralphanumericwrapw.md) peut être utilisé dans Windows XP. Elle ne sera pas disponible dans les versions ultérieures. Vous devez utiliser [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) à la place.\]

\[cette fonction est disponible via Windows XP SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows. Utilisez [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) ou [**WNetGetConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona) à la place.\]

\[cette interface est prise en charge par Windows XP SP2 et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

\[cette fonction est disponible via Windows XP avec SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows. Utilisez [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) à la place.\]

\[cette fonction est disponible via Windows XP avec SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction ne peut pas être utilisée à partir de Windows 7.\]

\[cette fonction est disponible par le biais de Windows XP et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction ne peut pas être utilisée à partir de Windows 7.\]

\[cette fonction est disponible par le biais de Windows XP et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction peut être utilisée dans Windows XP. Elle n’est peut-être pas disponible dans les versions ultérieures. Utilisez [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) à la place.\]

\[la fonction [**ParseField**](parsefield.md) est actuellement censée être utilisée dans la prochaine version du système d’exploitation Microsoft Windows. Il peut être modifié ou non disponible dans les versions ultérieures.\]

\[cette fonction est disponible via Windows XP avec SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction est disponible via Windows XP avec SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction n’est pas prise en charge à partir de Windows Vista.\]

\[cette fonction est disponible via Windows XP SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction est disponible via Windows XP SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction est disponible via Windows XP SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction est disponible via Windows XP SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows. Utilisez [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) à la place.\]

\[cette fonction est disponible par le biais de Windows XP et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction est disponible par le biais de Windows XP et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[Cette structure n’est pas prise en charge.\]

\[cette fonction est disponible via Windows XP SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows. Utilisez [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) à la place.\]

\[[**SHCreateProcessAsUserW**](/windows/desktop/api/Shellapi/nf-shellapi-shcreateprocessasuserw) n’est pas implémenté sous Windows XP ou les systèmes ultérieurs.\]

\[[**SHCreateProcessAsUserW**](/windows/desktop/api/Shellapi/nf-shellapi-shcreateprocessasuserw) n’est plus implémenté dans Windows XP ou versions ultérieures.\]

\[Cette fonction est déconseillée. Utilisez [**CreateClassMoniker**](/windows/win32/api/objbase/nf-objbase-createclassmoniker) à la place. Notez que le CLSID utilisé dans l’appel à **CreateClassMoniker** doit être défini par l’application. N’appelez pas **CreateClassMoniker** avec un CLSID défini par le système.\]

\[[**SHDestroyPropSheetExtArray**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdestroypropsheetextarray) peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

\[cette fonction est disponible via Windows XP SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[[**SHExtractIconsW**](shextracticonsw.md) est disponible via Windows XP SP2. Il peut être modifié ou non disponible dans les versions ultérieures.\]

\[cette fonction est disponible via Windows XP SP2 et Windows Server 2003. elle n’est pas prise en charge sous Windows Vista et versions ultérieures. Utilisez [**OleFlushClipboard**](/windows/win32/api/ole2/nf-ole2-oleflushclipboard) à la place.\]

\[cette fonction est disponible via Windows XP SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows. Utilisez [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) à la place.\]

\[cette fonction est disponible par le biais de Windows XP et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[[**SHGetMalloc**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetmalloc) est disponible via Windows Vista et Windows Server 2003, mais peut être modifié ou non disponible dans les versions ultérieures du système d’exploitation ou du produit. Pour obtenir d’autres recommandations, consultez la section Notes.\]

\[[**SHGetShellStyleHInstance**](/previous-versions/windows/desktop/legacy/bb762202(v=vs.85)) peut être utilisé dans le système d’exploitation Windows XP jusqu’à SP2, y compris. elle n’est pas disponible dans les versions ultérieures de Windows, comme Windows Vista.\]

\[cette fonction est disponible par le biais de Windows XP et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction est disponible via Windows XP SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction est disponible via Windows XP SP2 et Windows Server 2003. elle n’est pas prise en charge à partir de Windows Vista.\]

\[cette fonction est disponible via Windows XP SP2 et Windows Server 2003. elle n’est pas disponible à partir de Windows Vista.\]

\[Cette fonction n’est plus prise en charge.\]

\[Cette fonction n’est plus prise en charge.\]

\[cette fonction est disponible via Windows XP SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction est disponible par le biais de Windows XP et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction est disponible par le biais de Windows XP et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction est disponible par le biais de Windows XP et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction est disponible par le biais de Windows XP et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cette fonction est disponible via Windows XP avec SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cet objet est disponible via Windows XP SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cet objet est disponible via Windows XP SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cet objet est disponible via Windows XP SP2 et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cet objet est disponible via Windows XP Service Pack 2 (SP2) et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

\[cet objet est pris en charge par Windows XP SP2 et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

\[cet objet est pris en charge par Windows XP SP2 et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

\[cet objet est pris en charge par Windows XP SP2 et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

\[cet objet est pris en charge par Windows XP SP2 et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

\[cet objet est pris en charge par Windows XP SP2 et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

\[cet objet est pris en charge par Windows XP SP2 et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

\[la seule méthode, [**DoContextMenuPopup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenusite-docontextmenupopup), ne peut plus être utilisée à partir de Windows Server 2003.\]

\[Cette interface a été déconseillée. il est pris en charge par Windows XP SP2 et Windows Server 2003. elle n’est pas prise en charge à partir de Windows Vista.\]

\[Les [**IDeskBandInfo**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskbandinfo) peuvent être modifiés ou non disponibles dans les versions ultérieures du système d’exploitation ou du produit.\]

\[cette interface est prise en charge via Windows XPSP2 et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

\[cette interface est prise en charge par Windows XP SP2 et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

\[cette interface est prise en charge par Windows XP SP2 et Windows Server 2003. elle n’est pas prise en charge à partir de Windows Vista.\]

\[l’interface [**IEnumSyncItems**](/previous-versions/windows/desktop/legacy/bb761957(v=vs.85)) peut être utilisée via Windows XP. Elle n’est pas disponible dans les versions ultérieures de Windows.\]

\[l’interface [**IEnumSyncSchedules**](/previous-versions/windows/desktop/legacy/bb761937(v=vs.85)) peut être utilisée via Windows XP. Elle n’est pas disponible dans les versions ultérieures de Windows.\]

\[l’interface [**IIdentityChangeNotify**](iidentitychangenotify.md) peut être utilisée dans Windows 2000. dans Windows XP, cette fonctionnalité a été remplacée par [des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance](fastuserswitching.md)et peut être modifiée ou non disponible dans les versions ultérieures.\]

\[cette interface est prise en charge par Windows XP SP2 et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

\[cette interface n’est pas prise en charge à partir de Windows Vista. Elle a été supprimée des en-têtes publics.\]

\[cette interface est prise en charge par Windows XP SP2 et Windows Server 2003. elle n’est pas prise en charge à partir de Windows Vista.\]

\[cette interface est prise en charge par Windows XP SP2 et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

\[[**IShellFolderView**](/windows/win32/api/shlobj_core/nn-shlobj_core-ishellfolderview) n’est plus disponible pour une utilisation à partir de Windows 7. Utilisez plutôt [**IFolderView2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2) et [**IFolderView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview).\]

\[Cette interface n’est finalement pas prise en charge. il est recommandé d’utiliser les api Windows GDI+ à la place des méthodes [**IShellImageData**](/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata) .\]

\[[**IShellTaskScheduler2**](/previous-versions/windows/desktop/legacy/bb774852(v=vs.85)) est disponible dans Windows XP. Il peut être modifié ou non disponible dans les versions ultérieures.\]

\[l’interface [**ISyncSchedule**](/previous-versions/windows/desktop/isync-schedule/bb774693(v=vs.85)) peut être utilisée via Windows XP. Elle n’est pas disponible dans les versions ultérieures de Windows.\]

\[l’interface [**ISyncScheduleMgr**](/previous-versions/windows/desktop/isync-schedule-mgr/bb774672(v=vs.85)) peut être utilisée via Windows XP. Elle n’est pas disponible dans les versions ultérieures de Windows.\]

\[[**ITravelEntry**](/windows/desktop/api/Shdeprecated/nn-shdeprecated-itravelentry) peut ne pas être pris en charge dans les versions de Windows ultérieures à Windows XP.\]

\[cette notification est prise en charge par Windows XP SP2 et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

\[cette notification est prise en charge par Windows XP SP2 et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

Les API suivantes sont déconseillées ou remplacées par des API plus récentes.

## <a name="in-this-section"></a>Contenu de cette section




| Rubrique | Description | 
|-------|-------------|
| <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-auto_scroll_data"><strong>AUTO_SCROLL_DATA</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-auto_scroll_data"><strong>AUTO_SCROLL_DATA</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-cabinetstate"><strong>CABINETSTATE</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-cabinetstate"><strong>CABINETSTATE</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo"><strong>DESKBANDINFO</strong></a><br /> | Reçoit des informations sur un objet de bande. Cette structure est utilisée avec la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ideskband-getbandinfo"><strong>IDeskBand :: GetBandInfo</strong></a> déconseillée.<br /> | 
| <a href="/windows/desktop/api/shdeprecated/ne-shdeprecated-securelockcode"><strong>SECURELOCK</strong></a><br /> | Action déconseillée. Cette énumération est utilisée par la structure <a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a> pour indiquer l’état de l’icône de verrou du navigateur de base.<br /> | 
| <a href="/windows/win32/api/shdeprecated/ns-shdeprecated-foldersetdata"><strong>FOLDERSETDATA</strong></a><br /> | Action déconseillée. Données utilisées dans <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-getfoldersetdata"><strong>IBrowserService2 :: GetFolderSetData</strong></a>.<br /> | 
| <a href="/windows/win32/api/shdeprecated/ns-shdeprecated-toolbaritem"><strong>TOOLBARITEM</strong></a><br /> | Action déconseillée. Données utilisées dans <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-_gettoolbaritem"><strong>IBrowserService2 :: _GetToolbarItem</strong></a>, <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-v_maygetnexttoolbarfocus"><strong>IBrowserService2 :: v_MayGetNextToolbarFocus</strong></a>et <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-_setfocus"><strong>IBrowserService2 :: _SetFocus</strong></a> pour définir un élément de barre d’outils.<br /> | 
| <a href="addmrustring.md"><strong>AddMRUStringW</strong></a><br /> | Ajoute une chaîne en haut de la liste des derniers fichiers utilisés.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb776387(v=vs.85)"><strong>CallCPLEntry16</strong></a><br /> | N’exécute aucune fonction. Fourni pour la compatibilité ascendante.<br /> | 
| <a href="cansharefolderw.md"><strong>CanShareFolderW</strong></a><br /> | Utilisé pour déterminer s’il faut afficher l’option <strong>partager ce dossier</strong> dans l’affichage Web.<br /> | 
| <a href="charlowerwrapw.md"><strong>CharLowerWrapW</strong></a><br /> | Convertit une chaîne de caractères Unicode ou un caractère unique en minuscules. Si l’opérande est une chaîne de caractères, la fonction convertit les caractères sur place. <br /><blockquote>[!Note]<br /><a href="charlowerwrapw.md"><strong>CharLowerWrapW</strong></a> est un wrapper pour la fonction <strong>CharLowerW</strong> . Pour plus d’informations sur les remarques d’utilisation, consultez la page <a href="/windows/desktop/api/winuser/nf-winuser-charlowera"><strong>CharLower</strong></a> .</blockquote><br /> | 
| <a href="charupperbuffwrapw.md"><strong>CharUpperBuffWrapW</strong></a><br /> | Convertit les caractères minuscules d’une mémoire tampon en caractères majuscules. La fonction convertit les caractères sur place. <br /><blockquote>[!Note]<br /><a href="charupperbuffwrapw.md"><strong>CharUpperBuffWrapW</strong></a> est un wrapper pour la fonction <strong>CharUpperBuffW</strong> . Pour plus d’informations sur les remarques d’utilisation, consultez la page <a href="/windows/desktop/api/winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a> .</blockquote><br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-cidldata_createfromidarray"><strong>CIDLData_CreateFromIDArray</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-cidldata_createfromidarray"><strong>CIDLData_CreateFromIDArray</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="comparestringwrapw.md"><strong>CompareStringWrapW</strong></a><br /> | Compare deux chaînes de caractères Unicode à l’aide des paramètres régionaux spécifiés. <br /><blockquote>[!Note]<br /><a href="comparestringwrapw.md"><strong>CompareStringWrapW</strong></a> est un wrapper pour la fonction <strong>CompareStringW</strong> . Pour plus d’informations sur les remarques d’utilisation, consultez la page <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a> .</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-connecttoconnectionpoint"><strong>ConnectToConnectionPoint</strong></a><br /> | Établit ou met fin à une connexion entre le récepteur d’un client et un conteneur de point de connexion.<br /> | 
| <a href="createhardwareeventmoniker.md"><strong>CreateHardwareEventMoniker</strong></a><br /> | Crée un moniker qui représente un composant matériel et son gestionnaire d’événements associé. La lecture automatique utilise cette fonction pour permettre aux applications d’utiliser des événements de lecture automatique.<br /> | 
| <a href="createuserprofileex.md"><strong>CreateUserProfileEx</strong></a><br /> | Crée un profil utilisateur pour un utilisateur spécifié. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/cc448310(v=vs.85)"><strong>CscSearchApiGetInterface</strong></a><br /> | Crée une instance d’un objet <a href="/previous-versions/windows/desktop/legacy/cc448312(v=vs.85)"><strong>CCscSearchApiInterface</strong></a> .<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_autoscroll"><strong>DAD_AutoScroll</strong></a><br /> | Fait défiler la fenêtre pendant le glissement d’une image.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_dragenterex"><strong>DAD_DragEnterEx</strong></a><br /> | Verrouille les mises à jour de la fenêtre spécifiée pendant une opération glisser et affiche l’image de glissement à la position spécifiée dans la fenêtre.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_dragenterex2"><strong>DAD_DragEnterEx2</strong></a><br /> | Verrouille les mises à jour de la fenêtre spécifiée pendant une opération de glisser-déplacer et affiche l’image de glissement à la position spécifiée dans la fenêtre.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_dragleave"><strong>DAD_DragLeave</strong></a><br /> | Déverrouille la fenêtre verrouillée par la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_dragenterex"><strong>DAD_DragEnterEx</strong></a> . <br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_dragmove"><strong>DAD_DragMove</strong></a><br /> | Déplace l’image glissée pendant une opération de glisser-déplacer.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_setdragimage"><strong>DAD_SetDragImage</strong></a><br /> | Définit l’image du glissement.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_showdragimage"><strong>DAD_ShowDragImage</strong></a><br /> | Affiche ou masque l’image glissée.<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-doenvironmentsubsta"><strong>DoEnvironmentSubst</strong></a><br /> | Analyse une chaîne d’entrée qui contient des références à une ou plusieurs variables d’environnement et les remplace par leurs valeurs entièrement développées. <br /> | 
| <a href="/windows/desktop/api/shlobj/nf-shlobj-drivetype"><strong>DriveType</strong></a><br /> | <a href="/windows/desktop/api/shlobj/nf-shlobj-drivetype"><strong>DriveType</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="enummrulist.md"><strong>EnumMRUListW</strong></a><br /> | Énumère le contenu de la liste MRU. Récupère éventuellement un élément de l’énumération.<br /> | 
| <a href="estimatefilerisklevel.md"><strong>EstimateFileRiskLevel</strong></a><br /> | Estime le risque d’exécution de code inconnu lorsqu’un gestionnaire est appelé sur un fichier donné. Ce risque est basé sur une compréhension du gestionnaire et le contenu du code du fichier.<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-extractassociatediconexa"><strong>ExtractAssociatedIconEx</strong></a><br /> | <a href="/windows/desktop/api/Shellapi/nf-shellapi-extractassociatediconexa"><strong>ExtractAssociatedIconEx</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="findresourcewrapw.md"><strong>FindResourceWrapW</strong></a><br /> | Détermine l’emplacement d’une ressource avec le type et le nom spécifiés, dans le module spécifié. <br /><blockquote>[!Note]<br /><a href="findresourcewrapw.md"><strong>FindResourceWrapW</strong></a> est un wrapper pour la fonction <strong>FindResourceW</strong> . Pour plus d’informations sur l’utilisation, consultez <a href="/windows/desktop/api/winbase/nf-winbase-findresourcea"><strong>FindResource</strong></a> .</blockquote><br /> | 
| <a href="getdateformatwrapw.md"><strong>GetDateFormatWrapW</strong></a><br /> | Met en forme une date sous forme de chaîne de date pour les paramètres régionaux spécifiés. La fonction met en forme une date spécifiée ou la date du système local. <br /><blockquote>[!Note]<br /><a href="getdateformatwrapw.md"><strong>GetDateFormatWrapW</strong></a> est un wrapper pour la fonction <strong>GetDateFormatW</strong> . Pour plus d’informations sur les remarques d’utilisation, consultez la page <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata"><strong>GetDateFormat</strong></a> .</blockquote><br /> | 
| <a href="/windows/desktop/api/shlobj/nf-shlobj-getfilenamefrombrowse"><strong>GetFileNameFromBrowse</strong></a><br /> | Crée une boîte de dialogue <strong>ouverte</strong> qui permet à l’utilisateur de spécifier le lecteur, le répertoire et le nom d’un fichier à ouvrir.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getmenuposfromid"><strong>GetMenuPosFromID</strong></a><br /> | <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getmenuposfromid"><strong>GetMenuPosFromID</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="gettimeformatwrapw.md"><strong>GetTimeFormatWrapW</strong></a><br /> | Met en forme l’heure sous la forme d’une chaîne d’heure pour les paramètres régionaux spécifiés. La fonction met en forme une heure spécifiée ou l’heure système locale. <br /><blockquote>[!Note]<br /><a href="gettimeformatwrapw.md"><strong>GetTimeFormatWrapW</strong></a> est un wrapper pour la fonction <strong>GetTimeFormatW</strong> . Pour plus d’informations sur les remarques d’utilisation, consultez la page <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata"><strong>getTimeFormat</strong></a> .</blockquote><br /> | 
| <a href="guidfromstring.md"><strong>GUIDFromString</strong></a><br /> | Convertit une chaîne en GUID.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-illoadfromstream"><strong>ILLoadFromStream</strong></a><br /> | Action déconseillée. Charge une structure <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> à partir d’un flux.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-illoadfromstreamex"><strong>ILLoadFromStreamEx (IStream *, PIDLIST_ABSOLUTE*)</strong></a><br /> | Cette fonction peut être modifiée ou non disponible.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb776452(v=vs.85)"><strong>ILLoadFromStreamEx (IStream *, PIDLIST_RELATIVE*)</strong></a><br /> | Cette fonction peut être modifiée ou non disponible.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb776453(v=vs.85)"><strong>ILLoadFromStreamEx (IStream *, PITEMID_CHILD*)</strong></a><br /> | Cette fonction peut être modifiée ou non disponible.<br /> | 
| <a href="ischaralphanumericwrapw.md"><strong>IsCharAlphaNumericWrapW</strong></a><br /> | Détermine si un caractère est un caractère alphabétique ou numérique. Cette détermination est basée sur la sémantique de la langue sélectionnée par l’utilisateur pendant l’installation ou par le biais du panneau de configuration. <br /><blockquote>[!Note]<br /><a href="ischaralphanumericwrapw.md"><strong>IsCharAlphaNumericWrapW</strong></a> est un wrapper pour la fonction <strong>IsCharAlphaNumericW</strong> . Pour plus d’informations sur les remarques d’utilisation, consultez la page <a href="/windows/desktop/api/winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a> .</blockquote><br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-isnetdrive"><strong>IsNetDrive</strong></a><br /> | Teste si un lecteur est un lecteur réseau.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-isuseranadmin"><strong>IsUserAnAdmin</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-isuseranadmin"><strong>IsUserAnAdmin</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-lpfndfmcallback"><strong>LPFNDFMCALLBACK</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-lpfndfmcallback"><strong>LPFNDFMCALLBACK</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-lpfnviewcallback"><strong>LPFNVIEWCALLBACK</strong></a><br /> | Définit le prototype pour la fonction de rappel utilisée par l’objet de vue de dossier système. Cette fonction duplique essentiellement les fonctionnalités de <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellfolderviewcb"><strong>IShellFolderViewCB</strong></a>.<br /> | 
| <a href="linkwindow-registerclass.md"><strong>LinkWindow_RegisterClass</strong></a><br /> | Inscrit une classe de fenêtre qui permet d’utiliser le contrôle commun <a href="/windows/desktop/Controls/syslink-overview">Syslink</a> dans une fenêtre.<br /> | 
| <a href="linkwindow-unregisterclass.md"><strong>LinkWindow_UnregisterClass</strong></a><br /> | Annule l’inscription d’une classe de fenêtre inscrite par <a href="linkwindow-registerclass.md"><strong>LinkWindow_RegisterClass</strong></a>.<br /> | 
| <a href="/windows/desktop/shell/about-user-profiles"><strong>MLFreeLibrary</strong></a><br /> | Annule le mappage d’une DLL de ressource chargée par la fonction <a href="/windows/desktop/shell/callbacks"><strong>MLLoadLibrary</strong></a> . <br /> | 
| <a href="mlhtmlhelp.md"><strong>MLHtmlHelp</strong></a><br /> | Affiche une fenêtre d’aide qui correspond au paramètre de langue de l’interface utilisateur actuel.<br /> | 
| <a href="/windows/desktop/shell/callbacks"><strong>MLLoadLibrary</strong></a><br /> | Cartes une DLL de ressource appropriée dans l’espace d’adressage de la fonction appelante, en fonction de la langue de l’interface utilisateur par défaut de l’utilisateur. <br /> | 
| <a href="mlwinhelp.md"><strong>MLWinHelp</strong></a><br /> | démarre Windows aide (Winhelp.exe) et transmet des données supplémentaires qui indiquent la nature de l’aide demandée par l’application.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-openregstream"><strong>OpenRegStream</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-openregstream"><strong>OpenRegStream</strong></a> peut être modifié ou non disponible. Au lieu de cela, utilisez <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstream2a"><strong>SHOpenRegStream2</strong></a> ou <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstreama"><strong>SHOpenRegStream</strong></a>.<br /> | 
| <a href="outputdebugstringwrapw.md"><strong>OutputDebugStringWrapW</strong></a><br /> | Envoie une chaîne Unicode au débogueur pour l’affichage.<br /><blockquote>[!Note]<br /><a href="outputdebugstringwrapw.md"><strong>OutputDebugStringWrapW</strong></a> est un wrapper pour la fonction <strong>OutputDebugStringW</strong> . Pour plus d’informations sur les remarques d’utilisation, consultez la page <a href="/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw"><strong>OutputDebugString</strong></a> .</blockquote><br /> | 
| <a href="parsefield.md"><strong>ParseField</strong></a><br /> | Lit une ligne à partir de Setup. inf et extrait le champ spécifié de la chaîne. <br /> | 
| <a href="passportwizardrundll.md"><strong>PassportWizardRunDll</strong></a><br /> | Lance l’Assistant Passport lorsqu’il est utilisé avec Rundll32.exe.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathcleanupspec"><strong>PathCleanupSpec</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathcleanupspec"><strong>PathCleanupSpec</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathgetshortpath"><strong>PathGetShortPath</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathgetshortpath"><strong>PathGetShortPath</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathisexe"><strong>PathIsExe</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathisexe"><strong>PathIsExe</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shlobj/nf-shlobj-pathisslowa"><strong>PathIsSlow</strong></a><br /> | <a href="/windows/desktop/api/Shlobj/nf-shlobj-pathisslowa"><strong>PathIsSlow</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shlobj/nf-shlobj-pathprocesscommand"><strong>PathProcessCommand</strong></a><br /> | Action déconseillée. Traite une chaîne qui contient une ligne de commande et génère une chaîne entre guillemets appropriée, avec les arguments attachés, si nécessaire.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathresolve"><strong>PathResolve</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathresolve"><strong>PathResolve</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shlobj/nf-shlobj-peruserinit"><strong>PerUserInit</strong></a><br /> | Crée <a href="manage.md">Mes documents</a> et d’autres dossiers spéciaux, les initialise en fonction des besoins et crée l’élément de menu <strong>Envoyer au</strong> raccourci pour mes documents. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb776773(v=vs.85)"><strong>PFNASYNCICONTASKCALLBACK</strong></a><br /> | Définit le prototype pour la fonction de rappel utilisée par <a href="/previous-versions/windows/desktop/legacy/bb762218(v=vs.85)"><strong>SHMapIDListToImageListIndexAsync</strong></a>. <br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pickicondlg"><strong>PickIconDlg</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pickicondlg"><strong>PickIconDlg</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-readcabinetstate"><strong>ReadCabinetState</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-readcabinetstate"><strong>ReadCabinetState</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-realdrivetype"><strong>RealDriveType</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-realdrivetype"><strong>RealDriveType</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-restartdialog"><strong>RestartDialog</strong></a><br /> | Affiche une boîte de dialogue qui invite l’utilisateur à redémarrer Windows. Quand l’utilisateur clique sur le bouton, la fonction appelle <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a> pour tenter de redémarrer Windows.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-restartdialogex"><strong>RestartDialogEx</strong></a><br /> | Affiche une boîte de dialogue qui demande à l’utilisateur de redémarrer Windows. Quand l’utilisateur clique sur le bouton, la fonction appelle <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a> pour tenter de redémarrer Windows.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddfrompropsheetextarray"><strong>SHAddFromPropSheetExtArray</strong></a><br /> | Ajoute des pages à un tableau d’extensions de feuille de propriétés créé par <a href="/windows/desktop/api/Shlobj/nf-shlobj-shcreatepropsheetextarray"><strong>SHCreatePropSheetExtArray</strong></a>.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shalloc"><strong>SHAlloc</strong></a><br /> | Alloue de la mémoire à partir du tas du shell.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shallocshared"><strong>SHAllocShared</strong></a><br /> | <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shallocshared"><strong>SHAllocShared</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shansitoansi"><strong>SHAnsiToAnsi</strong></a><br /> | Copie une chaîne ANSI.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shansitounicode"><strong>SHAnsiToUnicode</strong></a><br /> | Convertit une chaîne de la page de codes ANSI en page de codes Unicode.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangedwordasidlist"><strong>SHChangeDWORDAsIDList</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangedwordasidlist"><strong>SHChangeDWORDAsIDList</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj/ns-shlobj-shchangeproductkeyasidlist"><strong>SHChangeProductKeyAsIDList</strong></a><br /> | 
| <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangeupdateimageidlist"><strong>SHChangeUpdateImageIDList</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangeupdateimageidlist"><strong>SHChangeUpdateImageIDList</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shclonespecialidlist"><strong>SHCloneSpecialIDList</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shclonespecialidlist"><strong>SHCloneSpecialIDList</strong></a> peut être modifié ou non disponible. Utilisez plutôt <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation"><strong>SHGetSpecialFolderLocation</strong></a>.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shclsidfromstring"><strong>SHCLSIDFromString</strong></a><br /> | Prend la forme de chaîne d’un identificateur de classe (CLSID) et crée le CLSID correspondant.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcocreateinstance"><strong>SHCoCreateInstance</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcocreateinstance"><strong>SHCoCreateInstance</strong></a> peut être modifié ou non disponible. Utilisez à la place <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance"><strong>CoCreateInstance</strong></a>.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedirectory"><strong>SHCreateDirectory</strong></a><br /> | Crée un dossier de système de fichiers.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedirectoryexa"><strong>SHCreateDirectoryEx</strong></a><br /> | Crée un dossier de système de fichiers, avec des attributs de sécurité facultatifs.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatefileextracticonw"><strong>SHCreateFileExtractIcon</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatefileextracticonw"><strong>SHCreateFileExtractIcon</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shcreateprocessasuserw"><strong>SHCreateProcessAsUserW</strong></a><br /> | Crée un nouveau processus en mode utilisateur et son thread principal pour exécuter un fichier exécutable spécifié. <br /> | 
| <a href="/windows/desktop/api/Shellapi/ns-shellapi-shcreateprocessinfow"><strong>SHCREATEPROCESSINFOW</strong></a><br /> | Contient les informations requises par <a href="/windows/desktop/api/Shellapi/nf-shellapi-shcreateprocessasuserw"><strong>SHCreateProcessAsUserW</strong></a> pour créer un processus. <br /> | 
| <a href="/windows/desktop/api/Shlobj/nf-shlobj-shcreatepropsheetextarray"><strong>SHCreatePropSheetExtArray</strong></a><br /> | <a href="/windows/desktop/api/Shlobj/nf-shlobj-shcreatepropsheetextarray"><strong>SHCreatePropSheetExtArray</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shlobj/nf-shlobj-shcreatequerycancelautoplaymoniker"><strong>SHCreateQueryCancelAutoPlayMoniker</strong></a><br /> | Action déconseillée. Crée un moniker de la classe <strong>QueryCancelAutoPlay</strong> , qui peut ensuite être utilisé pour inscrire le gestionnaire <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iquerycancelautoplay"><strong>IQueryCancelAutoPlay</strong></a> dans la table ROT (Running Object Table).<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatestdenumfmtetc"><strong>SHCreateStdEnumFmtEtc</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatestdenumfmtetc"><strong>SHCreateStdEnumFmtEtc</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatestreamonfilea"><strong>SHCreateStreamOnFile</strong></a><br /> | <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatestreamonfilea"><strong>SHCreateStreamOnFile</strong></a> peut être modifié ou non disponible. Utilisez plutôt <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatestreamonfileex"><strong>SHCreateStreamOnFileEx</strong></a>.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdestroypropsheetextarray"><strong>SHDestroyPropSheetExtArray</strong></a><br /> | Libère des gestionnaires de feuille de propriétés pointés vers un tableau créé par <a href="/windows/desktop/api/Shlobj/nf-shlobj-shcreatepropsheetextarray"><strong>SHCreatePropSheetExtArray</strong></a>.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shell_getcachedimageindex"><strong>Shell_GetCachedImageIndex</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shell_getcachedimageindex"><strong>Shell_GetCachedImageIndex</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shell_getimagelists"><strong>Shell_GetImageLists</strong></a><br /> | Récupère des listes d’images système pour les grandes et les petites icônes.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shell_mergemenus"><strong>Shell_MergeMenus</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shell_mergemenus"><strong>Shell_MergeMenus</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellmessageboxa"><strong>ShellMessageBox</strong></a><br /> | <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellmessageboxa"><strong>ShellMessageBox</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="shextracticonsw.md"><strong>SHExtractIconsW</strong></a><br /> | Crée un tableau de handles pour les icônes extraites d’un fichier spécifié.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shfind_initmenupopup"><strong>SHFind_InitMenuPopup</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shfind_initmenupopup"><strong>SHFind_InitMenuPopup</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shfindfiles"><strong>SHFindFiles</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shfindfiles"><strong>SHFindFiles</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb762167(v=vs.85)"><strong>SHFlushClipboard</strong></a><br /> | Exécute la séquence d’arrêt du presse-papiers. Elle libère également le pointeur <a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>IDataObject</strong></a> placé dans le presse-papiers par la fonction <a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard"><strong>OleSetClipboard</strong></a> . <br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shflushsfcache"><strong>SHFlushSFCache</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shflushsfcache"><strong>SHFlushSFCache</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a><br /> | <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shformatdrive"><strong>SHFormatDrive</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shformatdrive"><strong>SHFormatDrive</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shfree"><strong>SHFree</strong></a><br /> | Libère la mémoire allouée par <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shalloc"><strong>SHAlloc</strong></a>. <br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shfreeshared"><strong>SHFreeShared</strong></a><br /> | <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shfreeshared"><strong>SHFreeShared</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetattributesfromdataobject"><strong>SHGetAttributesFromDataObject</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetattributesfromdataobject"><strong>SHGetAttributesFromDataObject</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation"><strong>SHGetFolderLocation</strong></a><br /> | Action déconseillée. Récupère le chemin d’accès d’un dossier sous la forme d’une structure <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha"><strong>SHGetFolderPath</strong></a><br /> | Action déconseillée. Obtient le chemin d’accès d’un dossier identifié par une valeur <a href="csidl.md"><strong>CSIDL</strong></a> . <br /><blockquote>[!Note]<br />à partir de Windows Vista, cette fonction est simplement un wrapper pour <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>SHGetKnownFolderPath</strong></a>. La valeur CSIDL est convertie en <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a> associée, puis <strong>SHGetKnownFolderPath</strong> est appelée. Les nouvelles applications doivent utiliser le système de dossiers connu plutôt que l’ancien système CSIDL, qui est pris en charge uniquement pour la compatibilité descendante.</blockquote><br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpathandsubdira"><strong>SHGetFolderPathAndSubDir</strong></a><br /> | Obtient le chemin d’accès d’un dossier et ajoute un chemin d’accès au sous-dossier fourni par l’utilisateur.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shgetinversecmap"><strong>SHGetInverseCMAP</strong></a><br /> | Récupère le mappage de table de couleur inverse pour la palette de demi-teintes.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetmalloc"><strong>SHGetMalloc</strong></a><br /> | Récupère un pointeur vers l’interface <a href="/windows/desktop/api/objidl/nn-objidl-imalloc"><strong>IMalloc</strong></a> de l’interpréteur de commandes. <br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetrealidl"><strong>SHGetRealIDL</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetrealidl"><strong>SHGetRealIDL</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings"><strong>SHGetSetFolderCustomSettings</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings"><strong>SHGetSetFolderCustomSettings</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>SHGetSetSettings</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>SHGetSetSettings</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb762202(v=vs.85)"><strong>SHGetShellStyleHInstance</strong></a><br /> | Action déconseillée. Tente d’obtenir un handle vers le fichier Shellstyle.dll.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation"><strong>SHGetSpecialFolderLocation</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation"><strong>SHGetSpecialFolderLocation</strong></a> n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation"><strong>SHGetFolderLocation</strong></a>.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha"><strong>SHGetSpecialFolderPath</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha"><strong>SHGetSpecialFolderPath</strong></a> n’est pas pris en charge. Utilisez plutôt <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha"><strong>ShGetFolderPath</strong></a>.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shgetviewstatepropertybag"><strong>SHGetViewStatePropertyBag</strong></a><br /> | <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shgetviewstatepropertybag"><strong>SHGetViewStatePropertyBag</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shhandleupdateimage"><strong>SHHandleUpdateImage</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shhandleupdateimage"><strong>SHHandleUpdateImage</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shilcreatefrompath"><strong>SHILCreateFromPath</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shilcreatefrompath"><strong>SHILCreateFromPath</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda"><strong>SHInvokePrinterCommand</strong></a><br /> | Exécute une commande sur un objet Printer. <br /><blockquote>[!Note]<br />cette fonction a été déconseillée à partir de Windows Vista. Il est recommandé, à la place, d’appeler des verbes sur des imprimantes via <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a> ou <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a>.</blockquote><br /> | 
| <a href="/windows/desktop/shell/common-file-dialog"><strong>SHIsChildOrSelf</strong></a><br /> | Compare si une fenêtre est égale à, un enfant ou un descendant de, une deuxième fenêtre.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shlimitinputedit"><strong>SHLimitInputEdit</strong></a><br /> | Définit des limites sur les caractères valides pour un contrôle d’édition.<br /> | 
| <a href="/windows/desktop/api/Shlobj/nf-shlobj-shloadole"><strong>SHLoadOLE</strong></a><br /> | Action déconseillée. Fourni pour la compatibilité ascendante.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shlockshared"><strong>SHLockShared</strong></a><br /> | <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shlockshared"><strong>SHLockShared</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb762218(v=vs.85)"><strong>SHMapIDListToImageListIndexAsync</strong></a><br /> | Récupère un index dans la liste d’images système lorsqu’un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> et un <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> qu’il contient sont fournis. Cette fonction obtient également l’icône finale du rappel, si nécessaire.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shmappidltosystemimagelistindex"><strong>SHMapPIDLToSystemImageListIndex</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shmappidltosystemimagelistindex"><strong>SHMapPIDLToSystemImageListIndex</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shmessageboxchecka"><strong>SHMessageBoxCheck</strong></a><br /> | <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shmessageboxchecka"><strong>SHMessageBoxCheck</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shobjectproperties"><strong>SHObjectProperties</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shobjectproperties"><strong>SHObjectProperties</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shlobj/nf-shlobj-shopenpropsheeta"><strong>SHOpenPropSheet</strong></a><br /> | <a href="/windows/desktop/api/Shlobj/nf-shlobj-shopenpropsheeta"><strong>SHOpenPropSheet</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstreama"><strong>SHOpenRegStream</strong></a><br /> | Action déconseillée. Ouvre une valeur de Registre et fournit un flux qui peut être utilisé pour lire ou écrire dans la valeur. <br /><blockquote>[!Note]<br />Cette fonction a été remplacée par <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstream2a"><strong>SHOpenRegStream2</strong></a>. Nous vous recommandons d’utiliser <strong>SHOpenRegStream2</strong> à tout moment.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetboolvaluefromhkcuhklm"><strong>SHRegGetBoolValueFromHKCUHKLM</strong></a><br /> | Évalue une valeur de clé de Registre et retourne une valeur booléenne qui indique si la valeur existe et si l’État attendu correspond à l’état réel. Cette fonction vérifie d’abord HKEY_CURRENT_USER pour les informations demandées dans la sous-clé spécifiée. Si les informations n’existent pas dans la sous-arborescence HKEY_CURRENT_USER, la sous-arborescence de HKEY_LOCAL_MACHINE est vérifiée pour obtenir les mêmes informations. <br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea"><strong>SHRegGetValue</strong></a><br /> | Récupère une valeur de registre.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluefromhkcuhklm"><strong>SHRegGetValueFromHKCUHKLM</strong></a><br /> | Obtient des informations spécifiées à partir du Registre. Cette fonction vérifie HKEY_CURRENT_USER pour les informations demandées dans la sous-clé spécifiée. Si les informations n’existent pas dans la sous-arborescence HKEY_CURRENT_USER, la fonction vérifie la HKEY_LOCAL_MACHINE sous-arborescence pour obtenir les mêmes informations. <br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shreplacefrompropsheetextarray"><strong>SHReplaceFromPropSheetExtArray</strong></a><br /> | Demande à chaque feuille de propriétés d’un tableau d’extensions de feuille de propriétés de remplacer des pages. Chaque page est autorisée jusqu’à un seul remplacement.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shrestricted"><strong>SHRestricted</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shrestricted"><strong>SHRestricted</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha"><strong>SHSetFolderPath</strong></a><br /> | Action déconseillée. Assigne un nouveau chemin d’accès à un dossier système identifié par son CSIDL.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shsendmessagebroadcasta"><strong>SHSendMessageBroadcast</strong></a><br /> | Envoie un message à toutes les fenêtres de niveau supérieur du système.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message"><strong>SHShellFolderView_Message</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message"><strong>SHShellFolderView_Message</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsimpleidlistfrompath"><strong>SHSimpleIDListFromPath</strong></a><br /> | Action déconseillée. Retourne un pointeur vers une structure <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> lorsqu’un chemin d’accès lui est passé.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shstartnetconnectiondialoga"><strong>SHStartNetConnectionDialog</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shstartnetconnectiondialoga"><strong>SHStartNetConnectionDialog</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstripmneumonica"><strong>SHStripMneumonic</strong></a><br /> | Supprime le marqueur mnémonique d’une chaîne.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shunicodetoansi"><strong>SHUnicodeToAnsi</strong></a><br /> | Convertit une chaîne de la page de codes Unicode en page de codes ANSI.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shunicodetounicode"><strong>SHUnicodeToUnicode</strong></a><br /> | Copie une chaîne Unicode.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shunlockshared"><strong>SHUnlockShared</strong></a><br /> | <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shunlockshared"><strong>SHUnlockShared</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shvalidateunc"><strong>SHValidateUNC</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shvalidateunc"><strong>SHValidateUNC</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-signalfileopen"><strong>SignalFileOpen</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-signalfileopen"><strong>SignalFileOpen</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-stopwatchflush"><strong>StopWatchFlush</strong></a><br /> | <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-stopwatchflush"><strong>StopWatchFlush</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-stopwatchmode"><strong>StopWatchMode</strong></a><br /> | <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-stopwatchmode"><strong>StopWatchMode</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/win32/api/shlobj/nf-shlobj-iadesktopp2-updatealldesktopsubscriptions"><strong>UpdateAllDesktopSubscriptions</strong></a><br /> | Action déconseillée. Énumère les URL de tous les composants de bureau, puis teste pour voir s’ils sont abonnés. S’ils sont abonnés à, les abonnements sont remis.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlfixupw"><strong>UrlFixupW</strong></a><br /> | <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlfixupw"><strong>UrlFixupW</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-whichplatform"><strong>WhichPlatform</strong></a><br /> | <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-whichplatform"><strong>WhichPlatform</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-win32deletefile"><strong>Win32DeleteFile</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-win32deletefile"><strong>Win32DeleteFile</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="wowshellexecute.md"><strong>WOWShellExecute</strong></a><br /> | Effectue une opération sur un fichier spécifié. <a href="wowshellexecute.md"><strong>WOWShellExecute</strong></a> existe uniquement pour une utilisation avec la Machine DOS virtuelle Microsoft Windows NT (Ntvdm.exe), qui permet l’exécution du système d’exploitation sur disque (DOS) et du logiciel 16 bits sur un système Windows, et ne doit pas être utilisée par une autre personne. Utilisez à la place <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a> .<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-writecabinetstate"><strong>WriteCabinetState</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-writecabinetstate"><strong>WriteCabinetState</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="shlwapi-wrappers.md"><strong>Fonctions de wrapper SHLWAPI</strong></a><br /> | les tables de ce document contiennent des fonctions de wrapper de Shlwapi.dll qui fournissent des fonctionnalités Unicode limitées à Windows 95, Windows 98 et Windows millennium edition (Windows Me).<br /> | 
| <a href="/windows/desktop/shell/samples-namespacetreecontrol"><strong>FileOpen</strong></a><br /> | Prend en charge la boîte de dialogue <strong>ouvrir un fichier</strong> commun.<br /> | 
| <a href="/windows/desktop/shell/samples-nondefaultdropmenuverb"><strong>Types</strong></a><br /> | crée la <strong>page Types de fichiers</strong> de la feuille de propriétés options des <strong>dossiers</strong> affichée par l’utilisateur en cliquant sur <strong>Options des dossiers</strong> dans le menu <strong>outils</strong> de l’explorateur de Windows. <br /> | 
| <a href="/windows/desktop/shell/functions"><strong>FolderItemsFDF</strong></a><br /> | Représente un dossier shell et tous ses enfants.<br /> | 
| <a href="/windows/desktop/shell/known-folders"><strong>ImageRecompress</strong></a><br /> | Utilisé pour recompresser une image.<br /> | 
| <a href="/windows/desktop/shell/profiles-directory"><strong>MenuBand</strong></a><br /> | Prend en charge les bandes de menus Shell.<br /> | 
| <a href="/windows/desktop/shell/mandatory-user-profiles"><strong>MenuBandSite</strong></a><br /> | Obtient ou définit les informations de site de la bande de menu.<br /> | 
| <a href="/windows/desktop/shell/roaming-user-profiles"><strong>NewMenu</strong></a><br /> | Crée un menu <strong>contextuel pour</strong> un élément de Shell.<br /> | 
| <a href="/windows/desktop/shell/user-profiles"><strong>ShellFldSetExt</strong></a><br /> | Crée une boîte de dialogue <strong>Options des dossiers</strong> . <br /> | 
| <a href="/windows/desktop/shell/local-user-profiles"><strong>ShellFolderBand</strong></a><br /> | Gère les bandes de dossiers. La barre lancement rapide est un exemple de bande de dossiers.<br /> | 
| <a href="/windows/desktop/shell/context-menu"><strong>Magasin d’images de l’interpréteur de commandes</strong></a><br /> | Crée une instance d’un objet <a href="/windows/desktop/api/shlobj/nn-shlobj-ishellimagestore"><strong>IShellImageStore</strong></a> .<br /> | 
| <a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-ibrowserservice"><strong>IBrowserService</strong></a><br /> | Action déconseillée. Les méthodes exposées par cette interface sont analogues aux méthodes protégées virtuelles en héritage C++ normal. La hiérarchie d’héritage des objets s’étend sur plusieurs dll. La hiérarchie est constituée d’une classe de base et de plusieurs classes dérivées qui correspondent aux contrôles, y compris CLSID_WebBrowser et le Bureau de l’utilisateur. Les objets qui ne sont pas dans la hiérarchie ne doivent pas implémenter cette interface ou utiliser la plupart de ses méthodes.<br /> | 
| <a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-ibrowserservice2"><strong>IBrowserService2</strong></a><br /> | Action déconseillée. <a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-ibrowserservice2"><strong>IBrowserService2</strong></a> étend <a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-ibrowserservice"><strong>IBrowserService</strong></a>. Les méthodes exposées par cette interface sont analogues aux méthodes protégées virtuelles en héritage C++ normal. La hiérarchie d’héritage des objets s’étend sur plusieurs dll. La hiérarchie est constituée d’une classe de base et de plusieurs classes dérivées qui correspondent aux contrôles, y compris CLSID_WebBrowser et le Bureau de l’utilisateur. Les objets qui ne sont pas dans la hiérarchie ne doivent pas implémenter cette interface ou utiliser la plupart de ses méthodes.<br /> | 
| <a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-ibrowserservice3"><strong>IBrowserService3</strong></a><br /> | Action déconseillée. Les méthodes exposées par cette interface sont analogues aux méthodes protégées virtuelles en héritage C++ normal. La hiérarchie d’héritage des objets s’étend sur plusieurs dll. La hiérarchie est constituée d’une classe de base et de plusieurs classes dérivées qui correspondent aux contrôles, y compris CLSID_WebBrowser et le Bureau de l’utilisateur. Les objets qui ne sont pas dans la hiérarchie ne doivent pas implémenter cette interface, ni utiliser la plupart de ses méthodes.<br /> | 
| <a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-ibrowserservice4"><strong>IBrowserService4</strong></a><br /> | Action déconseillée.<br /> | 
| <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icdburnext"><strong>ICDBurnExt</strong></a><br /> | <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icdburnext"><strong>ICDBurnExt</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider"><strong>IColumnProvider</strong></a><br /> | expose des méthodes qui permettent d’ajouter des colonnes personnalisées dans le mode détails de l’explorateur de Windows. <br /><blockquote>[!Note]<br />la prise en charge de <a href="/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider"><strong>IColumnProvider</strong></a> a été supprimée à partir de Windows Vista. le système de propriétés de Windows est utilisé à la place. consultez <a href="/windows/desktop/properties/windows-properties-system">Windows système de propriétés</a> pour obtenir des documents conceptuels expliquant l’utilisation du nouveau système.</blockquote><br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite"><strong>IContextMenuSite</strong></a><br /> | Implémenté par l’affichage des dossiers par défaut créé à l’aide de <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a>. Une implémentation de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite"><strong>IContextMenuSite</strong></a> prend en charge <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu"><strong>IContextMenu :: QueryContextMenu</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu :: commande InvokeCommand</strong></a>et <a href="/windows/desktop/api/winuser/nf-winuser-trackpopupmenu"><strong>TrackPopupMenu</strong></a> et tout transfert de messages nécessaire pour cette fonction. <strong>IContextMenuSite</strong> met également à jour également la barre d’État.<br /> | 
| <a href="/windows/desktop/api/shlobj/nn-shlobj-idefviewframe"><strong>IDefViewFrame</strong></a><br /> | Utilisé uniquement pour ses fonctionnalités <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> . Elle n’a pas de méthode propre.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb762074(v=vs.85)"><strong>IDefViewID</strong></a><br /> | <a href="/previous-versions/windows/desktop/legacy/bb762074(v=vs.85)"><strong>IDefViewID</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb762072(v=vs.85)"><strong>IDefViewSafety</strong></a><br /> | Action déconseillée. Expose une méthode qui détermine le paramètre de zone de contenu Web d’une page avant l’accès à la page.<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband"><strong>IDeskBand</strong></a><br /> | Utilisé pour obtenir des informations sur un objet de bande.<br /><blockquote>[!Important]<br />vous devez utiliser les <a href="taskbar-extensions.md">barres d’outils miniatures</a> dans un nouveau développement à la place des bandes de bureau, qui ne sont pas prises en charge à partir de Windows 7.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2"><strong>IDeskBand2</strong></a><br /> | Expose des méthodes pour activer et interroger des effets translucidité dans un objet Deskband.<br /><blockquote>[!Important]<br />vous devez utiliser les <a href="taskbar-extensions.md">barres d’outils miniatures</a> dans un nouveau développement à la place des bandes de bureau, qui ne sont pas prises en charge à partir de Windows 7.</blockquote><br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskbandinfo"><strong>IDeskBandInfo</strong></a><br /> | Expose une méthode pour obtenir la bande passante par défaut de la bande de bureau.<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskbar"><strong>IDeskBar</strong></a><br /> | Expose des méthodes qui permettent la manipulation de la barre de bureau.<br /> | 
| <a href="/windows/desktop/api/shlobj/nn-shlobj-idocviewsite"><strong>IDocViewSite</strong></a><br /> | Utilisé comme objet de site par l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> .<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb762022(v=vs.85)"><strong>IDVGetEnum</strong></a><br /> | Expose des méthodes qui permettent à l’objet de vue de dossier système de fournir un autre objet avec une énumération d’éléments, sans le deuxième objet qui exécute une énumération redondante elle-même.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb761957(v=vs.85)"><strong>IEnumSyncItems</strong></a><br /> | Expose des méthodes qui fournissent l’énumération de tous les éléments dans un calendrier de synchronisation.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb761937(v=vs.85)"><strong>IEnumSyncSchedules</strong></a><br /> | Fournit une énumération de toutes les planifications de synchronisation.<br /> | 
| <a href="ienumuseridentity.md"><strong>IEnumUserIdentity</strong></a><br /> | <a href="ienumuseridentity.md"><strong>IEnumUserIdentity</strong></a> n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt <a href="fastuserswitching.md">des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance</a>.<br /> | 
| <a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-iexpdispsupport"><strong>IExpDispSupport</strong></a><br /> | Action déconseillée. Expose des méthodes qui permettent la récupération de propriétés, la traduction d’accélérateurs de clavier et la détermination d’un point de connexion pour certains événements.<br /> | 
| <a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-iexpdispsupportxp"><strong>IExpDispSupportXP</strong></a><br /> | Action déconseillée. Expose des méthodes qui permettent la récupération de propriétés, la traduction d’accélérateurs de clavier et la détermination d’un point de connexion pour certains événements.<br /> | 
| <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderbandpriv"><strong>IFolderBandPriv</strong></a><br /> | <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderbandpriv"><strong>IFolderBandPriv</strong></a> peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.<br /> | 
| <a href="iidentitychangenotify.md"><strong>IIdentityChangeNotify</strong></a><br /> | Action déconseillée. Fournit une notification des modifications apportées aux identités des utilisateurs sur le système, ainsi que les demandes des utilisateurs pour changer l’identité de l’utilisateur actuel.<br /> | 
| <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iinsertitem"><strong>IInsertItem</strong></a><br /> | <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iinsertitem"><strong>IInsertItem</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenuband"><strong>IMenuBand</strong></a><br /> | Expose des méthodes qui permettent à un objet COM (Component Object Model) de recevoir et de traduire des messages appropriés.<br /> | 
| <a href="/windows/desktop/shell/syncmgr-using-from-a-program"><strong>IPassportClientServices</strong></a><br /> | l’interface <a href="/windows/desktop/shell/syncmgr-using-from-a-program"><strong>IPassportClientServices</strong></a> expose une méthode pour déterminer si un ID Live Windows existe.<br /> | 
| <a href="/windows/desktop/shell/thumbnail-providers"><strong>IPassportWizard</strong></a><br /> | expose une méthode qui appelle l’assistant Passport Windows XP. <br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iregtreeitem"><strong>IRegTreeItem</strong></a><br /> | Expose des méthodes qui récupèrent et définissent l’état des éléments dans un contrôle d’arborescence dont l’indicateur de <a href="/windows/desktop/Controls/tree-view-control-window-styles"><strong>styles de fenêtre de contrôle d’arborescence</strong></a> est défini.<br /> | 
| <a href="/windows/desktop/shell/how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"><strong>IShellExecuteHook</strong></a><br /> | <blockquote>[!Note]<br />les hooks d’exécution de Shell sont déconseillés à partir de Windows Vista.</blockquote><br /> Expose une méthode qui étend le comportement des fonctions <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a> ou <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> . elle est généralement implémentée par les sous-systèmes qui exposent les noms des objets que l’utilisateur peut spécifier dans la boîte de dialogue <strong>exécuter</strong> après avoir cliqué sur le bouton Windows <strong>démarrer</strong> .<br /> | 
| <a href="/windows/desktop/api/shlobj/nn-shlobj-ishellfolderband"><strong>IShellFolderBand</strong></a><br /> | <a href="/windows/desktop/api/shlobj/nn-shlobj-ishellfolderband"><strong>IShellFolderBand</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellfolderview"><strong>IShellFolderView</strong></a><br /> | Expose des méthodes qui manipulent des vues de dossiers de Shell.<br /> | 
| <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlaymanager"><strong>IShellIconOverlayManager</strong></a><br /> | <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlaymanager"><strong>IShellIconOverlayManager</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata"><strong>IShellImageData</strong></a><br /> | Expose des méthodes et des propriétés qui affichent, manipulent et décrivent des données image.<br /> | 
| <a href="/windows/desktop/api/shlobj/nn-shlobj-ishellimagestore"><strong>IShellImageStore</strong></a><br /> | Action déconseillée. Expose des méthodes qui manipulent le cache d’images.<br /> | 
| <a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-ishellservice"><strong>IShellService</strong></a><br /> | Action déconseillée. <a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-ishellservice"><strong>IShellService</strong></a> expose une méthode qui déclare la propriété lorsqu’un composant de service implémentant une certaine interface est partagé entre plusieurs clients, par exemple Windows Internet explorer et Windows explorer. <br /> | 
| <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelltaskscheduler"><strong>IShellTaskScheduler</strong></a><br /> | <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelltaskscheduler"><strong>IShellTaskScheduler</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/bb774852(v=vs.85)"><strong>IShellTaskScheduler2</strong></a><br /> | Étend les fonctionnalités de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelltaskscheduler"><strong>IShellTaskScheduler</strong></a> en héritant de toutes ses méthodes, en fournissant la possibilité de placer une tâche dans la file d’attente avec une référence à d’autres tâches de sa priorité, et d’ajouter une méthode pour réinitialiser la priorité d’une tâche.<br /> | 
| <a href="/previous-versions/windows/desktop/isync-schedule/bb774693(v=vs.85)"><strong>ISyncSchedule</strong></a><br /> | Expose les méthodes associées à une planification de synchronisation individuelle.<br /> | 
| <a href="/previous-versions/windows/desktop/isync-schedule-mgr/bb774672(v=vs.85)"><strong>ISyncScheduleMgr</strong></a><br /> | Expose des méthodes pour configurer et contrôler un planificateur de synchronisation pour la gestion de la synchronisation.<br /> | 
| <a href="/windows/desktop/api/shlobj/nn-shlobj-ithumbnailcapture"><strong>IThumbnailCapture</strong></a><br /> | Expose une méthode qui obtient une représentation miniature d’un papier peint HTML. <br /><blockquote>[!Note]<br />cette interface est déconseillée à partir de Windows 7. La fonctionnalité prise en charge n’est plus présente dans Windows.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-itravelentry"><strong>ITravelEntry</strong></a><br /> | Action déconseillée. Expose des méthodes pour identifier, appeler et mettre à jour un élément individuel dans l’historique des déplacements du navigateur.<br /> | 
| <a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-itravellog"><strong>ITravelLog</strong></a><br /> | Action déconseillée. Expose des méthodes qui maintiennent et manipulent un enregistrement de voyages dans le navigateur.<br /> | 
| <a href="iuseridentity.md"><strong>IUserIdentity</strong></a><br /> | <a href="iuseridentity.md"><strong>IUserIdentity</strong></a> n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt <a href="fastuserswitching.md">des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance</a>.<br /> | 
| <a href="iuseridentity2.md"><strong>IUserIdentity2</strong></a><br /> | <a href="iuseridentity2.md"><strong>IUserIdentity2</strong></a> n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt <a href="fastuserswitching.md">des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance</a>.<br /> | 
| <a href="iuseridentitymanager.md"><strong>IUserIdentityManager</strong></a><br /> | <a href="iuseridentitymanager.md"><strong>IUserIdentityManager</strong></a> n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt <a href="fastuserswitching.md">des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance</a>.<br /> | 
| <a href="sfvm-diddragdrop.md"><strong>SFVM_DIDDRAGDROP</strong></a><br /> | <a href="sfvm-diddragdrop.md"><strong>SFVM_DIDDRAGDROP</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="sfvm-getdetailsof.md"><strong>SFVM_GETDETAILSOF</strong></a><br /> | <a href="sfvm-getdetailsof.md"><strong>SFVM_GETDETAILSOF</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="sfvm-getpane.md"><strong>SFVM_GETPANE</strong></a><br /> | <a href="sfvm-getpane.md"><strong>SFVM_GETPANE</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="sfvm-getzone.md"><strong>SFVM_GETZONE</strong></a><br /> | Permet à l’objet de rappel de fournir des informations sur la zone Internet. Utilisé par <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb"><strong>IShellFolderViewCB :: MessageSFVCB</strong></a>.<br /> | 
| <a href="sfvm-queryfsnotify.md"><strong>SFVM_QUERYFSNOTIFY</strong></a><br /> | <a href="sfvm-queryfsnotify.md"><strong>SFVM_QUERYFSNOTIFY</strong></a> peut être modifié ou non disponible.<br /> | 
| <a href="sfvm-setisfv.md"><strong>SFVM_SETISFV</strong></a><br /> | Avertit l’objet de rappel du site de conteneur. Utilisé uniquement quand <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)"><strong>IObjectWithSite :: SetSite</strong></a> n’est pas pris en charge et <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>SHCreateShellFolderViewEx</strong></a> est utilisé. Utilisé par <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb"><strong>IShellFolderViewCB :: MessageSFVCB</strong></a>.<br /> | 
| <a href="sfvm-thisidlist.md"><strong>SFVM_THISIDLIST</strong></a><br /> | <a href="sfvm-thisidlist.md"><strong>SFVM_THISIDLIST</strong></a> peut être modifié ou non disponible.<br /> | 




 

 

 
