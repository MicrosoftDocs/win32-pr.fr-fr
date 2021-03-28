---
description: Gère les liens de l’interpréteur de commandes. Cet objet permet d’accéder à la plupart des fonctionnalités de l’interface IShellLink pour la script des applications.
title: Objet ShellLinkObject (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: d3c0ccf8-0f83-42f7-9d6f-1fb293da6364
ms.openlocfilehash: 1daf1aafae4bc230014890b79d4fb0310aa30a1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973738"
---
# <a name="shelllinkobject-object"></a>Objet ShellLinkObject

Gère les liens de l’interpréteur de commandes. Cet objet permet d’accéder à la plupart des fonctionnalités de l’interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) pour la script des applications.

## <a name="members"></a>Membres

L’objet **ShellLinkObject** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **ShellLinkObject** a ces méthodes.



| Méthode                                                     | Description                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetIconLocation**](shelllinkobject-geticonlocation.md) | Obtient l’emplacement de l’icône assignée au lien.<br/>                                 |
| [**Résolution**](shelllinkobject-resolve.md)                 | Recherche la cible d’un lien de Shell, même si la cible a été déplacée ou renommée.<br/> |
| [**Enregistrer**](shelllinkobject-save.md)                       | Enregistre toutes les modifications apportées au lien.<br/>                                                      |
| [**SetIconLocation**](shelllinkobject-seticonlocation.md) | Définit l’emplacement de l’icône assignée au lien.<br/>                                 |



 

### <a name="properties"></a>Propriétés

L’objet **ShellLinkObject** a ces propriétés.



| Propriété                                                                | Type d’accès           | Description                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Arguments**](shelllinkobject-arguments.md)<br/>               | Lecture/écriture<br/> | Contient les arguments d’un lien.<br/>                                                                   |
| [**Description**](shelllinkobject-description.md)<br/>           | Lecture/écriture<br/> | Obtient ou définit la description du lien.<br/>                                                      |
| [**Touche d’accès rapide**](shelllinkobject-hotkey.md)<br/>                     | Lecture/écriture<br/> | Obtient ou définit le raccourci clavier du lien.<br/>                                               |
| [**Path**](shelllinkobject-path.md)<br/>                         | Lecture/écriture<br/> | Obtient ou définit le chemin d’accès à l’objet de lien.<br/>                                                      |
| [**ShowCommand**](shelllinkobject-showcommand.md)<br/>           | Lecture/écriture<br/> | Obtient ou définit l’état d’affichage initial (dimensionné, réduit ou agrandi) de la commande du lien.<br/> |
| [**WorkingDirectory**](shelllinkobject-workingdirectory.md)<br/> | Lecture/écriture<br/> | Obtient ou définit le répertoire de travail spécifié dans le lien.<br/>                                      |



 

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

[Liens de Shell](./links.md)
</dt> </dl>

 

 
