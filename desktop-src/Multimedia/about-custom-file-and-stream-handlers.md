---
title: À propos des gestionnaires de fichiers et de flux personnalisés
description: À propos des gestionnaires de fichiers et de flux personnalisés
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
keywords:
- Video for Windows (VFW), gestionnaires de fichiers personnalisés
- Video for Windows (VFW), gestionnaires de flux personnalisés
- Video for Windows (VFW), gestionnaires de fichiers
- Video for Windows (VFW), gestionnaires de flux
- VFW (vidéo pour Windows), gestionnaires de fichiers personnalisés
- VFW (vidéo pour Windows), gestionnaires de flux personnalisés
- VFW (vidéo pour Windows), gestionnaires de fichiers
- VFW (vidéo pour Windows), gestionnaires de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e1872aa8a2f5c55df0db43860e318c792801e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840801"
---
# <a name="about-custom-file-and-stream-handlers"></a>À propos des gestionnaires de fichiers et de flux personnalisés

Votre application peut utiliser un gestionnaire de fichiers personnalisé pour lire un fichier ou écrire dans un fichier dont le format n’est pas standard. Pour ce faire, votre application utilise simplement le nom de votre gestionnaire de fichiers lors de l’ouverture du fichier ou de l’allocation de l’interface de fichier. La bibliothèque AVIFile utilise ensuite les fonctions de votre gestionnaire de fichiers au lieu de celles d’un autre gestionnaire de fichiers. Le format non standard apparaît sous forme de données AVI standard pour votre application ou toute autre application à l’aide de votre gestionnaire de fichiers personnalisé.

De même, votre application peut utiliser un gestionnaire de flux personnalisé pour lire un flux dans un format non standard. Un flux, qu’il s’agisse de données audio, vidéo, MIDI, de texte ou de données personnalisées, est un composant d’un fichier AVI. Par exemple, un fichier AVI qui contient une séquence vidéo, une bande son anglaise et une bande son française sont constitués de trois flux. Votre application peut spécifier les flux dans un fichier AVI pour traiter et diriger chacun de ces flux vers un gestionnaire qui peut traiter de façon optimale le type approprié de données multimédias.

> [!Note]  
> Vous devez placer des gestionnaires de fichiers et de flux personnalisés dans une ou plusieurs dll, séparés des fichiers d’application principaux.

 

 

 




