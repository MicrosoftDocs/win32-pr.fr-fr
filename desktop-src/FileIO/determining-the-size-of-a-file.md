---
description: La fonction GetFileSize récupère la taille d’un fichier.
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: Détermination de la taille d’un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf4185d0bb695d73dc3afd03bb1ee7d6fe95cf606960fbdc41c4ce0b33b732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150612"
---
# <a name="determining-the-size-of-a-file"></a>Détermination de la taille d’un fichier

La fonction [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) récupère la taille d’un fichier.

Étant donné que l’implémentation de fichiers du système de fichiers NTFS autorise plusieurs flux dans un fichier, toute application que vous écrivez et qui accède à des fichiers doit tenir compte du fait que le créateur du fichier peut inclure plusieurs flux dans le fichier. Si plusieurs flux ne sont pas vérifiés dans un fichier, l’application peut sous-estimer la taille totale du fichier, entre autres erreurs.

 

 



