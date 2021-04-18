---
description: Après l’attribution d’adresses, l’interface TAPI assigne des identificateurs d’adresse aux adresses.
ms.assetid: 19394db1-4408-4ba6-be48-b408c1fa0f30
title: Identificateurs d’adresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80ee463271a4d7fe9e4dcec086b08c37326551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512946"
---
# <a name="address-identifiers"></a><span data-ttu-id="eb3be-103">Identificateurs d’adresse</span><span class="sxs-lookup"><span data-stu-id="eb3be-103">Address Identifiers</span></span>

<span data-ttu-id="eb3be-104">Après l’attribution d’adresses, l’interface TAPI assigne des identificateurs d’adresse aux adresses.</span><span class="sxs-lookup"><span data-stu-id="eb3be-104">After address assignment, TAPI assigns address identifiers to the addresses.</span></span> <span data-ttu-id="eb3be-105">Un *identificateur d’adresse* est un nombre compris entre 0 et le nombre d’adresses sur la ligne moins un.</span><span class="sxs-lookup"><span data-stu-id="eb3be-105">An *address identifier* is a number between 0 and the number of addresses on the line minus one.</span></span> <span data-ttu-id="eb3be-106">Un identificateur d’adresse est un nombre permanent attribué à un appareil donné et reste constant même entre les mises à niveau du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="eb3be-106">An address identifier is a permanent number assigned to a given device and remains constant even across operating system upgrades.</span></span> <span data-ttu-id="eb3be-107">La combinaison de l' [identificateur d’appareil](device-identifier-ovr.md) et de l’identificateur d’adresse identifie de façon unique une adresse donnée.</span><span class="sxs-lookup"><span data-stu-id="eb3be-107">The combination of [device identifier](device-identifier-ovr.md) and address identifier uniquely identifies a given address.</span></span>

<span data-ttu-id="eb3be-108">**TAPI 2. x :** Les applications obtiennent un identificateur d’adresse (et un identificateur de périphérique) lors d’un appel à [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) ou [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), dans la structure [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) ou dans un appel à [**lineGetAddressID**](/windows/win32/api/tapi/nf-tapi-linegetaddressid).</span><span class="sxs-lookup"><span data-stu-id="eb3be-108">**TAPI 2.x:** Applications obtain an address identifier (and device identifier) during a call to [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) or [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), in the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure, or in a call to [**lineGetAddressID**](/windows/win32/api/tapi/nf-tapi-linegetaddressid).</span></span>

<span data-ttu-id="eb3be-109">**TAPI 3. x :** Le [**ITAddressCapabilities :: obtenir \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) appelé *AddressCap* défini sur la [**\_ fonctionnalité d’adresse**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) de **\_ ADDRESSID AC** est retourné avec le paramètre *plCapability* défini sur l’ID d’adresse actuel.</span><span class="sxs-lookup"><span data-stu-id="eb3be-109">**TAPI 3.x:** The [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) called *AddressCap* set to the **AC\_ADDRESSID** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) will return with the *plCapability* parameter set to the current address ID.</span></span>

 

 
