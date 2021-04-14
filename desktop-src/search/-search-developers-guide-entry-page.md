---
description: Des tiers peuvent créer des applications qui interrogent l’index sur les données par programme et peuvent étendre Windows Search pour indexer les données des formats de fichiers personnalisés et des magasins de données.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Guide du développeur Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61593f47e081059966936a99a7d2baea114df92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484441"
---
# <a name="windows-search-developers-guide"></a>Guide du développeur Windows Search

Des tiers peuvent créer des applications qui interrogent l’index sur les données par programme et peuvent étendre Windows Search pour indexer les données des formats de fichiers personnalisés et des magasins de données. Pour créer des applications de recherche Windows, les développeurs tiers doivent tout d’abord implémenter un magasin de données Shell pour obtenir une expérience utilisateur raisonnable. Pour plus d’informations, consultez [implémentation des interfaces d’objets de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Vous devez également télécharger le [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) pour les bibliothèques de recherche Windows. Les [exemples du kit de développement logiciel (SDK) Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contiennent des exemples de code utiles et un assembly d’interopérabilité pour le développement avec du code managé. Pour plus d’informations sur l’utilisation des exemples de code, consultez [exemples de code Windows Search](-search-3x-wds-sampleentry.md).

Cette section est organisée comme suit :

- [Gestion de l’index](-search-3x-wds-mngidx-overview.md)
- [Interrogation de l’index programmatiquement](-search-3x-wds-qryidx-overview.md)
- [Extension de l’index](-search-3x-wds-extidx-overview.md)
- [Extension des ressources linguistiques](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a>Ressources supplémentaires

- Pour obtenir des forums de discussion et des questions sur les technologies de recherche prises en charge par la Communauté, consultez le [forum MSDN : développement de Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
- Pour télécharger les exemples de code de recherche :
  - [Exemples de recherche Windows](-search-samples-ovw.md)
- Pour télécharger les SDK Windows :
  - Pour Windows 10 : [SDK Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)
  - Pour Windows 7 : [SDK Windows pour Windows 7 et .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

## <a name="related-topics"></a>Rubriques connexes

[Vue d’ensemble de Windows Search](-search-3x-wds-overview.md)

[Référence de recherche Windows](-search-reference-entry-page.md)

[Exemples de code Windows Search](-search-samples-ovw.md)

[Recherche fédérée dans Windows](-search-federated-search-overview.md)

[Technologies de recherche associées](-search-3x-wds-sampleentry.md)

[Glossaire Windows Search](search-glossary.md)
