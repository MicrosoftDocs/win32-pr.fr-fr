---
description: Écriture de filtres de capture
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Écriture de filtres de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa4807f381dc925a68fa3c60e45d5c8c5c444653230f366895b370e97aaccb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049089"
---
# <a name="writing-capture-filters"></a>Écriture de filtres de capture

l’écriture d’un filtre de capture audio ou vidéo pour DirectShow n’est pas recommandée. au lieu de cela, DirectShow fournit une prise en charge automatique des périphériques de capture audio et vidéo, à l’aide de filtres de wrapper et de l' [énumérateur de périphérique système](system-device-enumerator.md). pour plus d’informations sur l’implémentation d’un pilote de périphérique, reportez-vous à la documentation de Windows driver Kit (WDK).

Cette section est destinée uniquement aux développeurs qui ont besoin de capturer des données personnalisées à partir d’un périphérique matériel inhabituel.

Cet article contient les sections suivantes :

-   [Exigences de code confidentiel pour les filtres de capture](pin-requirements-for-capture-filters.md)
-   [Implémentation d’un pin d’aperçu (facultatif)](implementing-a-preview-pin--optional.md)
-   [Génération de données dans un filtre de capture](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[écriture de filtres de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



