---
title: Interrogation des variables d’État
description: L’interface IUPnPService fournit la méthode QueryStateVariable, qui retourne la valeur d’une variable d’état spécifiée.
ms.assetid: 9e8b98b0-488a-4f9c-9ad7-039dbd470486
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a716bbe93c2306eca43b977a42f33a85187f92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309837"
---
# <a name="querying-state-variables"></a><span data-ttu-id="6263e-103">Interrogation des variables d’État</span><span class="sxs-lookup"><span data-stu-id="6263e-103">Querying State Variables</span></span>

<span data-ttu-id="6263e-104">L’interface [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) fournit la méthode [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) , qui retourne la valeur d’une variable d’état spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6263e-104">The [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface provides the [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) method, that returns the value of a specified state variable.</span></span>

<span data-ttu-id="6263e-105">Le Forum UPnP déconseille l’utilisation de [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable).</span><span class="sxs-lookup"><span data-stu-id="6263e-105">The UPnP Forum discourages the use of [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable).</span></span> <span data-ttu-id="6263e-106">Les créateurs d’appareils ont été encouragés à écrire des actions appropriées pour fournir ces informations.</span><span class="sxs-lookup"><span data-stu-id="6263e-106">Device writers have been encouraged to write appropriate actions to provide this information.</span></span> <span data-ttu-id="6263e-107">Les créateurs d’appareils ne sont pas tenus d’implémenter **QueryStateVariable**.</span><span class="sxs-lookup"><span data-stu-id="6263e-107">Device writers are under no obligation to implement **QueryStateVariable**.</span></span>

<span data-ttu-id="6263e-108">Consultez la section [appel d’actions](invoking-actions.md).</span><span class="sxs-lookup"><span data-stu-id="6263e-108">See the section [Invoking Actions](invoking-actions.md).</span></span>

 

 




