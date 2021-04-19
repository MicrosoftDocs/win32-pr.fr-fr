---
title: PROPSHEETHEADER, structure (Prsht. h)
description: Définit le frame et les pages d’une feuille de propriétés.
keywords:
- Contrôles Windows de la structure PROPSHEETHEADER
topic_type:
- apiref
api_name:
- PROPSHEETHEADER
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/23/2021
ms.openlocfilehash: 90a11ff727b491a1801f8071e28c39a3a6594408
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106540955"
---
# <a name="propsheetheader--structure"></a>PROPSHEETHEADER, structure

Définit le frame et les pages d’une feuille de propriétés.

## <a name="syntax"></a>Syntaxe

```cpp
typedef struct {
    DWORD      dwSize;
    DWORD      dwFlags;
    HWND       hwndParent;
    HINSTANCE  hInstance;
    union {
        HICON   hIcon;
        LPCTSTR pszIcon;
    };
    LPCTSTR  pszCaption;
    UINT     nPages;
    union {
        UINT    nStartPage;
        LPCTSTR pStartPage;
    };
    union {
        LPCPROPSHEETPAGE ppsp;
        HPROPSHEETPAGE   *phpage;
    };
    PFNPROPSHEETCALLBACK pfnCallback;
    union {
        HBITMAP hbmWatermark;
        LPCTSTR pszbmWatermark;
    };
    HPALETTE  hplWatermark;
    union {
        HBITMAP hbmHeader;
        LPCSTR  pszbmHeader;
    };
} PROPSHEETHEADER, *LPPROPSHEETHEADER;
```

## <a name="members"></a>Membres

*dwSize nul* 

Type : [DWORD](../winprog/windows-data-types.md)

Taille, en octets, de cette structure. Le gestionnaire de feuille de propriétés utilise ce membre pour déterminer la version de la structure **PROPSHEETHEADER** que vous utilisez. Pour plus d'informations, consultez la section Notes.

*dwFlags* 

Type : [DWORD](../winprog/windows-data-types.md)

Indicateurs qui spécifient quelles options utiliser pour créer la page de feuille de propriétés. Ce membre peut être une combinaison des valeurs suivantes.

