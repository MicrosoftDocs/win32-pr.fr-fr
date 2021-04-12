---
description: Les sections suivantes contiennent une liste alphabétique des fonctions regroupées par zone. Les informations de chaque fonction incluent une liste des États d’appel valides à l’entrée de la fonction et des transitions d’état d’appel standard lorsque la demande est terminée.
ms.assetid: 555d6af2-b440-4636-b90e-da297a369753
title: Fonctions TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38532fa1c0b978e3e59e54b08fbc43152fa0bd64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529212"
---
# <a name="tapi-functions"></a><span data-ttu-id="d4bd6-104">Fonctions TAPI</span><span class="sxs-lookup"><span data-stu-id="d4bd6-104">TAPI Functions</span></span>

<span data-ttu-id="d4bd6-105">Les sections suivantes contiennent une liste alphabétique des fonctions regroupées par zone.</span><span class="sxs-lookup"><span data-stu-id="d4bd6-105">The following sections contain an alphabetic list of functions grouped by area.</span></span> <span data-ttu-id="d4bd6-106">Les informations de chaque fonction incluent une liste des États d’appel valides à l’entrée de la fonction et des transitions d’état d’appel standard lorsque la demande est terminée.</span><span class="sxs-lookup"><span data-stu-id="d4bd6-106">The information for each function includes a list of the valid call states on entry of the function and typical call state transitions when the request is complete.</span></span>

-   [<span data-ttu-id="d4bd6-107">Fonctions de téléphonie assistée</span><span class="sxs-lookup"><span data-stu-id="d4bd6-107">Assisted Telephony Functions</span></span>](assisted-telephony-functions.md)
-   [<span data-ttu-id="d4bd6-108">Fonctions du centre d’appels</span><span class="sxs-lookup"><span data-stu-id="d4bd6-108">Call Center Functions</span></span>](call-center-functions.md)
-   [<span data-ttu-id="d4bd6-109">Fonctions du périphérique de ligne</span><span class="sxs-lookup"><span data-stu-id="d4bd6-109">Line Device Functions</span></span>](line-device-functions.md)
-   [<span data-ttu-id="d4bd6-110">Fonctions des appareils téléphoniques</span><span class="sxs-lookup"><span data-stu-id="d4bd6-110">Phone Device Functions</span></span>](phone-device-functions.md)

<span data-ttu-id="d4bd6-111">Pour les fonctions TAPI catégorisées par niveau de service et tâche, consultez [référence des fonctions rapides TAPI](tapi-quick-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d4bd6-111">For TAPI functions categorized by service level and task, see [TAPI Quick Function Reference](tapi-quick-function-reference.md).</span></span>

<span data-ttu-id="d4bd6-112">Notez que les limitations du fournisseur de services peuvent exister en ce qui concerne les États réels dans lesquels une fonction peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="d4bd6-112">Please note that service provider limitations may exist concerning the actual states in which a function can be performed.</span></span> <span data-ttu-id="d4bd6-113">Les applications doivent vérifier le membre **dwCallFeatures** dans la structure [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , le membre **dwAddressFeatures** dans la structure [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) et le membre **dwLineFeatures** dans la structure [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) pour déterminer si une fonction est autorisée ou non dans l’état d’appel actuel.</span><span class="sxs-lookup"><span data-stu-id="d4bd6-113">Applications must check the **dwCallFeatures** member in the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure, the **dwAddressFeatures** member in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure, and the **dwLineFeatures** member in the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) structure to determine whether or not a function is permitted within the current call state.</span></span>

 

 



