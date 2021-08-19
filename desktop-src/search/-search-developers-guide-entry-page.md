---
description: des tiers peuvent créer des applications qui interrogent l’index sur les données par programme et peuvent étendre Windows recherche pour indexer les données à partir de formats de fichiers personnalisés et de magasins de données.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Windows Rechercher dans le Guide du développeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84773f23f5e82ce5cbb15c163b0ff2421f9b7c92b18129c9875729be37518b02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117864188"
---
# <a name="windows-search-developers-guide"></a>Windows Rechercher dans le Guide du développeur

des tiers peuvent créer des applications qui interrogent l’index sur les données par programme et peuvent étendre Windows recherche pour indexer les données à partir de formats de fichiers personnalisés et de magasins de données. pour créer des applications de recherche Windows, les développeurs tiers doivent tout d’abord implémenter un magasin de données Shell pour obtenir une expérience utilisateur raisonnable. Pour plus d’informations, consultez [implémentation des interfaces d’objets de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

vous devez également télécharger les [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) pour les bibliothèques de recherche Windows. les [exemples du kit de développement logiciel (SDK) Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contiennent des exemples de code utiles et un assembly d’interopérabilité pour le développement avec du code managé. pour plus d’informations sur l’utilisation des exemples de code, consultez [Windows des exemples de code de recherche](-search-3x-wds-sampleentry.md).

Cette section est organisée comme suit :

- [Gestion de l’index](-search-3x-wds-mngidx-overview.md)
- [Interrogation de l’index programmatiquement](-search-3x-wds-qryidx-overview.md)
- [Extension de l’index](-search-3x-wds-extidx-overview.md)
- [Extension des ressources linguistiques](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a>Ressources supplémentaires

- pour obtenir des forums de discussion et des questions sur les technologies de recherche prises en charge par la communauté, consultez le [Forum MSDN : Windows Desktop search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
- Pour télécharger les exemples de code de recherche :
  - [Windows Exemples de recherche](-search-samples-ovw.md)
- pour télécharger les SDK Windows :
  - pour Windows 10 : [kit de développement logiciel (SDK) Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)
  - pour Windows 7 : [SDK Windows pour Windows 7 et .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

## <a name="related-topics"></a>Rubriques connexes

[Vue d’ensemble de Windows Search](-search-3x-wds-overview.md)

[Windows Référence de recherche](-search-reference-entry-page.md)

[Windows Rechercher des exemples de code](-search-samples-ovw.md)

[Recherche fédérée dans Windows](-search-federated-search-overview.md)

[Technologies de recherche associées](-search-3x-wds-sampleentry.md)

[Windows Rechercher dans le Glossaire](search-glossary.md)
