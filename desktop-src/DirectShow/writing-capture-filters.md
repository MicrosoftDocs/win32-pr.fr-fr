---
description: Écriture de filtres de capture
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Écriture de filtres de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1a64de2b56dbc0728432307036fc46387f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534575"
---
# <a name="writing-capture-filters"></a>Écriture de filtres de capture

L’écriture d’un filtre de capture audio ou vidéo pour DirectShow n’est pas recommandée. Au lieu de cela, DirectShow assure la prise en charge automatique des périphériques de capture audio et vidéo à l’aide de filtres de wrapper et de l' [énumérateur de périphérique système](system-device-enumerator.md). Pour plus d’informations sur l’implémentation d’un pilote de périphérique, reportez-vous à la documentation de Windows Driver Kit (WDK).

Cette section est destinée uniquement aux développeurs qui ont besoin de capturer des données personnalisées à partir d’un périphérique matériel inhabituel.

Cet article contient les sections suivantes :

-   [Exigences de code confidentiel pour les filtres de capture](pin-requirements-for-capture-filters.md)
-   [Implémentation d’un pin d’aperçu (facultatif)](implementing-a-preview-pin--optional.md)
-   [Génération de données dans un filtre de capture](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture de filtres DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



