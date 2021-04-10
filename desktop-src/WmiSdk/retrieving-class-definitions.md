---
description: Les requêtes de schéma sont des instructions WQL qui demandent des définitions de classe et des informations sur les associations de schéma.
ms.assetid: cb65e99f-9046-4c63-ab56-60dedc45bcef
ms.tgt_platform: multiple
title: Récupération de définitions de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d865b1a85eefa7e67b12ed4c0acc16ea9e19f9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114895"
---
# <a name="retrieving-class-definitions"></a>Récupération de définitions de classe

Les requêtes de schéma sont des instructions WQL qui demandent des définitions de classe et des informations sur les [associations de schéma](schema-associations.md). Les fournisseurs de classes utilisent des requêtes de schéma dans leurs instances de la classe [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) pour spécifier les classes qu’ils prennent en charge lorsqu’ils s’inscrivent auprès de WMI. Les requêtes de schéma sont placées dans les propriétés **ResultSetQueries**, **ReferencedSetQueries** et **UnsupportedQueries** de l’instance **\_ \_ ClassProviderRegistration** .

Les requêtes de schéma sont similaires aux requêtes de données en ce qu’elles prennent en charge les instructions WQL suivantes :

-   [SELECT](select-statement-for-schema-queries.md)
-   [ASSOCIATEURS DE](schema-associations.md)
-   [RÉFÉRENCES DE](schema-associations.md)
-   [ISA](isa-operator-for-schema-queries.md)

Une requête de schéma est semblable à une requête [de](references-of-statement.md) données qui spécifie le mot clé **ClassDefsOnly** ; en d’autres termes, retourne un jeu de résultats d’objets de définition de classe plutôt que des instances réelles de classes d’association. Toutefois, les références de retournent les définitions de classe uniquement si des instances existent. Une requête de schéma retourne des définitions de classe, qu’il y ait ou non des instances.

 

 