| Valeur | Signification |
|-------|---------|
| PSH_DEFAULT (0x00000000) | Utilise la signification par défaut pour tous les membres de structure et crée une feuille de propriétés normale. Cet indicateur a une valeur égale à zéro et n’est pas combiné avec d’autres indicateurs. |
| PSH_AEROWIZARD (0x00004000) | [Version 6,00](common-control-versions.md) et versions ultérieures. Crée une feuille de propriétés d’assistant qui utilise le style Aero. L’indicateur PSH_WIZARD doit également être défini. Le modèle STA (Single-Threaded Apartment) doit être utilisé. |
| PSH_HASHELP (0x00000200) | Autorise les pages de la feuille de propriétés à afficher un bouton **d’aide** . Vous devez également définir l’indicateur PSP_HASHELP dans la structure [PROPSHEETPAGE](pss-propsheetpage.md) de la page lors de la création de la page. Si l’une des pages de la feuille de propriétés initiale active un bouton **aide** , PSH_HASHELP est défini automatiquement. Si aucune des pages initiales n’active un bouton **aide** , vous devez définir explicitement PSH_HASHELP si vous souhaitez avoir des boutons d’aide sur des pages qui peuvent être ajoutées ultérieurement. Cet indicateur n’est pas pris en charge conjointement avec PSH_AEROWIZARD.|
| PSH_HEADER (0x00080000) | [Version 5,80](common-control-versions.md) et versions ultérieures. Indique qu’une bitmap d’en-tête sera utilisée avec un Assistant Wizard97. Vous devez également définir l’indicateur PSH_WIZARD97. Si l’indicateur PSH_USEHBMHEADER est défini, la bitmap d’en-tête est obtenue à partir du membre *hbmHeader* . Dans le cas contraire, la bitmap d’en-tête est obtenue à partir du membre *pszbmHeader* . Cet indicateur n’est pas pris en charge conjointement avec PSH_AEROWIZARD. |
| PSH_HEADERBITMAP (0x08000000) | [Version 6,00](common-control-versions.md) et versions ultérieures. Le membre *pszbmHeader* spécifie une image bitmap qui est affichée dans la zone d’en-tête. Doit être utilisé en association avec PSH_AEROWIZARD. |
| PSH_MODELESS (0x00000400) | Fait en sorte que la fonction [feuille](/windows/win32/api/prsht/nf-prsht-propertysheeta) crée la feuille de propriétés en tant que boîte de dialogue non modale et non en tant que boîte de dialogue modale. Lorsque cet indicateur est défini, [feuille](/windows/win32/api/prsht/nf-prsht-propertysheeta) est retourné immédiatement après la création de la boîte de dialogue et la valeur de retour de [feuille](/windows/win32/api/prsht/nf-prsht-propertysheeta) est le handle de fenêtre de la boîte de dialogue de la feuille de propriétés. Cet indicateur n’est pas pris en charge conjointement avec PSH_AEROWIZARD. |
| PSH_NOAPPLYNOW (0x00000080) | Supprime le bouton **appliquer** . Cet indicateur n’est pas pris en charge conjointement avec PSH_AEROWIZARD. |
| PSH_NOCONTEXTHELP (0x02000000) | [Version 5,80](common-control-versions.md) et versions ultérieures. Supprime le bouton d’aide contextuelle («  ? »), qui est généralement présent dans la barre de légende des feuilles de propriétés. Cet indicateur n’est pas valide pour les assistants. Pour plus d’informations sur la suppression du bouton d' **aide** de la barre de légende pour les versions antérieures des contrôles communs, consultez à [propos des feuilles de propriétés](property-sheets.md) . Cet indicateur n’est pas pris en charge conjointement avec PSH_AEROWIZARD. |
| PSH_NOMARGIN (0x10000000) | [Version 6,00](common-control-versions.md) ou ultérieure. Spécifie qu’aucune marge n’est insérée entre la page et le cadre. Doit être utilisé en association avec PSH_AEROWIZARD. |
| PSH_PROPSHEETPAGE (0x00000008) | Utilise le membre *PPSP* et ignore le membre *phpage* lors de la création des pages pour la feuille de propriétés. |
| PSH_PROPTITLE (0x00000001) | Indique que le *pszCaption* est le nom de l’élément pour lequel les propriétés sont affichées. Windows effectue un ajustement dépendant de la version et de la langue de la légende. Par exemple, en anglais, l’expression « propriétés pour » est ajoutée à un *pszCaption* non vide (et si le *pszCaption* produit une légende vide, le titre est simplement « propriétés »). Si cet indicateur est omis, le pszCaption est utilisé sans modification.  |
| PSH_RESIZABLE (0x04000000) | Autorise le redimensionnement de l’Assistant par l’utilisateur. Les boutons agrandir et réduire s’affichent dans le frame de l’Assistant et le cadre est redimensionnable. Pour utiliser cet indicateur, vous devez également définir PSH_AEROWIZARD. |
| PSH_RTLREADING (0x00000800) | Affecte l’ordre de lecture de droite à gauche (RTL) à la feuille de propriétés ou à la fenêtre de l’Assistant, en fonction des langues telles que l’hébreu et l’arabe. Si cet indicateur n’est pas spécifié, les fenêtres de la feuille de propriétés sont définies par défaut de gauche à droite (LTR) et les fenêtres de l’Assistant correspondent à l’ordre de lecture de la page actuelle. |
| PSH_STRETCHWATERMARK (0x00040000) | Étire le filigrane dans les assistants de style Wizard97. Cet indicateur n’est pas pris en charge conjointement avec PSH_AEROWIZARD. Cet indicateur de style est uniquement inclus pour fournir une compatibilité descendante pour certaines applications. Son utilisation n’est pas recommandée, et elle est uniquement prise en charge par les contrôles communs versions 4,0 et 4,01. Avec les contrôles communs version 5,80 et versions ultérieures, cet indicateur est ignoré. |
| PSH_USECALLBACK (0x00000100) | Appelle la fonction spécifiée par le paramètre *pfnCallback* lorsque certains événements se produisent. Pour plus d’informations, consultez la description de la fonction de rappel [PFNPROPSHEETCALLBACK](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) . |
| PSH_USEHBMHEADER (0x00100000) | [Version 5,80](common-control-versions.md). Obtient la bitmap d’en-tête à partir du membre *hbmHeader* au lieu du membre *pszbmHeader* . Vous devez également définir l’indicateur PSH_AEROWIZARD ou l’indicateur PSH_WIZARD97 avec l’indicateur PSH_HEADER. |
| PSH_USEHBMWATERMARK (0x00010000) | [Version 5,80](common-control-versions.md). Obtient la bitmap de filigrane à partir du membre *hbmWatermark* au lieu du membre *pszbmWatermark* . Vous devez également définir PSH_WIZARD97 et PSH_WATERMARK. Cet indicateur n’est pas pris en charge conjointement avec PSH_AEROWIZARD. |
| PSH_USEHICON (0x00000002) | Utilise *HICON* comme petite icône dans la barre de titre de la boîte de dialogue feuille de propriétés. |
| PSH_USEHPLWATERMARK (0x00020000) | [Version 5,80](common-control-versions.md). Utilise la structure **HPALETTE** désignée par le membre *hplWatermark* au lieu de la palette par défaut pour dessiner la bitmap de filigrane et/ou l’image bitmap d’en-tête pour un Assistant Wizard97. Vous devez également définir PSH_WIZARD97, et PSH_WATERMARK ou PSH_HEADER. Cet indicateur n’est pas pris en charge conjointement avec PSH_AEROWIZARD.  |
| PSH_USEICONID (0x00000004) | Utilise *pszIcon* comme nom de la ressource icône à charger et utiliser comme petite icône dans la barre de titre de la boîte de dialogue feuille de propriétés. |
| PSH_USEPAGELANG (0x00200000) | [Version 5,80](common-control-versions.md). Spécifie que la langue de la feuille de propriétés sera extraite de la ressource de la première page. Cette page doit être spécifiée par l’identificateur de ressource. |
| PSH_USEPSTARTPAGE (0x00000040) | Utilise le membre *pStartPage* à la place du membre *nStartPage* lors de l’affichage de la page initiale de la feuille de propriétés. |
| PSH_WATERMARK (0x00008000) | [Version 5,80](common-control-versions.md). Spécifie qu’une bitmap de filigrane sera utilisée avec un Assistant Wizard97 sur les pages qui ont le style PSP_HIDEHEADER. Vous devez également définir l’indicateur PSH_WIZARD97. La bitmap de filigrane est obtenue à partir du membre *pszbmWatermark* , sauf si PSH_USEHBMWATERMARK est défini. Dans ce cas, la bitmap d’en-tête est obtenue à partir du membre *hbmWatermark* . Cet indicateur n’est pas pris en charge conjointement avec PSH_AEROWIZARD.  |
| PSH_WIZARD (0x00000020) | Crée une feuille de propriétés d’Assistant. Lorsque vous utilisez PSH_AEROWIZARD, vous devez également définir cet indicateur. |
| PSH_WIZARD97 (0x01000000) | [Version 5,80](common-control-versions.md). Crée une feuille de propriétés de type Wizard97, qui prend en charge les bitmaps dans l’en-tête des pages intérieures et sur le côté gauche des pages extérieures. Cet indicateur n’est pas pris en charge conjointement avec PSH_AEROWIZARD. |
| PSH_WIZARDCONTEXTHELP (0x00001000) | Ajoute un bouton **d’aide** contextuelle («  ? »), qui est généralement absent de la barre de légende d’un Assistant. Cet indicateur n’est pas valide pour les feuilles de propriétés standard. Cet indicateur n’est pas pris en charge conjointement avec PSH_AEROWIZARD. |
| PSH_WIZARDHASFINISH (0x00000010)  | Affiche toujours le bouton **Terminer** dans l’Assistant. Vous devez également définir PSH_WIZARD, PSH_WIZARD97 ou PSH_AEROWIZARD. |
| PSH_WIZARD_LITE (0x00400000) | [Version 5,80](common-control-versions.md). Utilise le style Assistant-Lite. Ce style est semblable à PSH_WIZARD97, mais il est implémenté de la même façon que PSH_WIZARD. Il existe peu de restrictions sur la façon dont les pages sont mises en forme. Par exemple, il n’y a pas de bordures imposées et le style de PSH_WIZARD_LITE ne peint pas les bitmaps de filigrane et d’en-tête pour vous comme le fait Wizard97. Cet indicateur n’est pas pris en charge conjointement avec PSH_AEROWIZARD. |

