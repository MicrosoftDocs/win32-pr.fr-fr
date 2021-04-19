---
description: Le \_ type de données DRV REQUESTID est utilisé pour fournir un identificateur unique pour une demande au fournisseur de services.
ms.assetid: cef6a42a-2e40-4f65-8fab-79cfba143206
title: DRV_REQUESTID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9c0db093b06b263bcdc702ff14af7e308033f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529825"
---
# <a name="drv_requestid"></a><span data-ttu-id="f44ba-103">DRV \_ REQUESTID</span><span class="sxs-lookup"><span data-stu-id="f44ba-103">DRV\_REQUESTID</span></span>

<span data-ttu-id="f44ba-104">Le type de données **DRV \_ REQUESTID** est utilisé pour fournir un identificateur unique pour une demande au fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="f44ba-104">The **DRV\_REQUESTID** datatype is used to supply a unique identifier for a request to the service provider.</span></span> <span data-ttu-id="f44ba-105">Une valeur de ce type est passée en tant que paramètre à chaque fonction qui autorise l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f44ba-105">A value of this type is passed as a parameter to every function that allows for asynchronous operation.</span></span> <span data-ttu-id="f44ba-106">Si l’opération est asynchrone, le fournisseur de services retourne cette valeur comme valeur de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="f44ba-106">If the operation is asynchronous, the service provider returns this value as the return value of the function.</span></span> <span data-ttu-id="f44ba-107">Chaque fois que le fournisseur de services marque une requête comme asynchrone de cette manière, il doit finalement signaler que l’opération est terminée en appelant la fonction de rappel de la [*\_ procédure d’achèvement*](/windows/win32/api/tspi/nc-tspi-async_completion) .</span><span class="sxs-lookup"><span data-stu-id="f44ba-107">Whenever the service provider flags a request as asynchronous in this way, it must eventually report the operation is complete by calling the [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) callback function.</span></span>

<span data-ttu-id="f44ba-108">L’interface TAPI garantit que les valeurs du **DRV \_ REQUESTID** fournies sont strictement positives, c’est-à-dire entre les valeurs 0x00000001 et 0x7FFFFFFF incluses.</span><span class="sxs-lookup"><span data-stu-id="f44ba-108">TAPI ensures that the **DRV\_REQUESTID** values it supplies are strictly positive, that is, between the values of 0x00000001 and 0x7FFFFFFF, inclusive.</span></span> <span data-ttu-id="f44ba-109">En outre, les valeurs sont uniques dans la mesure où aucune valeur retournée par une fonction pour marquer la requête comme asynchrone est réutilisée avant que l’opération ne soit signalée comme terminée.</span><span class="sxs-lookup"><span data-stu-id="f44ba-109">Furthermore, the values are unique in that no value returned from a function to flag the request as asynchronous will be re-used before the operation is reported complete.</span></span>

 

 
