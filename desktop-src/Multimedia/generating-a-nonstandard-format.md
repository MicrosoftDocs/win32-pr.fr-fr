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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364055"
---
# <a name="generating-a-nonstandard-format"></a>Génération d’un format non standard

Parfois, une application a besoin d’un format non standard. Par exemple, une application peut nécessiter un fichier au format ADPCM 16 kHz. Étant donné que 16 kHz n’est pas standard, les fonctions d’énumération ne génèrent pas ce format. En fait, peu de codage personnalisé des algorithmes de format dans l’application, il n’existe pas de méthode fiable pour générer un format non standard. Toutefois, il est parfois possible de générer un format analogue en configurant un format PCM valide avec toutes les informations requises, puis en utilisant la fonction [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) . Étant donné que les compresseurs et les décompresseurs essaient de suggérer un format le plus proche du format souhaité, le nombre de canaux et la fréquence sont généralement préservés.

 

 