*hwndParent* 

Type : [HWND](../winprog/windows-data-types.md)

Handle vers la fenêtre propriétaire de la feuille de propriétés.

*hInstance* 

Type : [HINSTANCE](../winprog/windows-data-types.md)

Handle de l’instance à partir de laquelle charger l’icône, la ressource de chaîne de titre, le nom de la page de démarrage, la bitmap d’en-tête ou le filigrane. Si le membre *pszIcon*, *pszCaption*, *pStartPage*, *pszbmHeader* ou *pszbmWatermark* identifie une ressource à charger, ce membre doit être spécifié.

*hIcon* 

Type : [HICON](../winprog/windows-data-types.md)

Handle de l’icône à utiliser comme petite icône dans la barre de titre de la boîte de dialogue feuille de propriétés. Ce membre est utilisé si le membre *dwFlags* comprend PSH_USEHICON. Ce membre est déclaré en tant qu’Union avec *pszIcon*.

*pszIcon* 

Type : [LPCTSTR](../winprog/windows-data-types.md)

Ressource icône à utiliser comme petite icône dans la barre de titre de la boîte de dialogue feuille de propriétés. Ce membre est utilisé si le membre *dwFlags* comprend PSH_USEICONID. Ce membre peut spécifier l’identificateur de la ressource icône ou l’adresse de la chaîne qui spécifie le nom de la ressource icône. Dans les deux cas, l’icône est chargée à partir de l’instance fournie par le membre *HINSTANCE* . Ce membre est déclaré en tant qu’Union avec *HICON*.

