---
description: Étend l’objet FolderItem. En plus des propriétés et des méthodes prises en charge par FolderItem, ShellFolderItem a deux méthodes supplémentaires.
title: Objet ShellFolderItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0e2f4c91-f9f9-4daa-a801-9c7fea8af738
ms.openlocfilehash: a9e6d6b3f954f0c8ee4b13fb651a9ea04274deb6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840770"
---
# <a name="shellfolderitem-object"></a>Objet ShellFolderItem

Étend l’objet [**FolderItem**](folderitem.md) . En plus des propriétés et des méthodes prises en charge par **FolderItem**, **ShellFolderItem** a deux méthodes supplémentaires.

## <a name="members"></a>Membres

L’objet **ShellFolderItem** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’objet **ShellFolderItem** a ces méthodes.



| Méthode                                                       | Description                                                                                                                                                                                         |
|:-------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExtendedProperty**](shellfolderitem-extendedproperty.md) | Obtient la valeur d’une propriété à partir du jeu de propriétés d’un élément. La propriété peut être spécifiée par nom ou par l’identificateur de format (FMTID) et l’identificateur de propriété (PID) du jeu de propriétés.<br/> |
| [**InvokeVerbEx**](invokeverbex.md)                         | Exécute un verbe sur un élément de Shell.<br/>                                                                                                                                                         |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 




