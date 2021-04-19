---
description: L’interface IUpdateSearcher définit les méthodes suivantes.
ms.assetid: 82735555-b23a-43b0-bf5b-a8cf72dc40d4
title: Méthodes IUpdateSearcher
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 462cbd371546743bab836ed1cdc2479e30f13612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514638"
---
# <a name="iupdatesearcher-methods"></a><span data-ttu-id="8f4b2-103">Méthodes IUpdateSearcher</span><span class="sxs-lookup"><span data-stu-id="8f4b2-103">IUpdateSearcher Methods</span></span>

<span data-ttu-id="8f4b2-104">L’interface [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) définit les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="8f4b2-104">The [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) interface defines the following methods.</span></span>



| <span data-ttu-id="8f4b2-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="8f4b2-105">Method</span></span>                                                              | <span data-ttu-id="8f4b2-106">Description</span><span class="sxs-lookup"><span data-stu-id="8f4b2-106">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f4b2-107">**BeginSearch**</span><span class="sxs-lookup"><span data-stu-id="8f4b2-107">**BeginSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)                   | <span data-ttu-id="8f4b2-108">Commence l’exécution d’une recherche asynchrone des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="8f4b2-108">Begins execution of an asynchronous search for updates.</span></span> <span data-ttu-id="8f4b2-109">La recherche utilise les options de recherche qui sont actuellement configurées.</span><span class="sxs-lookup"><span data-stu-id="8f4b2-109">The search uses the search options that are currently configured.</span></span> |
| [<span data-ttu-id="8f4b2-110">**EndSearch**</span><span class="sxs-lookup"><span data-stu-id="8f4b2-110">**EndSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)                       | <span data-ttu-id="8f4b2-111">Termine une recherche asynchrone des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="8f4b2-111">Completes an asynchronous search for updates.</span></span>                                                                             |
| [<span data-ttu-id="8f4b2-112">**EscapeString**</span><span class="sxs-lookup"><span data-stu-id="8f4b2-112">**EscapeString**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-escapestring)                 | <span data-ttu-id="8f4b2-113">Convertit une chaîne en une chaîne qui peut être utilisée comme valeur littérale dans une chaîne de critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="8f4b2-113">Converts a string into a string that can be used as a literal value in a search criteria string.</span></span>                          |
| [<span data-ttu-id="8f4b2-114">**GetTotalHistoryCount**</span><span class="sxs-lookup"><span data-stu-id="8f4b2-114">**GetTotalHistoryCount**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-gettotalhistorycount) | <span data-ttu-id="8f4b2-115">Retourne le nombre d’événements de mise à jour sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8f4b2-115">Returns the number of update events on the computer.</span></span>                                                                      |
| [<span data-ttu-id="8f4b2-116">**QueryHistory**</span><span class="sxs-lookup"><span data-stu-id="8f4b2-116">**QueryHistory**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-queryhistory)                | <span data-ttu-id="8f4b2-117">Interroge de manière synchrone l’ordinateur sur l’historique des événements de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="8f4b2-117">Synchronously queries the computer for the history of update events.</span></span>                                                      |
| [<span data-ttu-id="8f4b2-118">**Recherche**</span><span class="sxs-lookup"><span data-stu-id="8f4b2-118">**Search**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search)                             | <span data-ttu-id="8f4b2-119">Effectue une recherche synchrone des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="8f4b2-119">Performs a synchronous search for updates.</span></span> <span data-ttu-id="8f4b2-120">La recherche utilise les options de recherche qui sont actuellement configurées.</span><span class="sxs-lookup"><span data-stu-id="8f4b2-120">The search uses the search options that are currently configured.</span></span>              |



 

 

 



