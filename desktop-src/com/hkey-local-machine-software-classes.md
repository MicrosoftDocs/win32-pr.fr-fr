---
title: HKEY_LOCAL_MACHINESOFTWAREClasses
description: Les sous-clés et les valeurs de Registre associées à la \_ clé HKEY local \_ machine \\ Software \\ classes contiennent des informations sur une application qui est nécessaire pour prendre en charge les fonctionnalités com.
ms.assetid: a5b271d6-f445-45df-a8e4-f6e0194ac824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9a79c417c48c5392fe5ceea3e99cce5e874bc9
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884879"
---
# <a name="hkey_local_machinesoftwareclasses"></a>HKEY \_ local \_ machine \\ classes de logiciels \\

Les sous-clés et les valeurs de Registre associées à la clé **HKEY \_ local \_ machine \\ Software \\ classes** contiennent des informations sur une application qui est nécessaire pour prendre en charge les fonctionnalités com. Ces informations incluent des rubriques telles que des formats de données pris en charge, des informations de compatibilité, des identificateurs de programmation, DCOM et des contrôles.



| Sous-clé                                                                         | Description                                                                                                       |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**AppID**](appid-key.md)                                                     | Options de configuration pour les applications basées sur COM.                                                                 |
| [**IDENTIFICATEUR**](clsid-key-hklm.md)                                                | Options de configuration pour les classes COM.                                                                            |
| [**Extension de fichier<\_>**](-file-extension--key.md)                        | Associe une extension de nom de fichier à un ProgID.                                                                   |
| [**FileType**](filetype-key.md)                                               | Utilisé par [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) pour faire correspondre des modèles à différents octets de fichier dans un fichier non composé. |
| [**Interface**](interface-key.md)                                             | Associe un nom d’interface à un ID d’interface (IID).                                                          |
| [**&lt;ProgID&gt;**](-progid--key.md)                                         | Identifie une classe. Notez que le ProgID n’est pas garanti globalement unique, contrairement à un CLSID.                 |
| [**ProgID indépendant de la version<>**](-version-independent-progid--key.md) | Utilisé pour déterminer la version la plus récente d’une application d’objet.                                                    |



 

 

 




