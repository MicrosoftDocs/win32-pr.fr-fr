---
description: Le type d’adresse identifie le format requis pour une adresse. Par exemple, si le type est LINEADDRESSTYPE \_ PHONENUMBER, l’adresse utilisée pour la connexion à la session doit être un numéro de téléphone.
ms.assetid: bea48bde-927a-400a-9a7e-a77e30ba35eb
title: Type d’adresse pour une session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42499c19a08d67ce2e6e7ea5741053686c32aa6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527500"
---
# <a name="address-type-for-a-session"></a><span data-ttu-id="b5d97-104">Type d’adresse pour une session</span><span class="sxs-lookup"><span data-stu-id="b5d97-104">Address Type for a Session</span></span>

<span data-ttu-id="b5d97-105">Le [**type d’adresse**](lineaddresstype--constants.md) identifie le format requis pour une adresse.</span><span class="sxs-lookup"><span data-stu-id="b5d97-105">The [**address type**](lineaddresstype--constants.md) identifies the format required for an address.</span></span> <span data-ttu-id="b5d97-106">Par exemple, si le type est LINEADDRESSTYPE \_ PHONENUMBER, l’adresse utilisée pour la connexion à la session doit être un numéro de téléphone.</span><span class="sxs-lookup"><span data-stu-id="b5d97-106">For example, if the type is LINEADDRESSTYPE\_PHONENUMBER, the address used to dial on the session must be a phone number.</span></span>

<span data-ttu-id="b5d97-107">Un appareil et un fournisseur de services donnés prennent en charge un ou plusieurs types d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b5d97-107">A given device and service provider supports one or more address types.</span></span> <span data-ttu-id="b5d97-108">Pour plus d’informations sur la façon d’interroger un appareil en fonction des formats d’adresse pris en charge, consultez les [types d’adresses d’un appareil](address-type-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="b5d97-108">See the [address types for a device](address-type-ovr.md) for information on how to poll a device for the address formats it supports.</span></span>

<span data-ttu-id="b5d97-109">**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwAddressType** , membre de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span><span class="sxs-lookup"><span data-stu-id="b5d97-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwAddressType** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span></span>

<span data-ttu-id="b5d97-110">**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), appelé avec le **\_ CALLERIDADDRESSTYPE CIL**, **le CIL \_ CALLEDIDADDRESSTYPE** ou le membre **CIL \_ CONNECTEDIDADDRESSTYPE** de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="b5d97-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with the **CIL\_CALLERIDADDRESSTYPE**, **CIL\_CALLEDIDADDRESSTYPE**, or **CIL\_CONNECTEDIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

 

 
