---
description: Les informations de l’utilisateur sont une mémoire tampon qui peut être transmise d’une terminaison d’une connexion à une autre. Ces informations sont spécifiques à la norme Q. 931 RNIS. Reportez-vous à la documentation de votre fournisseur de services sur la signification et l’utilisation de ces données.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Informations utilisateur-utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4539db192b9c24b5d71dfb60a2129e66b6658b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529704"
---
# <a name="user-user-information"></a><span data-ttu-id="f2ca6-105">Informations utilisateur-utilisateur</span><span class="sxs-lookup"><span data-stu-id="f2ca6-105">User-user information</span></span>

<span data-ttu-id="f2ca6-106">Les informations de l’utilisateur sont une mémoire tampon qui peut être transmise d’une terminaison d’une connexion à une autre.</span><span class="sxs-lookup"><span data-stu-id="f2ca6-106">User-user information is a buffer that can be transmitted from one end of a connection to another.</span></span> <span data-ttu-id="f2ca6-107">Ces informations sont spécifiques à la norme Q. 931 RNIS.</span><span class="sxs-lookup"><span data-stu-id="f2ca6-107">This information is specific to the ISDN Q.931 standard.</span></span> <span data-ttu-id="f2ca6-108">Reportez-vous à la documentation de votre fournisseur de services sur la signification et l’utilisation de ces données.</span><span class="sxs-lookup"><span data-stu-id="f2ca6-108">Please refer to your service provider's documentation on the meaning and use of this data.</span></span>

<span data-ttu-id="f2ca6-109">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.</span><span class="sxs-lookup"><span data-stu-id="f2ca6-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="f2ca6-110">\* \* TAPI 2. x : \* \*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** et **dwCallDataOffset** membres de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)</span><span class="sxs-lookup"><span data-stu-id="f2ca6-110">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** and **dwCallDataOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)</span></span>

<span data-ttu-id="f2ca6-111">\* \* TAPI 3. x : \* \*[**ITCallInfo :: GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), appelé avec le membre **CIM \_ USERUSERINFO** de [**la \_ mémoire tampon CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo :: ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)</span><span class="sxs-lookup"><span data-stu-id="f2ca6-111">\*\*TAPI 3.x:  \*\*[**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), called with the **CIB\_USERUSERINFO** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo::ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)</span></span>

 

 