*pszCaption* 

Type : [LPCTSTR](../winprog/windows-data-types.md)

Titre de la boîte de dialogue de la feuille de propriétés. Ce membre peut spécifier l’identificateur d’une ressource de type chaîne (chargée à partir de l’instance spécifiée par le membre *HINSTANCE* ) ou l’adresse d’une chaîne qui spécifie le titre. Si le membre *dwFlags* comprend PSH_PROPTITLE, les **Propriétés de chaîne de** sont insérées au début du titre. Ce champ est ignoré pour les assistants Wizard97. Pour les assistants Aero, la chaîne seule est utilisée pour la légende, que l’indicateur PSH_PROPTITLE soit défini ou non.

*nPages* 

Type : [uint](../winprog/windows-data-types.md)

Nombre de pages de feuille de propriétés fournies dans le tableau *PPSP* ou *phpage* .

*nStartPage* 

Type : [uint](../winprog/windows-data-types.md)

Index de base zéro de la page initiale qui apparaît lors de la création de la boîte de dialogue de la feuille de propriétés. Ce membre est utilisé si le membre *dwFlags* n’inclut pas l’indicateur PSH_USEPSTARTPAGE. Ce membre est déclaré en tant qu’Union avec *pStartPage*.

*pStartPage* 

Type : [LPCTSTR](../winprog/windows-data-types.md)

Nom de la page initiale qui s’affiche lors de la création de la boîte de dialogue de la feuille de propriétés. Ce membre est utilisé si le membre *dwFlags* comprend l’indicateur PSH_USESTARTPAGE. Ce membre peut spécifier l’identificateur d’une ressource de type chaîne (chargée à partir de l’instance spécifiée par le membre *HINSTANCE* ) ou l’adresse d’une chaîne qui spécifie le nom. Le nom de la page de démarrage est mis en correspondance avec les légendes des pages. Ce membre est déclaré en tant qu’Union avec *nStartPage*.

*ppsp* 

Type : **LPCPROPSHEETPAGE**

Pointeur vers un tableau de structures [PROPSHEETPAGE](pss-propsheetpage.md) qui définissent les pages dans la feuille de propriétés. Si le membre *dwFlags* n’inclut pas PSH_PROPSHEETPAGE, ce membre est ignoré. Notez que la taille de la structure **PROPSHEETPAGE** est variable. Les applications qui analysent le tableau pointé par *PPSP* doivent prendre en compte la taille de chaque page. Ce membre est déclaré en tant qu’Union avec *phpage*.

