---
description: Une application peut décompresser un fichier compressé une partie à la fois à l’aide des fonctions LZSeek et LZRead.
ms.assetid: 9ceec1d4-37cd-4717-a731-dfb9cddb268c
title: Lire à partir de fichiers compressés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5ccc99aa20fc36f1055f22c01fbd4cab25337badeabbf34b02023889b7f3d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914499"
---
# <a name="reading-from-compressed-files"></a>Lire à partir de fichiers compressés

Outre la décompression d’un fichier complet en une seule opération, une application peut décompresser un fichier compressé une partie à la fois à l’aide des fonctions [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) et [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) . Ces fonctions sont particulièrement utiles quand il est nécessaire d’extraire des parties de fichiers volumineux. Par exemple, un fabricant de polices peut comporter des fichiers compressés contenant des métriques de police en plus des données de caractères. Pour utiliser les informations contenues dans ces fichiers, une application doit décompresser le fichier ; Toutefois, la plupart des applications utilisent uniquement une partie du fichier à un moment donné. Pour obtenir des informations sur les métriques de police, l’application extrait les données de l’en-tête. Pour récupérer des informations à partir du texte, l’application repositionne le pointeur de fichier en appelant **LZSeek** et en extrayant les données de caractères en appelant **LZRead**.

 

 



