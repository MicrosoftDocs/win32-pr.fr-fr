---
title: PROPSHEETPAGE, structure (Prsht.h)
description: Définit une page dans une feuille de propriétés.
keywords:
- PROPSHEETPAGE, structure Windows, contrôles
topic_type:
- apiref
api_name:
- PROPSHEETPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/23/2021
ms.openlocfilehash: 78e1d1e4e6b4b2067083443bdb5dc4db5df59558
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519425"
---
# <a name="propsheetpage-structure"></a>PROPSHEETPAGE, structure

Définit une page dans une feuille de propriétés.

## <a name="syntax"></a>Syntaxe

```cpp
typedef struct {
    DWORD      dwSize;
    DWORD      dwFlags;
    HINSTANCE  hInstance;
    union {
        LPCSTR                 pszTemplate;
        PROPSHEETPAGE_RESOURCE pResource;
    };
    union {
        HICON  hIcon;
        LPCSTR pszIcon;
    };
    LPCSTR          pszTitle;
    DLGPROC         pfnDlgProc;
    LPARAM          lParam;
    LPFNPSPCALLBACK pfnCallback;
    UINT            *pcRefParent;
    LPCTSTR         pszHeaderTitle;
    LPCTSTR         pszHeaderSubTitle;
    HANDLE          hActCtx;
    union 
    {
        HBITMAP     hbmHeader;
        LPCSTR      pszbmHeader;
    }
} PROPSHEETPAGE, *LPPROPSHEETPAGE;
```

## <a name="members"></a>Membres

*dwSize nul* 

Type : [DWORD](../winprog/windows-data-types.md)

Taille, en octets, de cette structure.

*dwFlags* 

Type : [DWORD](../winprog/windows-data-types.md)

Indicateurs qui spécifient quelles options utiliser pour créer la page de feuille de propriétés. Ce membre peut être une combinaison des valeurs suivantes.

| Valeur | Signification |
|-------|---------|
| PSP_DEFAULT | Utilise la signification par défaut pour tous les membres de structure. Cet indicateur n’est pas pris en charge lors de l’utilisation de l’Assistant style Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_DLGINDIRECT | Crée la page à partir du modèle de boîte de dialogue en mémoire vers laquelle pointe le membre de *présource* . La fonction [feuille](/windows/win32/api/prsht/nf-prsht-propertysheeta) suppose que le modèle qui est en mémoire n’est pas protégé en écriture. Un modèle en lecture seule lève une exception dans certaines versions de Windows. |
| PSP_HASHELP | Active le bouton **d’aide** de la feuille de propriétés lorsque la page est active. Cet indicateur n’est pas pris en charge lors de l’utilisation de l’Assistant style Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_HIDEHEADER | [Version 5,80](common-control-versions.md) et versions ultérieures. Fait en sorte que la feuille de propriétés de l’Assistant masque la zone d’en-tête lorsque la page est sélectionnée. Si un filigrane a été fourni, il est peint sur le côté gauche de la page. Cet indicateur doit être défini pour les pages d’accueil et de fin, et omis pour les pages intérieures. Cet indicateur n’est pas pris en charge lors de l’utilisation de l’Assistant style Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_PREMATURE | [Version 4,71](common-control-versions.md) ou ultérieure. Provoque la création de la page lors de la création de la feuille de propriétés. Si cet indicateur n’est pas spécifié, la page n’est pas créée tant qu’elle n’est pas sélectionnée la première fois. Cet indicateur n’est pas pris en charge lors de l’utilisation de l’Assistant style Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_RTLREADING | Inverse la direction dans laquelle *pszTitle* est affiché. Les fenêtres normales affichent tout le texte, y compris *pszTitle*, de gauche à droite (LTR). Pour les langues telles que l’hébreu ou l’arabe qui lisent de droite à gauche (RTL), une fenêtre peut être mise en miroir et tout le texte s’affichera à droite. Si PSP_RTLREADING est définie, *pszTitle* lira plutôt RTL dans une fenêtre parente normale et LTR dans une fenêtre parente mise en miroir. |
| PSP_USECALLBACK | Appelle la fonction spécifiée par le membre *pfnCallback* lors de la création ou de la destruction de la page de feuille de propriétés définie par cette structure. |
| PSP_USEFUSIONCONTEXT | [Version 6,0](common-control-versions.md) et versions ultérieures. Utilisez un contexte d’activation. Pour utiliser un contexte d’activation, vous devez définir cet indicateur et assigner le handle de contexte d’activation à *hActCtx*. Consultez les notes. |
| PSP_USEHEADERSUBTITLE | [Version 5,80](common-control-versions.md) ou ultérieure. Affiche la chaîne vers laquelle pointe le membre *pszHeaderSubTitle* en tant que sous-titre de la zone d’en-tête d’une page Wizard97. Pour utiliser cet indicateur, vous devez également définir l’indicateur PSH_WIZARD97 dans le membre *dwFlags* de la structure [PROPSHEETHEADER](pss-propsheetheader.md) associée. L’indicateur PSP_USEHEADERSUBTITLE est ignoré si PSP_HIDEHEADER est défini. Dans les assistants de style Aero, le titre apparaît près du haut de la zone cliente. |
| PSP_USEHEADERTITLE | [Version 5,80](common-control-versions.md) ou ultérieure. Affiche la chaîne pointée par le membre *pszHeaderTitle* comme titre dans l’en-tête d’une page Wizard97 Interior. Vous devez également définir l’indicateur PSH_WIZARD97 dans le membre *dwFlags* de la structure [PROPSHEETHEADER](pss-propsheetheader.md) associée. L’indicateur PSP_USEHEADERTITLE est ignoré si PSP_HIDEHEADER est défini. Cet indicateur n’est pas pris en charge lors de l’utilisation de l’Assistant style Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_USEHICON | Utilise *HICON* comme petite icône sous l’onglet de la page. Cet indicateur n’est pas pris en charge lors de l’utilisation de l’Assistant style Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)).  |
| PSP_USEICONID | Utilise *pszIcon* comme nom de la ressource icône à charger et à utiliser comme petite icône sous l’onglet de la page. Cet indicateur n’est pas pris en charge lors de l’utilisation de l’Assistant style Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_USEREFPARENT | Conserve le décompte de références spécifié par le membre *pcRefParent* pendant la durée de vie de la page de feuille de propriétés créée à partir de cette structure. |
| PSP_USETITLE | Utilise le membre *pszTitle* comme titre de la boîte de dialogue de la feuille de propriétés à la place du titre stocké dans le modèle de boîte de dialogue. Cet indicateur n’est pas pris en charge lors de l’utilisation de l’Assistant style Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |

