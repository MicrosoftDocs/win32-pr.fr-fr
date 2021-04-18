---
description: 'Les requêtes de données sont des instructions WQL qui demandent des instances de classes. Pour émettre une requête de données, les applications appellent la méthode IWbemServices :: ExecQuery ou IWbemServices :: ExecQueryAsync.'
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: Demande de données d’instance de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32df053ae1267f396978d98271f57f174ea6bf0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526297"
---
# <a name="requesting-class-instance-data"></a><span data-ttu-id="7423c-104">Demande de données d’instance de classe</span><span class="sxs-lookup"><span data-stu-id="7423c-104">Requesting Class Instance Data</span></span>

<span data-ttu-id="7423c-105">Les requêtes de données sont des instructions WQL qui demandent des instances de classes.</span><span class="sxs-lookup"><span data-stu-id="7423c-105">Data queries are WQL statements that request instances of classes.</span></span> <span data-ttu-id="7423c-106">Pour émettre une requête de données, les applications appellent la méthode [**IWbemServices :: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) ou [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="7423c-106">To issue a data query, applications call the [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) or [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method.</span></span>

<span data-ttu-id="7423c-107">Les instructions suivantes sont utilisées pour effectuer des requêtes de données :</span><span class="sxs-lookup"><span data-stu-id="7423c-107">The following statements are used to make data queries:</span></span>

-   [<span data-ttu-id="7423c-108">SELECT</span><span class="sxs-lookup"><span data-stu-id="7423c-108">SELECT</span></span>](select-statement-for-data-queries.md)
-   [<span data-ttu-id="7423c-109">ASSOCIATEURS DE</span><span class="sxs-lookup"><span data-stu-id="7423c-109">ASSOCIATORS OF</span></span>](associators-of-statement.md)
-   [<span data-ttu-id="7423c-110">RÉFÉRENCES DE</span><span class="sxs-lookup"><span data-stu-id="7423c-110">REFERENCES OF</span></span>](references-of-statement.md)
-   [<span data-ttu-id="7423c-111">ISA</span><span class="sxs-lookup"><span data-stu-id="7423c-111">ISA</span></span>](isa-operator-for-data-queries.md)

<span data-ttu-id="7423c-112">L’instruction WQL SELECT est l’instruction langage SQL standard (SQL) pour la récupération d’informations, avec quelques restrictions et extensions spécifiques à WQL.</span><span class="sxs-lookup"><span data-stu-id="7423c-112">The WQL SELECT statement is the standard Structured Query Language (SQL) statement for retrieving information, with a few restrictions and extensions specific to WQL.</span></span> <span data-ttu-id="7423c-113">Bien que l’instruction SQL SELECT soit généralement utilisée dans l’environnement de base de données pour récupérer des colonnes particulières de tables, l’instruction WQL SELECT est utilisée dans WMI pour récupérer les instances d’une classe unique.</span><span class="sxs-lookup"><span data-stu-id="7423c-113">Although the SQL SELECT statement is typically used in the database environment to retrieve particular columns from tables, the WQL SELECT statement is used in WMI to retrieve instances of a single class.</span></span> <span data-ttu-id="7423c-114">WQL ne prend pas en charge les requêtes sur plusieurs classes.</span><span class="sxs-lookup"><span data-stu-id="7423c-114">WQL does not support queries across multiple classes.</span></span>

<span data-ttu-id="7423c-115">Les ASSOCIateurs et les références d’instructions sont spécifiques à WQL et ne font pas partie du SQL standard.</span><span class="sxs-lookup"><span data-stu-id="7423c-115">The ASSOCIATORS OF and REFERENCES OF statements are specific to WQL and are not part of standard SQL.</span></span> <span data-ttu-id="7423c-116">Les ASSOCIateurs de l’instruction récupèrent toutes les instances de classe qui sont associées à une instance de classe source particulière, et les références de récupèrent toutes les instances qui font référence à une instance source particulière.</span><span class="sxs-lookup"><span data-stu-id="7423c-116">The ASSOCIATORS OF statement retrieves all class instances that are associated with a particular source class instance, and REFERENCES OF retrieves all instances that refer to a particular source instance.</span></span> <span data-ttu-id="7423c-117">Les associations sont représentées par des instances d’une [classe d’association](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="7423c-117">Associations are represented by instances of an [association class](declaring-an-association-class.md).</span></span>

 

 



