---
description: Représente un dossier de Shell. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur le dossier.
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: Objet Folder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: baf180149419178b489f3ba00042c561268b36e7b7ed7b0e2afab54b68f78466
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032617"
---
# <a name="folder-object"></a>Objet Folder

Représente un dossier de Shell. Cet objet contient des propriétés et des méthodes qui vous permettent de récupérer des informations sur le dossier.

## <a name="members"></a>Membres

L’objet **Folder** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **Folder** possède ces méthodes.



| Méthode                                      | Description                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [**CopyHere**](folder-copyhere.md)         | Copie un ou des éléments dans un dossier.<br/>                                                                            |
| [**GetDetailsOf**](folder-getdetailsof.md) | Récupère des détails sur un élément dans un dossier. Par exemple, sa taille, son type ou l’heure de sa dernière modification.<br/> |
| [**Éléments**](folder-items.md)               | Récupère un objet [**FolderItems**](folderitems.md) qui représente la collection d’éléments dans le dossier.<br/>    |
| [**MoveHere**](folder-movehere.md)         | Déplace un élément ou des éléments vers ce dossier.<br/>                                                                          |
| [**NewFolder**](folder-newfolder.md)       | Crée un nouveau dossier.<br/>                                                                                           |
| [**ParseName**](folder-parsename.md)       | Crée et retourne un objet [**FolderItem**](folderitem.md) qui représente un élément spécifié.<br/>                 |



 

### <a name="properties"></a>Propriétés

L’objet **Folder** possède ces propriétés.



| Propriété                                               | Type d’accès          | Description                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [**Application**](folder-application.md)<br/>   | Lecture seule<br/> | Contient l’objet d’application du dossier.<br/> |
| [**Parent**](folder-parent.md)<br/>             | Lecture seule<br/> | Non implémenté.<br/>                          |
| [**ParentFolder**](folder-parentfolder.md)<br/> | Lecture seule<br/> | Contient l’objet **dossier** parent.<br/>    |
| [**Titre**](folder-title.md)<br/>               | Lecture seule<br/> | Contient le titre du dossier.<br/>         |



 

## <a name="remarks"></a>Remarques

> [!Note]  
> Toutes les méthodes ne sont pas implémentées pour tous les dossiers. Par exemple, la méthode [**ParseName**](folder-parsename.md) n’est pas implémentée pour le dossier du panneau de configuration ( \_ contrôles CSIDL). Si vous tentez d’appeler une méthode non implémentée, une erreur 0x800A01BD (Decimal 445) est générée.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                 |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




