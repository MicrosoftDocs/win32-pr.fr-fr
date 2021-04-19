---
description: Décrit les opérateurs WQL utilisés dans la clause WHERE ou l’instruction SELECT.
ms.assetid: a62de66d-d5ba-49a1-8262-bfa10ac2db75
ms.tgt_platform: multiple
title: Opérateurs WQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5cc37d03884a3609abf3f76d2c78ba22b3c9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527931"
---
# <a name="wql-operators"></a><span data-ttu-id="72a07-103">Opérateurs WQL</span><span class="sxs-lookup"><span data-stu-id="72a07-103">WQL Operators</span></span>

<span data-ttu-id="72a07-104">Le langage WQL (Windows Management Instrumentation Query Language) prend en charge un ensemble d’opérateurs standard utilisés dans la [clause WHERE](where-clause.md) d’une instruction SELECT, comme suit.</span><span class="sxs-lookup"><span data-stu-id="72a07-104">The Windows Management Instrumentation Query Language (WQL) supports a set of standard operators that are used in the [WHERE clause](where-clause.md) of a SELECT statement, as follows.</span></span>



| <span data-ttu-id="72a07-105">Opérateur</span><span class="sxs-lookup"><span data-stu-id="72a07-105">Operator</span></span>       | <span data-ttu-id="72a07-106">Description</span><span class="sxs-lookup"><span data-stu-id="72a07-106">Description</span></span>              |
|----------------|--------------------------|
| =              | <span data-ttu-id="72a07-107">Égal à</span><span class="sxs-lookup"><span data-stu-id="72a07-107">Equal to</span></span>                 |
| <           | <span data-ttu-id="72a07-108">Inférieur à</span><span class="sxs-lookup"><span data-stu-id="72a07-108">Less than</span></span>                |
| >           | <span data-ttu-id="72a07-109">Supérieur à</span><span class="sxs-lookup"><span data-stu-id="72a07-109">Greater than</span></span>             |
| <=          | <span data-ttu-id="72a07-110">Inférieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="72a07-110">Less than or equal to</span></span>    |
| >=          | <span data-ttu-id="72a07-111">Supérieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="72a07-111">Greater than or equal to</span></span> |
| <span data-ttu-id="72a07-112">! = ou <></span><span class="sxs-lookup"><span data-stu-id="72a07-112">!= or <></span></span> | <span data-ttu-id="72a07-113">Différent de</span><span class="sxs-lookup"><span data-stu-id="72a07-113">Not equal to</span></span>             |



 

<span data-ttu-id="72a07-114">Il existe quelques opérateurs supplémentaires spécifiques à WQL : est, n’est pas, ISA et LIKE.</span><span class="sxs-lookup"><span data-stu-id="72a07-114">There are a few additional WQL-specific operators: IS, IS NOT, ISA, and LIKE.</span></span> <span data-ttu-id="72a07-115">Les opérateurs IS et IS NOT ne sont valides dans la clause WHERE que si la constante est **null**.</span><span class="sxs-lookup"><span data-stu-id="72a07-115">The IS and IS NOT operators are valid in the WHERE clause only if the constant is **NULL**.</span></span> <span data-ttu-id="72a07-116">Par exemple, les requêtes suivantes sont valides :</span><span class="sxs-lookup"><span data-stu-id="72a07-116">For example, the following queries are valid:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



<span data-ttu-id="72a07-117">Les requêtes suivantes montrent des utilisations non valides de IS et NOT :</span><span class="sxs-lookup"><span data-stu-id="72a07-117">The following queries show invalid uses of IS and IS NOT:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



<span data-ttu-id="72a07-118">L’opérateur ISA est utilisé dans la clause WHERE des requêtes de données et d’événements pour tester des objets incorporés pour une hiérarchie de classes.</span><span class="sxs-lookup"><span data-stu-id="72a07-118">The ISA operator is used in the WHERE clause of data and event queries to test embedded objects for a class hierarchy.</span></span> <span data-ttu-id="72a07-119">L’opérateur ISA élimine la nécessité d’effectuer le suivi des classes récemment dérivées lors de la demande d’une hiérarchie de classes.</span><span class="sxs-lookup"><span data-stu-id="72a07-119">The ISA operator eliminates the need for keeping track of newly derived classes when requesting a hierarchy of classes.</span></span> <span data-ttu-id="72a07-120">Lorsque vous utilisez ISA, les sous-classes nouvellement créées et existantes de la classe demandée sont automatiquement incluses dans le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="72a07-120">When you use ISA, newly created and existing subclasses of the requested class are automatically included in the result set.</span></span>

<span data-ttu-id="72a07-121">Pour plus d’informations sur la syntaxe et l’utilisation de cet opérateur, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="72a07-121">For more information about the syntax and use of this operator, see the following topics:</span></span>

-   [<span data-ttu-id="72a07-122">Opérateur ISA pour les requêtes de données</span><span class="sxs-lookup"><span data-stu-id="72a07-122">ISA Operator for Data Queries</span></span>](isa-operator-for-data-queries.md)
-   [<span data-ttu-id="72a07-123">Opérateur ISA pour les requêtes d’événements</span><span class="sxs-lookup"><span data-stu-id="72a07-123">ISA Operator for Event Queries</span></span>](isa-operator-for-event-queries.md)
-   [<span data-ttu-id="72a07-124">Opérateur ISA pour les requêtes de schéma</span><span class="sxs-lookup"><span data-stu-id="72a07-124">ISA Operator for Schema Queries</span></span>](isa-operator-for-schema-queries.md)

<span data-ttu-id="72a07-125">L’opérateur LIKE est valide dans la clause WHERE et est utilisé pour déterminer si une chaîne de caractères donnée correspond à un modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="72a07-125">The LIKE operator is valid in the WHERE clause and is used to determine whether a given character string matches a specified pattern.</span></span> <span data-ttu-id="72a07-126">Par exemple, la requête suivante retourne toutes les instances de \_ classes Win32.</span><span class="sxs-lookup"><span data-stu-id="72a07-126">For example, the following query returns all instances of Win32\_ classes.</span></span>


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



<span data-ttu-id="72a07-127">Pour plus d’informations sur la syntaxe et l’utilisation de cet opérateur, consultez [Like, opérateur](like-operator.md).</span><span class="sxs-lookup"><span data-stu-id="72a07-127">For more information about the syntax and use of this operator, see [LIKE Operator](like-operator.md).</span></span>

 

 



