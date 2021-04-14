---
title: Licences
description: Licences
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- Windows Media Format SDK, licences DRM
- Windows Media Format SDK, licences pour DRM
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), gestion des licences de fichiers protégés
- DRM (gestion des droits numériques), gestion des licences de fichiers protégés
- licences, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fbf2d7c0a25b2b19241d90743f43f46a71d7e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311260"
---
# <a name="licenses"></a>Licences

Une licence est un ensemble de données décrivant les conditions dans lesquelles les données des fichiers protégés peuvent être lues. Chaque licence s’applique à un identificateur de clé, qui est généralement affecté à un seul fichier multimédia. Cet identificateur est utilisé pour identifier le contenu protégé de la licence.

Chaque licence spécifie une ou plusieurs actions qui peuvent être effectuées avec le contenu protégé. Ces actions, également appelées droits, peuvent être limitées de plusieurs façons. En associant les dates de début, les dates de fin, les nombres et les limites de temps, l’émetteur de licence peut créer quasiment n’importe quelle limitation imaginaire sur un droit.

Les licences sont émises par un service Web. Lorsqu’une licence est acquise, elle est stockée sur l’ordinateur client dans le magasin de licences local, qui est un fichier protégé qui contient des licences et d’autres données DRM. Quand une application accède au contenu protégé, le sous-système DRM recherche une licence qui accorde le droit approprié dans le magasin de licences local. Si aucune licence n’est trouvée, l’application peut en acquérir une en fonction des informations stockées dans l’en-tête DRM du fichier.

Plusieurs licences peuvent être émises pour le même fichier protégé. Lorsque le sous-système DRM détermine si une action est autorisée, il agrège les droits de toutes les licences qui s’appliquent. Une priorité peut être affectée à chaque licence. Si plusieurs licences s’appliquent à une action, la licence dont la priorité est la plus élevée est vérifiée pour déterminer si les nombres doivent être décrémentée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Concepts**](drmconcepts.md)
</dt> </dl>

 

 




