---
description: Représente les objets dans une vue et fournit des propriétés et des méthodes utilisées pour obtenir des informations sur le contenu de la vue.
ms.assetid: 3b866266-fee0-42f7-a1e0-9adb6cc2e23f
title: Objet ShellFolderView (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a95d57edb7992c9511e34480190580d34ad42da23c64c4297f5e4ebb75a95e73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452126"
---
# <a name="shellfolderview-object"></a>Objet ShellFolderView

Représente les objets dans une vue et fournit des propriétés et des méthodes utilisées pour obtenir des informations sur le contenu de la vue.

## <a name="members"></a>Membres

L’objet **ShellFolderView** possède les types de membres suivants :

-   [Événements](#events)
-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="events"></a>Événements

L’objet **ShellFolderView** contient ces événements.



| Événement                                                        | Description                                                                              |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**SelectionChanged**](shellfolderview-selectionchanged.md) | Se produit lorsque l’état de sélection d’un élément ou d’éléments de la vue a été modifié.<br/> |



 

### <a name="methods"></a>Méthodes

L’objet **ShellFolderView** a ces méthodes.



| Méthode                                                 | Description                                                                                                        |
|:-------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**PopupItemMenu**](shellfolderview-popupitemmenu.md) | Crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.<br/>                 |
| [**SelectedItems**](shellfolderview-selecteditems.md) | Obtient un objet [**FolderItems**](folderitems.md) qui représente tous les éléments sélectionnés dans la vue.<br/> |
| [**SelectItem**](shellfolderview-selectitem.md)       | Définit l’état de sélection d’un élément dans la vue.<br/>                                                        |



 

### <a name="properties"></a>Propriétés

L’objet **ShellFolderView** a ces propriétés.



| Propriété                                                      | Type d’accès          | Description                                                                                                  |
|:--------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------|
| [**Application**](shellfolderview-application.md)<br/> | Lecture seule<br/> | Contient l’objet d’application de l’objet.<br/>                                                         |
| [**FocusedItem**](shellfolderview-focuseditem.md)<br/> | Lecture seule<br/> | Obtient un objet [**FolderItem**](folderitem.md) qui représente l’élément ayant le focus d’entrée.<br/> |
| [**Dossier**](shellfolderview-folder.md)<br/>           | Lecture seule<br/> | Obtient un objet [**dossier**](folder.md) qui représente la vue.<br/>                                  |
| [**Parent**](shellfolderview-parent.md)<br/>           | Lecture seule<br/> | Non implémenté.<br/>                                                                                  |
| [**Conseils**](shellfolderview-script.md)<br/>           | Lecture seule<br/> | Action déconseillée.<br/>                                                                                       |
| [**ViewOptions**](shellfolderview-viewoptions.md)<br/> | Lecture seule<br/> | Obtient un jeu d’indicateurs qui indiquent les options actuelles de la vue.<br/>                                |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |
| IID<br/>                      | CLSID \_ ShellFolderView<br/>                                                                              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Indicateurs ShellFolderViewOptions**](/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions)
</dt> </dl>

 

 




