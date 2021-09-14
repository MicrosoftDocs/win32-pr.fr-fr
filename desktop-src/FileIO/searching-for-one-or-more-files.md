---
description: Une application peut rechercher dans le répertoire actif tous les noms de fichiers qui correspondent à un modèle donné à l’aide des fonctions FindFirstFile, FindFirstFileEx, FindNextFile et FindClose.
ms.assetid: 7edd6c6e-7e8a-415c-866b-2283e5596a62
title: Recherche d’un ou plusieurs fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c5825b418221b1af429c6c0a731446d627701c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009848"
---
# <a name="searching-for-one-or-more-files"></a>Recherche d’un ou plusieurs fichiers

Une application peut rechercher dans le répertoire actif tous les noms de fichiers qui correspondent à un modèle donné à l’aide des fonctions [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)et [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) . Le modèle doit être un nom de fichier valide et peut inclure des caractères génériques.

Les fonctions [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) et [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) créent des handles que **FindFirstFileEx** utilise pour rechercher d’autres fichiers avec le même modèle. Toutes les fonctions retournent des informations sur le fichier qui a été trouvé. Ces informations incluent le nom, la taille, les attributs et l’heure du fichier.

La fonction [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) permet également à une application de rechercher des fichiers en fonction de critères de recherche supplémentaires. La fonction peut limiter les recherches à des noms de périphériques ou de répertoires.

La fonction [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) détruit les handles créés par [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) et [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).

Une application peut rechercher un seul fichier sur un chemin d’accès spécifique à l’aide de la fonction [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) .

 

 
