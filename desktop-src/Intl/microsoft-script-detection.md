---
description: Le service de détection de script ELS est appelé détection de script Microsoft.
ms.assetid: daf9f549-1eff-4666-b777-227ec31fba30
title: Détection de scripts Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd38b36cb409c1f03d84b9fc21f2fe4439b8152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114195"
---
# <a name="microsoft-script-detection"></a>Détection de scripts Microsoft

Le service de détection de script ELS est appelé détection de script Microsoft. Ce service permet aux applications de détecter les scripts dans lesquels le texte est écrit. L’équivalent NLS (National Language Support) d’un service de détection de script est la fonction [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) . Toutefois, le service ELS récupère également les plages de texte qui appartiennent à chaque système d’écriture.

## <a name="input-to-microsoft-script-detection"></a>Entrée de la détection de scripts Microsoft

L’entrée du service de détection de script Microsoft est du texte UTF-16 pour lequel le service détermine des plages de scripts.

## <a name="output-of-microsoft-script-detection"></a>Sortie de la détection de scripts Microsoft

La sortie du service de détection de script Microsoft est un tableau de plages, chacune contenant une chaîne UTF-16 terminée par un caractère NULL avec le nom spécifié au format Unicode du système d’écriture associé. Le service signale les caractères communs standard (ZYYY) et hérité (Qaai) comme appartenant à la plage de scripts précédente. Le début des caractères communs et hérités sont signalés comme appartenant à la plage de scripts suivante. Si tous les caractères du texte d’entrée sont communs ou hérités, la sortie du service est une plage unique avec la chaîne vide en tant que données.

## <a name="microsoft-script-detection-operation"></a>Opération de détection de script Microsoft

Le service de détection de script Microsoft mappe les points de code appartenant à la plage commune au système d’écriture précédent. Le service peut également mapper les points de code au système d’écriture suivant si les points de code sont au début de la chaîne d’entrée. L’application n’a pas à gérer la plage commune du tout.

## <a name="microsoft-script-detection-guid"></a>GUID de détection de script Microsoft

Le GUID du service de Détection de langue Microsoft est déclaré dans Elssrvc. h, comme indiqué dans le code suivant.


```C++
// {2D64B439-6CAF-4f6b-B688-E5D0F4FAA7D7}
static const GUID ELS_GUID_SCRIPT_DETECTION =
    { 0x2D64B439, 0x6CAF, 0x4F6B, { 0xB6, 0x88, 0xE5, 0xD0, 0xF4, 0xFA, 0xA7, 0xD7 } };
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des services linguistiques étendus](about-extended-linguistic-services.md)
</dt> </dl>

 

 



