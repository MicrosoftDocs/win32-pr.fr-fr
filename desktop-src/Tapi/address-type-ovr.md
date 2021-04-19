---
description: Le type d’adresse de l’appareil décrit les formes d’adressage autorisées sur une adresse, par exemple un numéro de téléphone ou une adresse IP.
ms.assetid: b474dfca-c4a6-4aab-a4dd-5aec7be3e02a
title: Type d'adresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9438c200c9b09dd4f78342ea18d412eaaf23b646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521051"
---
# <a name="address-type"></a><span data-ttu-id="f5c5f-103">Type d'adresse</span><span class="sxs-lookup"><span data-stu-id="f5c5f-103">Address Type</span></span>

<span data-ttu-id="f5c5f-104">Le type d’adresse de l’appareil décrit les formes d’adressage autorisées sur une adresse, par exemple un numéro de téléphone ou une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="f5c5f-104">The device address type describes the forms of addressing permissible on an address, such as a phone number or an IP address.</span></span> <span data-ttu-id="f5c5f-105">Un appareil donné va comprendre un ou plusieurs types d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f5c5f-105">A given device will understand one or more address types.</span></span> <span data-ttu-id="f5c5f-106">Pour obtenir la liste des types d’adresses pris en charge par TAPI, consultez [ \_ constantes LINEADDRESSTYPE](lineaddresstype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="f5c5f-106">For a list of address types supported by TAPI, see [LINEADDRESSTYPE\_ Constants](lineaddresstype--constants.md).</span></span> <span data-ttu-id="f5c5f-107">La [traduction d’adresses](initiate-a-session-ovr.md) peut être utilisée pour convertir une adresse d’un type en un autre.</span><span class="sxs-lookup"><span data-stu-id="f5c5f-107">[Address translation](initiate-a-session-ovr.md) may be used to convert an address from one type to another.</span></span>

<span data-ttu-id="f5c5f-108">Pour obtenir des informations générales sur les adresses, consultez [adresse](address-ovr.md) sous [catégories d’appareils](device-categories.md).</span><span class="sxs-lookup"><span data-stu-id="f5c5f-108">For general information on addresses, see [Address](address-ovr.md) under [Device Categories](device-categories.md).</span></span>

<span data-ttu-id="f5c5f-109">Le [type d’adresse d’une session](address-type-for-a-session-ovr.md) est un sous-ensemble des types d’adresse d’appareil.</span><span class="sxs-lookup"><span data-stu-id="f5c5f-109">The [address type for a session](address-type-for-a-session-ovr.md) will be a subset of the device address types.</span></span>

<span data-ttu-id="f5c5f-110">**TAPI 2. x :** Consultez [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) et le membre **dwAddressType** de [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps).</span><span class="sxs-lookup"><span data-stu-id="f5c5f-110">**TAPI 2.x:** See [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) and the **dwAddressType** member of [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps).</span></span>

<span data-ttu-id="f5c5f-111">**TAPI 3. x :** Consultez [**ITAddressCapabilities :: obtenir \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability), avec *AddressCap* défini sur la [**\_ fonctionnalité d’adresse**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)de **\_ ADDRESSTYPES AC** .</span><span class="sxs-lookup"><span data-stu-id="f5c5f-111">**TAPI 3.x:** See [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability), with *AddressCap* set to the **AC\_ADDRESSTYPES** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).</span></span>

 

 