*hInstance* 

Type : [HINSTANCE](../winprog/windows-data-types.md)

Handle de l’instance à partir de laquelle charger une ressource d’icône ou de chaîne. Si le membre *pszIcon*, *pszTitle*, *pszHeaderTitle* ou *PszHeaderSubTitle* identifie une ressource à charger, *HINSTANCE* doit être spécifié.

*pszTemplate* 

Type : [LPCSTR](../winprog/windows-data-types.md)

Modèle de boîte de dialogue à utiliser pour créer la page. Ce membre peut spécifier l’identificateur de ressource du modèle ou l’adresse d’une chaîne qui spécifie le nom du modèle. Si l’indicateur PSP_DLGINDIRECT dans le membre *dwFlags* est défini, *pszTemplate* est ignoré. Ce membre est déclaré en tant qu’Union avec la *présource*.

*Préversion* 

Type : **LPCDLGTEMPLATE**

Pointeur vers un modèle de boîte de dialogue en mémoire. La fonction [feuille](/windows/win32/api/prsht/nf-prsht-propertysheeta) suppose que le modèle n’est pas protégé en écriture. Un modèle en lecture seule lève une exception dans certaines versions de Windows. Pour utiliser ce membre, vous devez définir l’indicateur PSP_DLGINDIRECT dans le membre *dwFlags* . Ce membre est déclaré en tant qu’Union avec *pszTemplate*.

*hIcon* 

Type : [HICON](../winprog/windows-data-types.md)

Handle de l’icône à utiliser comme icône dans l’onglet de la page. Si le membre *dwFlags* n’inclut pas PSP_USEHICON, ce membre est ignoré. Ce membre est déclaré en tant qu’Union avec *pszIcon*.

*pszIcon* 

Type : [LPCSTR](../winprog/windows-data-types.md)

Ressource icône à utiliser comme icône dans l’onglet de la page. Ce membre peut spécifier l’identificateur de la ressource icône ou l’adresse de la chaîne qui spécifie le nom de la ressource icône. Pour utiliser ce membre, vous devez définir l’indicateur PSP_USEICONID dans le membre *dwFlags* . Ce membre est déclaré en tant qu’Union avec *HICON*.

*pszTitle* 

Type : [LPCSTR](../winprog/windows-data-types.md)

Titre de la boîte de dialogue de la feuille de propriétés. Ce titre remplace le titre spécifié dans le modèle de boîte de dialogue. Ce membre peut spécifier l’identificateur d’une ressource de chaîne ou l’adresse d’une chaîne qui spécifie le titre. Pour utiliser ce membre, vous devez définir l’indicateur PSP_USETITLE dans le membre *dwFlags* .

*pfnDlgProc* 

Type : **DLGPROC**

Pointeur vers la procédure de boîte de dialogue de la page. Étant donné que les pages sont créées sous forme de boîtes de dialogue non modales, la procédure de la boîte de dialogue ne doit pas appeler la fonction [EndDialog](/windows/win32/api/winuser/nf-winuser-enddialog) .

*lParam* 

Type : [lParam](../winprog/windows-data-types.md)

