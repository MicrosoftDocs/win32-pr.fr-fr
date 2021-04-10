---
description: Le code du pays ou de la région est pertinent uniquement lorsque le type d’adresse est LINEADDRESSTYPE \_ PHONENUMBER. Il identifie une zone du monde.
ms.assetid: d838c2ac-4ee3-4314-8573-deed6c7430e3
title: Code du pays ou de la région
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5557e4d67b701fda2aa05ad81686ae474b172063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863102"
---
# <a name="country-or-region-code"></a><span data-ttu-id="21a96-104">Code du pays ou de la région</span><span class="sxs-lookup"><span data-stu-id="21a96-104">Country or Region Code</span></span>

<span data-ttu-id="21a96-105">Le code du pays ou de la région est pertinent uniquement lorsque le type d’adresse est LINEADDRESSTYPE \_ PHONENUMBER.</span><span class="sxs-lookup"><span data-stu-id="21a96-105">The country or region code is relevant only when the address type is LINEADDRESSTYPE\_PHONENUMBER.</span></span> <span data-ttu-id="21a96-106">Il identifie une zone du monde.</span><span class="sxs-lookup"><span data-stu-id="21a96-106">It identifies an area of the world.</span></span>

<span data-ttu-id="21a96-107">Tous les fournisseurs de services qui prennent en charge l’utilisation de numéros de téléphone doivent prendre en charge l’utilisation de ces informations.</span><span class="sxs-lookup"><span data-stu-id="21a96-107">All service providers that support use of telephone numbers must support use of this information.</span></span>

<span data-ttu-id="21a96-108">**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membre **dwCountryCode** de *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="21a96-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCountryCode** member of *lpCallInfo*).</span></span>

<span data-ttu-id="21a96-109">**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CountryCode** Member of [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="21a96-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_COUNTRYCODE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
