---
title: À propos des informations de version
description: Cette rubrique décrit les fonctions d’informations de version.
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- ressources, informations sur la version
- informations de version
- ajouter des informations sur la version
- conflits de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25bf5c0914ba28b9a5178f99a94f83f57ac99550
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235745"
---
# <a name="about-version-information"></a>À propos des informations de version

Vous pouvez utiliser les fonctions d’informations de version pour déterminer l’emplacement d’installation d’un fichier et identifier les conflits avec les fichiers actuellement installés. Ces fonctions vous permettent d’éviter les problèmes suivants :

-   installation de versions antérieures de composants sur des versions plus récentes
-   modification de la langue dans un système mixte sans notification
-   installation de plusieurs copies d’une bibliothèque dans des répertoires différents
-   copie de fichiers dans des répertoires réseau partagés par plusieurs utilisateurs

Les fonctions d’informations de version permettent aux applications d’interroger une ressource de version pour obtenir des informations sur les fichiers et de présenter les informations dans un format clair. Ces informations incluent l’objectif du fichier, son auteur, son numéro de version, etc.

vous pouvez ajouter des informations de version à tous les fichiers qui peuvent avoir des ressources Windows, telles que des dll, des fichiers exécutables ou des fichiers de police. fon. Pour ajouter les informations, créez une [ressource VERSIONINFO](/windows/desktop/menurc/versioninfo-resource) et utilisez le compilateur de ressources pour compiler la ressource.

 

 