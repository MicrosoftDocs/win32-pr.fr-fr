---
description: L’application doit inventorier les ressources de communication disponibles, puis notifier à l’interface TAPI les ressources qu’elle utilisera et son mode d’utilisation.
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: Inventaire des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e743934f225fa4f932460eba0bbf895cc1bc21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543499"
---
# <a name="resource-inventory"></a><span data-ttu-id="ea33d-103">Inventaire des ressources</span><span class="sxs-lookup"><span data-stu-id="ea33d-103">Resource Inventory</span></span>

<span data-ttu-id="ea33d-104">L’application doit inventorier les ressources de communication disponibles, puis notifier à l’interface TAPI les ressources qu’elle utilisera et son mode d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="ea33d-104">The application must inventory the communications resources available to it, then notify TAPI about which resources it will use and how it will use them.</span></span> <span data-ttu-id="ea33d-105">Pour plus d’informations sur les types de ressources et capacités auxquelles une application peut accéder, consultez contrôle de l' [appareil](device-control.md) .</span><span class="sxs-lookup"><span data-stu-id="ea33d-105">See [Device Control](device-control.md) for additional information on the types of resources and capabilities an application might access.</span></span>

<span data-ttu-id="ea33d-106">**TAPI 2. x :** Les applications obtiennent le nombre de lignes disponibles lorsque [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) retourne.</span><span class="sxs-lookup"><span data-stu-id="ea33d-106">**TAPI 2.x:** Applications get the number of available lines when [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) returns.</span></span> <span data-ttu-id="ea33d-107">Ils peuvent ensuite effectuer des [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) sur chaque ligne, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) pour chaque adresse et [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) pour chaque ligne qui sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea33d-107">They can then perform [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) on each line, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) for each address, and [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) for each line that will be used.</span></span>

<span data-ttu-id="ea33d-108">**TAPI 3. x :** Les applications utilisent [**ITTAPI :: EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) ou [**ITTAPI :: obtenir des \_ adresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) pour découvrir les adresses disponibles.</span><span class="sxs-lookup"><span data-stu-id="ea33d-108">**TAPI 3.x:** Applications use [**ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) or [**ITTAPI::get\_Addresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) to discover the addresses available.</span></span> <span data-ttu-id="ea33d-109">[**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) et [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) fournissent des informations sur les types de communication possibles pour chaque adresse.</span><span class="sxs-lookup"><span data-stu-id="ea33d-109">[**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) and [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) supply information on communication types possible for each address.</span></span> <span data-ttu-id="ea33d-110">Si elle est implémentée par le fournisseur de services, [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) permet à une application d’accéder à des informations et des contrôles supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ea33d-110">If implemented by the service provider, [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) gives an application access to additional information and controls.</span></span>

 

 
