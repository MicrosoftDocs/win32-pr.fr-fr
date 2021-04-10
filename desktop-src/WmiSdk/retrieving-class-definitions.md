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
# <a name="retrieving-class-definitions"></a><span data-ttu-id="43405-103">Récupération de définitions de classe</span><span class="sxs-lookup"><span data-stu-id="43405-103">Retrieving Class Definitions</span></span>

<span data-ttu-id="43405-104">Les requêtes de schéma sont des instructions WQL qui demandent des définitions de classe et des informations sur les [associations de schéma](schema-associations.md).</span><span class="sxs-lookup"><span data-stu-id="43405-104">Schema queries are WQL statements that request class definitions and information about [schema associations](schema-associations.md).</span></span> <span data-ttu-id="43405-105">Les fournisseurs de classes utilisent des requêtes de schéma dans leurs instances de la classe [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) pour spécifier les classes qu’ils prennent en charge lorsqu’ils s’inscrivent auprès de WMI.</span><span class="sxs-lookup"><span data-stu-id="43405-105">Class providers use schema queries in their instances of the [**\_\_ClassProviderRegistration**](--classproviderregistration.md) class to specify the classes that they support when they register with WMI.</span></span> <span data-ttu-id="43405-106">Les requêtes de schéma sont placées dans les propriétés **ResultSetQueries**, **ReferencedSetQueries** et **UnsupportedQueries** de l’instance **\_ \_ ClassProviderRegistration** .</span><span class="sxs-lookup"><span data-stu-id="43405-106">Schema queries are placed in the **ResultSetQueries**, **ReferencedSetQueries**, and **UnsupportedQueries** properties of the **\_\_ClassProviderRegistration** instance.</span></span>

<span data-ttu-id="43405-107">Les requêtes de schéma sont similaires aux requêtes de données en ce qu’elles prennent en charge les instructions WQL suivantes :</span><span class="sxs-lookup"><span data-stu-id="43405-107">Schema queries are similar to data queries in that they support the following WQL statements:</span></span>

-   [<span data-ttu-id="43405-108">SELECT</span><span class="sxs-lookup"><span data-stu-id="43405-108">SELECT</span></span>](select-statement-for-schema-queries.md)
-   [<span data-ttu-id="43405-109">ASSOCIATEURS DE</span><span class="sxs-lookup"><span data-stu-id="43405-109">ASSOCIATORS OF</span></span>](schema-associations.md)
-   [<span data-ttu-id="43405-110">RÉFÉRENCES DE</span><span class="sxs-lookup"><span data-stu-id="43405-110">REFERENCES OF</span></span>](schema-associations.md)
-   [<span data-ttu-id="43405-111">ISA</span><span class="sxs-lookup"><span data-stu-id="43405-111">ISA</span></span>](isa-operator-for-schema-queries.md)

<span data-ttu-id="43405-112">Une requête de schéma est semblable à une requête [de](references-of-statement.md) données qui spécifie le mot clé **ClassDefsOnly** ; en d’autres termes, retourne un jeu de résultats d’objets de définition de classe plutôt que des instances réelles de classes d’association.</span><span class="sxs-lookup"><span data-stu-id="43405-112">A schema query is similar to a [REFERENCES OF](references-of-statement.md) data query that specifies the **ClassDefsOnly** keyword; in other words, that returns a result set of class definition objects rather than actual instances of association classes.</span></span> <span data-ttu-id="43405-113">Toutefois, les références de retournent les définitions de classe uniquement si des instances existent.</span><span class="sxs-lookup"><span data-stu-id="43405-113">However, REFERENCES OF returns class definitions only if there are instances present.</span></span> <span data-ttu-id="43405-114">Une requête de schéma retourne des définitions de classe, qu’il y ait ou non des instances.</span><span class="sxs-lookup"><span data-stu-id="43405-114">A schema query returns class definitions whether or not instances are present.</span></span>

 

 