*phpage* 

Type : **HPROPSHEETPAGE \***

Pointeur vers un tableau de handles vers les pages de feuille de propriétés. Ce membre est utilisé si le membre *dwFlags* n’inclut pas PSH_PROPSHEETPAGE. Chaque handle doit avoir été créé par un appel précédent à la fonction [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . Lorsque la fonction [feuille](/windows/win32/api/prsht/nf-prsht-propertysheeta) retourne, tous les descripteurs HPROPSHEETPAGE du tableau *phpage* ont été détruits. Ce membre est déclaré en tant qu’Union avec *PPSP*.

*pfnCallback* 

Type : **PFNPROPSHEETCALLBACK**

Pointeur vers une fonction de rappel définie par l’application qui est appelée lorsque certains événements se produisent. Pour plus d’informations sur la fonction de rappel, consultez la description de la fonction de rappel [PFNPROPSHEETCALLBACK](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) . Si le membre *dwFlags* n’inclut pas PSH_USECALLBACK, ce membre est ignoré.

*hbmWatermark* 

Type : [HBITMAP](../winprog/windows-data-types.md)

[Version 5,80](common-control-versions.md) ou ultérieure. Handle de la bitmap de filigrane. Si le membre *dwFlags* n’inclut pas PSH_USEHBMWATERMARK, ce membre est ignoré.

*pszbmWatermark* 

Type : [LPCTSTR](../winprog/windows-data-types.md)

[Version 5,80](common-control-versions.md) ou ultérieure. Ressource bitmap à utiliser comme filigrane. Ce membre peut spécifier soit l’identificateur de la ressource bitmap, soit l’adresse de la chaîne qui spécifie le nom de la ressource bitmap. Si le membre *dwFlags* comprend PSH_USEHBMWATERMARK, ce membre est ignoré.

*hplWatermark*

Type : [HPALETTE](../winprog/windows-data-types.md)

[Version 5,80](common-control-versions.md) ou ultérieure. Structure **HPALETTE** utilisée pour dessiner la bitmap de filigrane et/ou la bitmap d’en-tête. Si le membre *dwFlags* n’inclut pas PSH_USEHPLWATERMARK, ce membre est ignoré.

*hbmHeader*

Type : [HBITMAP](../winprog/windows-data-types.md)

[Version 5,80](common-control-versions.md) ou ultérieure. Handle vers la bitmap d’en-tête. Si le membre *dwFlags* n’inclut pas PSH_USEHBMHEADER, ce membre est ignoré.

*pszbmHeader*

Type : [LPCSTR](../winprog/windows-data-types.md)

[Version 5,80](common-control-versions.md) ou ultérieure. Ressource bitmap à utiliser comme en-tête. Ce membre peut spécifier soit l’identificateur de la ressource bitmap, soit l’adresse de la chaîne qui spécifie le nom de la ressource bitmap. Si le membre *dwFlags* comprend PSH_USEHBMHEADER, ce membre est ignoré.

## <a name="remarks"></a>Notes

Si l’utilisateur choisit un paramètre tel que grandes polices, qui agrandit la boîte de dialogue, le filigrane qui est peint sur les pages de démarrage et de fin est également agrandi. La taille et la position de la bitmap d’origine restent inchangées. La zone supplémentaire est remplie avec la couleur du pixel dans le coin supérieur gauche de l’image bitmap.

Les styles PSH_WIZARD, PSH_WIZARD97 et PSH_WIZARD_LITE sont mutuellement incompatibles. Un seul de ces indicateurs de style doit être défini. PSH_AEROWIZARD doit être combiné avec PSH_WIZARD.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | Applications de \[ Bureau Windows Vista uniquement\]                                    |
| Serveur minimal pris en charge | Applications de bureau Windows Server 2003 \[ uniquement\]                              |
| En-tête                   | Prsht. h |
| Noms Unicode et ANSI                   | **PROPSHEETHEADERW** (Unicode) et **PROPSHEETHEADERA** (ANSI) |
