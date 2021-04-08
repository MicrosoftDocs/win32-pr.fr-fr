---
title: Génération d’un format non standard
description: Génération d’un format non standard
ms.assetid: e9f80aec-d5dc-4c44-aea0-95220542e48d
keywords:
- Audio Compression Manager (ACM), formats non standard
- ACM (gestionnaire de compression audio), formats non standard
- Exemples ACM, formats non standard
- acmFormatSuggest fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e775fb09f926e0380b8141101b816b0dcbb221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839933"
---
# <a name="generating-a-nonstandard-format"></a>Génération d’un format non standard

Parfois, une application a besoin d’un format non standard. Par exemple, une application peut nécessiter un fichier au format ADPCM 16 kHz. Étant donné que 16 kHz n’est pas standard, les fonctions d’énumération ne génèrent pas ce format. En fait, peu de codage personnalisé des algorithmes de format dans l’application, il n’existe pas de méthode fiable pour générer un format non standard. Toutefois, il est parfois possible de générer un format analogue en configurant un format PCM valide avec toutes les informations requises, puis en utilisant la fonction [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) . Étant donné que les compresseurs et les décompresseurs essaient de suggérer un format le plus proche du format souhaité, le nombre de canaux et la fréquence sont généralement préservés.

 

 




