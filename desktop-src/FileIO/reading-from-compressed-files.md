---
description: Une application peut décompresser un fichier compressé une partie à la fois à l’aide des fonctions LZSeek et LZRead.
ms.assetid: 9ceec1d4-37cd-4717-a731-dfb9cddb268c
title: Lire à partir de fichiers compressés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c670e1ae473332451df72ddc394a234fa49e64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009862"
---
# <a name="reading-from-compressed-files"></a>Lire à partir de fichiers compressés

Outre la décompression d’un fichier complet en une seule opération, une application peut décompresser un fichier compressé une partie à la fois à l’aide des fonctions [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) et [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) . Ces fonctions sont particulièrement utiles quand il est nécessaire d’extraire des parties de fichiers volumineux. Par exemple, un fabricant de polices peut comporter des fichiers compressés contenant des métriques de police en plus des données de caractères. Pour utiliser les informations contenues dans ces fichiers, une application doit décompresser le fichier ; Toutefois, la plupart des applications utilisent uniquement une partie du fichier à un moment donné. Pour obtenir des informations sur les métriques de police, l’application extrait les données de l’en-tête. Pour récupérer des informations à partir du texte, l’application repositionne le pointeur de fichier en appelant **LZSeek** et en extrayant les données de caractères en appelant **LZRead**.

 

 



