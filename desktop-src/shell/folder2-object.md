---
description: Étend l’objet Folder pour prendre en charge les dossiers hors connexion.
title: Objet Dossier2 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b52b141-ced3-4d38-8584-7dfcfe12ab56
ms.openlocfilehash: 8db899fc52cc3511d1af82013fc6c4c87544f1cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973210"
---
# <a name="folder2-object"></a>Dossier2, objet

Étend l’objet [**Folder**](folder.md) pour prendre en charge les dossiers hors connexion.

## <a name="members"></a>Membres

L’objet **dossier2** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **dossier2** possède ces méthodes.



| Méthode                                                                 | Description                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**DismissedWebViewBarricade**](folder2-dismissedwebviewbarricade.md) | Appelée en réponse à la barricade d’affichage Web qui est ignorée par l’utilisateur.<br/> |
| [**Non**](folder2-synchronize.md)                             | Synchronise tous les fichiers hors connexion dans le dossier.<br/>                             |



 

### <a name="properties"></a>Propriétés

L’objet **dossier2** possède les propriétés suivantes.



| Propriété                                                                            | Type d’accès          | Description                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [**HaveToShowWebViewBarricade**](folder2-havetoshowwebviewbarricade.md)<br/> | Lecture seule<br/> | Actuellement non pris en charge.<br/>                                       |
| [**OfflineStatus**](folder2-offlinestatus.md)<br/>                           | Lecture seule<br/> | Contient l’état hors connexion du dossier.<br/>                     |
| [**Rythme**](folder2-self.md)<br/>                                             | Lecture seule<br/> | Contient l’objet [**FolderItem**](folderitem.md) du dossier.<br/> |



 

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

[**Dossier**](folder.md)
</dt> </dl>

 

 




