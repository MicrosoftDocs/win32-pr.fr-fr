---
description: Spécifie une fonction de rappel définie par l’application appelée par le gestionnaire de fichiers pour communiquer avec une extension du gestionnaire de fichiers.
title: FMExtensionProc, fonction de rappel (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMExtensionProc
- FMExtensionProcW
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 6e02d655-f7d8-460a-97d2-5b369493e941
ms.openlocfilehash: 7cd13fe534f3bb121a4056f67ceff47ddfa71fa5506c2020a243ab340768ce35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032657"
---
# <a name="fmextensionproc-callback-function"></a>FMExtensionProc fonction de rappel

Spécifie une fonction de rappel définie par l’application appelée par le gestionnaire de fichiers pour communiquer avec une extension du gestionnaire de fichiers.

## <a name="syntax"></a>Syntaxe


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Type : **HWND**

Handle de fenêtre vers le gestionnaire de fichiers. Une extension utilise ce handle pour spécifier la fenêtre parente pour une boîte de dialogue ou une boîte de message qu’elle doit afficher, et pour envoyer des messages de requête au gestionnaire de fichiers.

</dd> <dt>

*wMsg* 
</dt> <dd>

Type : **Word**

Un des messages du gestionnaire de fichiers suivants.

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 à 99**


</dt> <dd>

L’utilisateur a sélectionné un élément dans le menu fourni par l’extension. La valeur est l’identificateur de l’élément de menu sélectionné.

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT \_ HELPMENUITEM**


</dt> <dd>

L’utilisateur a appuyé sur F1 tout en sélectionnant un menu d’extension ou un élément de commande de barre d’outils. Indique que l’extension doit appeler **WinHelp** de manière appropriée pour l’élément de commande.

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**\_HELPSTRING FMEVENT**


</dt> <dd>

L’utilisateur a sélectionné un menu d’extension ou un élément de commande de barre d’outils. Indique que l’extension doit fournir une chaîne d’aide.

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT \_ INITMENU**


</dt> <dd>

L’utilisateur a sélectionné le menu de l’extension. L’extension doit initialiser des éléments dans le menu.

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**\_charge FMEVENT**


</dt> <dd>

Le gestionnaire de fichiers charge la DLL d’extension et invite la DLL à fournir des informations sur le menu fourni par la DLL.

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT \_ selChange**


</dt> <dd>

La sélection dans la fenêtre répertoire du **Gestionnaire de fichiers** ou dans la fenêtre des résultats de la **recherche** a changé.

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT \_ TOOLBARLOAD**


</dt> <dd>

Le gestionnaire de fichiers crée la barre d’outils et demande à la DLL d’extension des informations sur les boutons que la DLL ajoute à la barre d’outils.

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**\_déchargement FMEVENT**


</dt> <dd>

Le gestionnaire de fichiers décharge la DLL d’extension.

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT l’actualisation de l' \_ utilisateur \_**


</dt> <dd>

L’utilisateur a sélectionné la commande **Actualiser** dans le menu **fenêtre** . L’extension doit mettre à jour les éléments dans le menu, si nécessaire.

</dd> </dl> </dd> <dt>

*lParam* 
</dt> <dd>

Type : **long**

Valeur spécifique au message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **long**

Retourne une valeur en fonction du message de paramètre *wMsg* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **FMExtensionProcW** (Unicode)<br/>                                          |



 

 




