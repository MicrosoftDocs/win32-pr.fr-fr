---
description: Le service de détection de langage ELS est appelé Microsoft Détection de langue. Ce service utilise la technologie brevetée par Microsoft pour permettre aux applications de détecter la langue dans laquelle un texte spécifique est écrit.
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Détection de langue Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472c4c4df0484287ef8bebcfdb2f395212b1985b282b7391d6c047dfb98d2ed8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788379"
---
# <a name="microsoft-language-detection"></a>Détection de langue Microsoft

Le service de détection de langage ELS est appelé Microsoft Détection de langue. Ce service utilise la technologie brevetée par Microsoft pour permettre aux applications de détecter la langue dans laquelle un texte spécifique est écrit.

## <a name="input-to-microsoft-language-detection"></a>Entrée à Microsoft Détection de langue

L’entrée du service de Détection de langue Microsoft est le texte UTF-16 (formulaire normalisé C). Le service doit déterminer la langue de ce texte.

## <a name="output-of-microsoft-language-detection"></a>Sortie de Microsoft Détection de langue

Le service de Détection de langue Microsoft récupère une liste de chaînes UTF-16 se terminant par un caractère null, représentée par leurs noms, séparés par des délimiteurs de caractères null. La liste est triée par pertinence. Pour la plupart des langues, des noms neutres sont utilisés. Toutefois, pour certains, par exemple SR-Cyrl, SR-LATN, zh-Hant et zh-Hans, les noms complets sont utilisés.

## <a name="microsoft-language-detection-operation"></a>Opération de Détection de langue Microsoft

Le service de Détection de langue Microsoft vérifie le script Unicode du texte fourni par l’application. Il segmente le texte en fonction des scripts qu’il détecte, puis détermine la langue dans laquelle chaque segment est écrit. Si un script indique une seule langue, il est garanti que la langue est présente dans la liste des langages de sortie. Le service utilise un algorithme breveté pour déterminer la pertinence de chaque langue prise en charge.

## <a name="microsoft-language-detection-guid"></a>GUID de Microsoft Détection de langue

Le GUID du service de Détection de langue Microsoft est déclaré dans Elssrvc. h, comme indiqué dans le code suivant.


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des services linguistiques étendus](about-extended-linguistic-services.md)
</dt> </dl>

 

 



