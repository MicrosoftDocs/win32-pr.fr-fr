---
description: Transfère les événements déclenchés par un objet ShellFolderView spécifié aux gestionnaires d’événements ShellFolderViewOC correspondants.
title: Objet ShellFolderViewOC (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b50f549c-a79d-4411-a18e-a181b4b924e3
ms.openlocfilehash: b9a2b76f48731bf4c7b515779122503fa2cb02f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952757"
---
# <a name="shellfolderviewoc-object"></a>Objet ShellFolderViewOC

Transfère les événements déclenchés par un objet [**ShellFolderView**](shellfolderview.md) spécifié aux gestionnaires d’événements **ShellFolderViewOC** correspondants.

## <a name="members"></a>Membres

L’objet **ShellFolderViewOC** possède les types de membres suivants :

-   [Événements](#events)
-   [Méthodes](#methods)

### <a name="events"></a>Événements

L’objet **ShellFolderViewOC** contient ces événements.



| Événement                                                          | Description                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDone**](shellfolderviewoc-enumdone.md)                 | Indique que l’objet [**ShellFolderView**](shellfolderview.md) a terminé l’énumération du contenu du dossier.<br/> |
| [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) | Indique que l’état de sélection d’un ou plusieurs éléments de la vue a changé.<br/>                                     |



 

### <a name="methods"></a>Méthodes

L’objet **ShellFolderViewOC** a ces méthodes.



| Méthode                                                   | Description                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetFolderView**](shellfolderviewoc-setfolderview.md) | Transfère les événements de l’objet [**ShellFolderView**](shellfolderview.md) spécifié au gestionnaire d’événements **ShellFolderViewOC** correspondant.<br/> |



 

## <a name="remarks"></a>Notes

L’objet [**ShellFolderView**](shellfolderview.md) déclenche deux événements, [**EnumDone**](shellfolderviewoc-enumdone.md) et [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), qui sont généralement gérés par des applications. Toutefois, certaines applications doivent gérer les événements d’une série d’objets **ShellFolderView** . Par exemple, une application peut héberger un contrôle WebBrowser qui permet aux utilisateurs de naviguer dans une série de dossiers. Chaque dossier a son propre objet **ShellFolderView** avec ses événements associés. La gestion de ces événements peut être difficile.

L’objet **ShellFolderViewOC** simplifie la gestion des événements pour de tels scénarios. Elle permet aux applications de gérer des événements pour tous les objets [**ShellFolderView**](shellfolderview.md) avec une seule paire de gestionnaires d’événements **ShellFolderViewOC** . Chaque fois que l’utilisateur accède à un nouveau dossier, l’application transmet l’objet **ShellFolderView** associé à l’objet **ShellFolderViewOC** en appelant [**SetFolderView**](shellfolderviewoc-setfolderview.md). Ensuite, lorsqu’un événement [**EnumDone**](shellfolderviewoc-enumdone.md) ou [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) est déclenché, l’objet **ShellFolderViewOC** transfère l’événement à son propre gestionnaire de traitement.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ShellFolderView**](shellfolderview.md)
</dt> </dl>

 

 




