---
description: Obtenir la taille allouée ou la taille totale d’un fichier à l’aide de la fonction GetCompressedFileSize ou GetFileSize.
ms.assetid: 1894ea01-49ff-41e3-9912-1cd75966bd3f
title: Obtention de la taille d’un fichier partiellement alloué
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93a1c6a33f0d6913e0e6848e4593ea0e0bf0259
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009885"
---
# <a name="obtaining-the-size-of-a-sparse-file"></a>Obtention de la taille d’un fichier partiellement alloué

Utilisez la fonction [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) pour obtenir la taille réelle allouée sur le disque pour un fichier partiellement alloué. Ce total n’inclut pas la taille des régions qui ont été désallouées, car elles ont été remplies de zéros. Utilisez la fonction [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) pour déterminer la taille totale d’un fichier, y compris la taille des régions éparses qui ont été désallouées.

 

 



