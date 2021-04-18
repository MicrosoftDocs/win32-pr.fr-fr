---
description: Les requêtes d’événement sont utilisées par les consommateurs d’événements temporaires, les consommateurs d’événements permanents et les fournisseurs d’événements. Les consommateurs d’événements utilisent des requêtes d’événements pour spécifier des événements intéressants, et les fournisseurs d’événements utilisent les requêtes pour spécifier les événements qu’ils fournissent.
ms.assetid: 851ad9bd-2604-4988-8de0-8d29b5300b21
ms.tgt_platform: multiple
title: Réception des notifications d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43873c03155f2186f9d3a9a3daff9b8e322e511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540843"
---
# <a name="receiving-event-notifications"></a><span data-ttu-id="7bc5d-104">Réception des notifications d’événements</span><span class="sxs-lookup"><span data-stu-id="7bc5d-104">Receiving Event Notifications</span></span>

<span data-ttu-id="7bc5d-105">Les requêtes d’événement sont utilisées par les consommateurs d’événements temporaires, les consommateurs d’événements permanents et les fournisseurs d’événements.</span><span class="sxs-lookup"><span data-stu-id="7bc5d-105">Event queries are used by temporary event consumers, permanent event consumers, and event providers.</span></span> <span data-ttu-id="7bc5d-106">Les consommateurs d’événements utilisent des requêtes d’événements pour spécifier des événements intéressants, et les fournisseurs d’événements utilisent les requêtes pour spécifier les événements qu’ils fournissent.</span><span class="sxs-lookup"><span data-stu-id="7bc5d-106">Event consumers use event queries to specify events of interest, and event providers use the queries to specify the events that they provide.</span></span>

<span data-ttu-id="7bc5d-107">Les [consommateurs temporaires](receiving-events-for-the-duration-of-your-application.md) placent les requêtes dans les appels à la méthode [**IWbemServices :: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) ou [**IWbemServices :: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="7bc5d-107">[Temporary consumers](receiving-events-for-the-duration-of-your-application.md) place queries in calls to the [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) or [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method.</span></span> <span data-ttu-id="7bc5d-108">Les [consommateurs d’événements permanents](receiving-events-at-all-times.md) placent les requêtes dans la propriété **query** d’une instance de la classe système [**\_ \_ EventFilter**](--eventfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="7bc5d-108">[Permanent event consumers](receiving-events-at-all-times.md) place queries in the **Query** property of an instance of the [**\_\_EventFilter**](--eventfilter.md) system class.</span></span>

<span data-ttu-id="7bc5d-109">Les [fournisseurs d’événements](writing-an-event-provider.md) utilisent des requêtes d’événement pour s’inscrire afin de prendre en charge un ou plusieurs types d’événements.</span><span class="sxs-lookup"><span data-stu-id="7bc5d-109">[Event providers](writing-an-event-provider.md) use event queries to register to support one or more types of events.</span></span> <span data-ttu-id="7bc5d-110">Elles placent les requêtes dans la propriété **EventQueryList** d’une instance de la classe système [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="7bc5d-110">They place queries in the **EventQueryList** property of an instance of the [**\_\_EventProviderRegistration**](--eventproviderregistration.md) system class.</span></span> <span data-ttu-id="7bc5d-111">Tous les fournisseurs d’événements créent une instance **\_ \_ EventProviderRegistration** à inscrire auprès d’Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="7bc5d-111">All event providers create an **\_\_EventProviderRegistration** instance to register with Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="7bc5d-112">Pour plus d’informations, consultez [inscription d’un fournisseur d’événements](registering-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7bc5d-112">For more information, see [Registering an Event Provider](registering-an-event-provider.md).</span></span>

<span data-ttu-id="7bc5d-113">Les consommateurs et les fournisseurs d’événements utilisent l' [instruction SELECT](select-statement-for-event-queries.md) et une clause WHERE associée pour les requêtes d’événements, ainsi qu’une variété d’extensions spécifiques au langage de requêtes WMI (WQL) (WQL).</span><span class="sxs-lookup"><span data-stu-id="7bc5d-113">Event consumers and providers use the [SELECT statement](select-statement-for-event-queries.md) and a related WHERE clause for event queries, plus a variety of extensions specific to the WMI Query Language (WQL).</span></span> <span data-ttu-id="7bc5d-114">Les extensions sont utilisées pour empêcher les consommateurs d’être submergés par des notifications qui se produisent trop fréquemment pour être utiles.</span><span class="sxs-lookup"><span data-stu-id="7bc5d-114">The extensions are used to protect consumers from being flooded with notifications that occur too frequently to be useful.</span></span>

<span data-ttu-id="7bc5d-115">Les consommateurs qui ne nécessitent pas de notification chaque fois qu’un événement se produit peuvent spécifier les clauses suivantes dans leurs requêtes :</span><span class="sxs-lookup"><span data-stu-id="7bc5d-115">Consumers that do not require notification each time an event occurs can specify the following clauses in their queries:</span></span>

-   <span data-ttu-id="7bc5d-116">Clause [within](within-clause.md)</span><span class="sxs-lookup"><span data-stu-id="7bc5d-116">[WITHIN](within-clause.md) clause</span></span>
-   <span data-ttu-id="7bc5d-117">[Group](group-clause.md) , clause</span><span class="sxs-lookup"><span data-stu-id="7bc5d-117">[GROUP](group-clause.md) clause</span></span>
-   <span data-ttu-id="7bc5d-118">[Having](having-clause.md) (clause)</span><span class="sxs-lookup"><span data-stu-id="7bc5d-118">[HAVING](having-clause.md) clause</span></span>

<span data-ttu-id="7bc5d-119">Les clauses in et HAVING affectent le minutage des événements, et la clause GROUP provoque l’envoi d’un événement représentatif à la place d’un événement qui se produit fréquemment.</span><span class="sxs-lookup"><span data-stu-id="7bc5d-119">The WITHIN and HAVING clauses affect the timing of events, and the GROUP clause causes a representative event to be sent in place of a frequently occurring event.</span></span>

 

 