Lorsque la page est créée, une copie de la structure **PROPSHEETPAGE** de la page est transmise à la procédure de la boîte de dialogue avec un message de [WM_INITDIALOG](../dlgbox/wm-initdialog.md) . Le membre *lParam* est fourni pour vous permettre de passer des informations spécifiques à l’application à la procédure de boîte de dialogue. Il n'a aucun effet sur la page proprement dite.

*pfnCallback* 

Type : **LPFNPSPCALLBACK**

Pointeur vers une fonction de rappel définie par l’application qui est appelée lorsque la page est créée et quand elle est sur le point d’être détruite. Pour plus d’informations sur la fonction de rappel, consultez [fonction de rappel LPFNPSPCALLBACKA](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka). Pour utiliser ce membre, vous devez définir l’indicateur PSP_USECALLBACK dans le membre *dwFlags* .

*pcRefParent* 

Type : [uint *](../winprog/windows-data-types.md)

Pointeur vers la valeur du nombre de références. Pour utiliser ce membre, vous devez définir l’indicateur PSP_USEREFPARENT dans le membre *dwFlags* .

> [!NOTE]
> Lors de la création d’une page de feuille de propriétés, la valeur désignée par *pcRefParent* est incrémentée. Pour créer implicitement une page de feuille de propriétés, vous devez définir l’indicateur PSH_PROPSHEETPAGE dans le membre *dwFlags* de [PROPSHEETHEADER](pss-propsheetheader.md) et appeler la fonction [feuille](/windows/win32/api/prsht/nf-prsht-propertysheeta) . Vous pouvez le faire explicitement à l’aide de la fonction [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . Quand une page de feuille de propriétés est détruite, la valeur vers laquelle pointe le membre *pcRefParent* est décrémentée. Cette opération a lieu automatiquement lorsque la feuille de propriétés est détruite. Vous pouvez détruire explicitement une page de feuille de propriétés à l’aide de la fonction [DestroyPropertySheetPage](/windows/win32/api/prsht/nf-prsht-destroypropertysheetpage) .

*pszHeaderTitle* 

Type : [LPCTSTR](../winprog/windows-data-types.md)

[Version 5,80](common-control-versions.md) ou ultérieure. Titre de la zone d’en-tête. Pour utiliser ce membre sous l’Assistant de style Wizard97, vous devez également effectuer les opérations suivantes :

* Définissez l’indicateur PSP_USEHEADERTITLE dans le membre *dwFlags* .
* Définissez l’indicateur PSH_WIZARD97 dans le membre *dwFlags* de la structure [PROPSHEETHEADER](pss-propsheetheader.md) de la page.
* Assurez-vous que l’indicateur PSP_HIDEHEADER dans le membre *dwFlags* n’est pas défini.

*pszHeaderSubTitle* 

Type : [LPCTSTR](../winprog/windows-data-types.md)

[Version 5,80](common-control-versions.md) ou ultérieure. Sous-titre de la zone d’en-tête. Pour utiliser ce membre, vous devez effectuer les opérations suivantes :

* Définissez l’indicateur PSP_USEHEADERSUBTITLE dans le membre *dwFlags* .
* Définissez l’indicateur PSH_WIZARD97 dans le membre *dwFlags* de la structure [PROPSHEETHEADER](pss-propsheetheader.md) de la page.
* Assurez-vous que l’indicateur PSP_HIDEHEADER dans le membre *dwFlags* n’est pas défini.

> [!NOTE]
> Ce membre est ignoré lors de l’utilisation de l’Assistant style Aero ([PSH_AEROWIZARD](pss-propsheetheader.md))

*hActCtx* 

Type : [handle](../winprog/windows-data-types.md)

[Version 6,0](common-control-versions.md) ou ultérieure. Handle de contexte d’activation. Définissez ce membre sur le handle qui est retourné quand vous créez le contexte d’activation avec [CreateActCtx](/windows/win32/api/winbase/nf-winbase-createactctxa). Le système activera ce contexte avant de créer la boîte de dialogue. Vous n’avez pas besoin d’utiliser ce membre si vous utilisez un manifeste global.

*hbmHeader* 

Type : [HBITMAP](../winprog/windows-data-types.md)

Ce membre est déclaré en tant qu’Union avec *pszbmHeader*.

*pszbmHeader*

Type : [LPCSTR](../winprog/windows-data-types.md)

Ce membre est déclaré en tant qu’Union avec *hbmHeader*.

## <a name="remarks"></a>Notes

Comctl32.dll version 6 et versions ultérieures ne sont pas redistribuables. Pour utiliser Comctl32.dll version 6 ou ultérieure, spécifiez le fichier .dll dans un manifeste. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows \[Applications de bureau Vista uniquement\]                                    |
| Serveur minimal pris en charge | Windows Serveur 2003 \[ applications de bureau uniquement\]                              |
| En-tête                   | Prsht. h |
| Noms Unicode et ANSI                   | **PROPSHEETHEADERW** (Unicode) et **PROPSHEETHEADERA** (ANSI) |