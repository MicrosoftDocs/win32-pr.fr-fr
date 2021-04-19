---
description: La mémoire tampon de compatibilité est spécifique à la norme Q. 931 RNIS. Reportez-vous à la documentation de votre fournisseur de services sur la signification et l’utilisation de ces données.
ms.assetid: c4c87ca8-fbae-4275-9b69-7b32daf4c18f
title: Mémoire tampon de compatibilité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8669e32cd47978c10e2f5abdbe076bcf08ba1862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527756"
---
# <a name="compatibility-buffer"></a><span data-ttu-id="6e6f1-104">Mémoire tampon de compatibilité</span><span class="sxs-lookup"><span data-stu-id="6e6f1-104">Compatibility Buffer</span></span>

<span data-ttu-id="6e6f1-105">La mémoire tampon de compatibilité est spécifique à la norme Q. 931 RNIS.</span><span class="sxs-lookup"><span data-stu-id="6e6f1-105">The compatibility buffer is specific to the ISDN Q.931 standard.</span></span> <span data-ttu-id="6e6f1-106">Reportez-vous à la documentation de votre fournisseur de services sur la signification et l’utilisation de ces données.</span><span class="sxs-lookup"><span data-stu-id="6e6f1-106">Please refer to your service provider's documentation on the meaning and use of this data.</span></span>

<span data-ttu-id="6e6f1-107">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.</span><span class="sxs-lookup"><span data-stu-id="6e6f1-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="6e6f1-108">**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwHighLevelCompSize**, **dwHighLevelCompOffset**, **dwLowLevelCompSize** et **dwLowLevelCompOffset** les membres de *lpCallInfo*).</span><span class="sxs-lookup"><span data-stu-id="6e6f1-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwHighLevelCompSize**, **dwHighLevelCompOffset**, **dwLowLevelCompSize**, and **dwLowLevelCompOffset** members of *lpCallInfo*).</span></span>

<span data-ttu-id="6e6f1-109">**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIM \_ HIGHLEVELCOMPATIBILITYBUFFER** et **CIM \_ LOWLEVELCOMPATIBILITYBUFFER** membre de [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span><span class="sxs-lookup"><span data-stu-id="6e6f1-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB\_HIGHLEVELCOMPATIBILITYBUFFER** and **CIB\_LOWLEVELCOMPATIBILITYBUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).</span></span>

 

 
