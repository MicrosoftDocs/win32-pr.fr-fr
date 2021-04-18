---
description: L’interface TAPI fournit un certain nombre de fonctions pour manipuler les handles d’appel, en déterminant la relation entre les lignes, les appels et l’adresse, et ainsi de suite.
ms.assetid: 283fe5e9-689f-4b87-97a6-b345c22ec6a2
title: Appeler une manipulation de handle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 248f16088f891b1441626097de5c803a8fe14991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519027"
---
# <a name="call-handle-manipulation"></a><span data-ttu-id="2dbdf-103">Appeler une manipulation de handle</span><span class="sxs-lookup"><span data-stu-id="2dbdf-103">Call Handle Manipulation</span></span>

<span data-ttu-id="2dbdf-104">L’interface TAPI fournit un certain nombre de fonctions pour manipuler les handles d’appel, en déterminant la relation entre les lignes, les appels et l’adresse, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="2dbdf-104">TAPI provides a number of functions for manipulating call handles, determining the relationship among lines, calls, and address, and so on.</span></span> <span data-ttu-id="2dbdf-105">La plupart de ces fonctionnalités sont implémentées strictement dans TAPI sans référence au fournisseur de services, à l’exception de [**TSPI \_ lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid).</span><span class="sxs-lookup"><span data-stu-id="2dbdf-105">Most of this functionality is implemented strictly within TAPI without reference to the service provider, except for [**TSPI\_lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid).</span></span> <span data-ttu-id="2dbdf-106">Cette fonction récupère l’identificateur d’adresse d’un appel existant au sein de sa ligne.</span><span class="sxs-lookup"><span data-stu-id="2dbdf-106">This function retrieves the address identifier of an existing call within its line.</span></span> <span data-ttu-id="2dbdf-107">Les fournisseurs de services qui modélisent une ligne en tant que groupe d’identificateurs d’adresses peuvent choisir une adresse imprévisible pour un nouvel appel entrant ou sortant.</span><span class="sxs-lookup"><span data-stu-id="2dbdf-107">Service providers that model a line as a group of address identifiers can choose an unpredictable address for a new inbound or outbound call.</span></span> <span data-ttu-id="2dbdf-108">Cette fonction fournit à TAPI des informations suffisantes pour implémenter l’opération [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) lorsqu’elle est appelée avec l' \_ option d’adresse LINECALLSELECT.</span><span class="sxs-lookup"><span data-stu-id="2dbdf-108">This function gives TAPI sufficient information to implement the [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) operation when it is invoked with the LINECALLSELECT\_ADDRESS option.</span></span>

 

 
