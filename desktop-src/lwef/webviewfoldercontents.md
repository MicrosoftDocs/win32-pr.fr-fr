---
title: WebViewFolderContents, objet (Shldisp.h)
description: Implémenté par le Shell pour une utilisation à l’intérieur d’une WebView.
ms.assetid: c9c46e21-2721-43c9-a6f4-38fafbda3798
keywords:
- fonctionnalités d’environnement Windows héritées d’objets WebViewFolderContents
- fonctionnalités de l’environnement Windows héritées de l’objet WebViewFolderContents, description
topic_type:
- apiref
api_name:
- WebViewFolderContents
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fe0146f49d0e5172410ca119953a7b3f245af20c0e4c2d83ff78fa23b93e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035957"
---
# <a name="webviewfoldercontents-object"></a>Objet WebViewFolderContents

Implémenté par le Shell pour une utilisation à l’intérieur d’une *WebView*. **WebViewFolderContents** s’initialise automatiquement dans le dossier actif de WebView. Il crée un affichage des dossiers de l’interpréteur de commandes qui affiche le contenu du dossier dans l’un des cinq formats suivants : petite icône, grande icône, liste, détails ou miniature. Elle n’est pas valide en dehors d’une WebView.

Les méthodes et propriétés exposées par **WebViewFolderContents** sont identiques à celles de l’objet [**ShellFolderView**](/windows/desktop/shell/shellfolderview) .

## <a name="members"></a>Membres

L’objet **WebViewFolderContents** possède les types de membres suivants :

-   [Événements](#events)
-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="events"></a>Événements

L’objet **WebViewFolderContents** contient ces événements.



| Événement                                                              | Description                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**SelectionChanged**](webviewfoldercontents-selectionchanged.md) | Se produit lorsque l’état de sélection d’un élément ou d’éléments de la vue a été modifié.<br/> |



 

### <a name="methods"></a>Méthodes

L’objet **WebViewFolderContents** a ces méthodes.



| Méthode                                                       | Description                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**PopupItemMenu**](webviewfoldercontents-popupitemmenu.md) | Crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.<br/>                   |
| [**SelectedItems**](webviewfoldercontents-selecteditems.md) | Obtient un objet [**FolderItems**](../shell/folderitems.md) qui représente tous les éléments sélectionnés dans la vue.<br/> |
| [**SelectItem**](webviewfoldercontents-selectitem.md)       | Définit l’état de sélection d’un élément dans la vue.<br/>                                                          |



 

### <a name="properties"></a>Propriétés

L’objet **WebViewFolderContents** a ces propriétés.



| Propriété                                                            | Type d’accès          | Description                                                                                                                              |
|:--------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Application**](webviewfoldercontents-application.md)<br/> | Lecture seule<br/> | Non implémenté.<br/>                                                                                                              |
| [**FocusedItem**](webviewfoldercontents-focuseditem.md)<br/> | Lecture seule<br/> | Obtient un objet [**FolderItem**](../shell/folderitem.md) qui représente l’élément ayant le focus d’entrée.<br/>                           |
| [**Dossier**](webviewfoldercontents-folder.md)<br/>           | Lecture seule<br/> | Obtient un objet [**dossier**](../shell/folder.md) qui représente la vue.<br/>                                                            |
| [**Parent**](webviewfoldercontents-parent.md)<br/>           | Lecture seule<br/> | Non implémenté.<br/>                                                                                                              |
| [**Conseils**](webviewfoldercontents-script.md)<br/>           | Lecture seule<br/> | Obtient l’objet de script pour la vue.<br/>                                                                                       |
| [**ViewOptions**](webviewfoldercontents-viewoptions.md)<br/> | Lecture seule<br/> | Obtient un jeu d’indicateurs [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) qui indiquent les options actuelles de la vue.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

