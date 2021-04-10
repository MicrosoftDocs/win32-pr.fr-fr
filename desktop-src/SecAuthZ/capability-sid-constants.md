---
description: Définissez pour les fonctionnalités connues des applications à l’aide de la fonction AllocateAndInitializeSid.
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: Constantes SID de capacité (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55809cbb341bcbe60578043778bc824e09b8a295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211077"
---
# <a name="capability-sid-constants"></a><span data-ttu-id="fc343-103">Constantes SID de capacité</span><span class="sxs-lookup"><span data-stu-id="fc343-103">Capability SID Constants</span></span>

<span data-ttu-id="fc343-104">Les constantes de SID de fonctionnalité définissent pour les fonctionnalités bien connues des applications à l’aide de la fonction [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .</span><span class="sxs-lookup"><span data-stu-id="fc343-104">The capability SID constants define for applications well-known capabilities by using the [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) function.</span></span>

<dl> <dt>

<span data-ttu-id="fc343-105"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**\_ \_ client Internet des fonctionnalités de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="fc343-105"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**SECURITY\_CAPABILITY\_INTERNET\_CLIENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc343-106">(0x00000001L)</span><span class="sxs-lookup"><span data-stu-id="fc343-106">(0x00000001L)</span></span>
</dt> <dt>



<span data-ttu-id="fc343-107">Un compte a accès à Internet à partir d’un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="fc343-107">An account has access to the Internet from a client computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc343-108"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**\_ \_ \_ serveur client Internet de capacité de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="fc343-108"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**SECURITY\_CAPABILITY\_INTERNET\_CLIENT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc343-109">(0x00000002L)</span><span class="sxs-lookup"><span data-stu-id="fc343-109">(0x00000002L)</span></span>
</dt> <dt>



<span data-ttu-id="fc343-110">Un compte a accès à Internet à partir des ordinateurs client et serveur.</span><span class="sxs-lookup"><span data-stu-id="fc343-110">An account has access to the Internet from the client and server computers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc343-111"><span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**\_ \_ \_ serveur client de réseau \_ privé \_ de fonctionnalités de sécurité**</span><span class="sxs-lookup"><span data-stu-id="fc343-111"><span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**SECURITY\_CAPABILITY\_PRIVATE\_NETWORK\_CLIENT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc343-112">(0x00000003L)</span><span class="sxs-lookup"><span data-stu-id="fc343-112">(0x00000003L)</span></span>
</dt> <dt>



<span data-ttu-id="fc343-113">Un compte a accès à Internet à partir d’un réseau privé.</span><span class="sxs-lookup"><span data-stu-id="fc343-113">An account has access to the Internet from a private network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc343-114"><span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**\_bibliothèque d' \_ images des fonctionnalités de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="fc343-114"><span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**SECURITY\_CAPABILITY\_PICTURES\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc343-115">(0x00000004L)</span><span class="sxs-lookup"><span data-stu-id="fc343-115">(0x00000004L)</span></span>
</dt> <dt>



<span data-ttu-id="fc343-116">Un compte a accès à la bibliothèque d’images.</span><span class="sxs-lookup"><span data-stu-id="fc343-116">An account has access to the pictures library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc343-117"><span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**bibliothèque de vidéos sur les fonctionnalités de sécurité \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fc343-117"><span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**SECURITY\_CAPABILITY\_VIDEOS\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc343-118">(0x00000005L)</span><span class="sxs-lookup"><span data-stu-id="fc343-118">(0x00000005L)</span></span>
</dt> <dt>



<span data-ttu-id="fc343-119">Un compte a accès à la bibliothèque vidéos.</span><span class="sxs-lookup"><span data-stu-id="fc343-119">An account has access to the videos library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc343-120"><span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**Médiathèque sur les fonctionnalités de sécurité \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fc343-120"><span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**SECURITY\_CAPABILITY\_MUSIC\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc343-121">(0x00000006L)</span><span class="sxs-lookup"><span data-stu-id="fc343-121">(0x00000006L)</span></span>
</dt> <dt>



<span data-ttu-id="fc343-122">Un compte a accès à la bibliothèque musique.</span><span class="sxs-lookup"><span data-stu-id="fc343-122">An account has access to the music library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc343-123"><span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**bibliothèque de documents sur les capacités de sécurité \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fc343-123"><span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**SECURITY\_CAPABILITY\_DOCUMENTS\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc343-124">(0x00000007L)</span><span class="sxs-lookup"><span data-stu-id="fc343-124">(0x00000007L)</span></span>
</dt> <dt>



<span data-ttu-id="fc343-125">Un compte a accès à la bibliothèque de documentation.</span><span class="sxs-lookup"><span data-stu-id="fc343-125">An account has access to the documentation library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc343-126"><span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**\_authentification de \_ l’entreprise des fonctionnalités de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="fc343-126"><span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**SECURITY\_CAPABILITY\_ENTERPRISE\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc343-127">(0x00000008L)</span><span class="sxs-lookup"><span data-stu-id="fc343-127">(0x00000008L)</span></span>
</dt> <dt>



<span data-ttu-id="fc343-128">Un compte a accès aux informations d’identification Windows par défaut.</span><span class="sxs-lookup"><span data-stu-id="fc343-128">An account has access to the default Windows credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc343-129"><span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**\_certificats d' \_ \_ utilisateur partagé de capacité \_ de sécurité**</span><span class="sxs-lookup"><span data-stu-id="fc343-129"><span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**SECURITY\_CAPABILITY\_SHARED\_USER\_CERTIFICATES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc343-130">(0x00000009L)</span><span class="sxs-lookup"><span data-stu-id="fc343-130">(0x00000009L)</span></span>
</dt> <dt>



<span data-ttu-id="fc343-131">Un compte a accès aux certificats utilisateur partagés.</span><span class="sxs-lookup"><span data-stu-id="fc343-131">An account has access to the shared user certificates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc343-132"><span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**\_ \_ stockage amovible des fonctionnalités de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="fc343-132"><span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**SECURITY\_CAPABILITY\_REMOVABLE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc343-133">(0x0000000AL)</span><span class="sxs-lookup"><span data-stu-id="fc343-133">(0x0000000AL)</span></span>
</dt> <dt>



<span data-ttu-id="fc343-134">Un compte a accès au stockage amovible.</span><span class="sxs-lookup"><span data-stu-id="fc343-134">An account has access to removable storage.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc343-135">Notes</span><span class="sxs-lookup"><span data-stu-id="fc343-135">Remarks</span></span>

<span data-ttu-id="fc343-136">Lors de la construction d’un SID de fonctionnalité, vous devez inclure l’autorité de package, l' \_ \_ \_ autorité {0,0,0,0,0,15} de package d’application de sécurité, dans l’appel à la fonction [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .</span><span class="sxs-lookup"><span data-stu-id="fc343-136">When constructing a capability SID, you need to include the package authority, SECURITY\_APP\_PACKAGE\_AUTHORITY {0,0,0,0,0,15}, in the call to the [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) function.</span></span> <span data-ttu-id="fc343-137">En outre, vous avez besoin du RID de base et du nombre RID pour les fonctionnalités intégrées, le RID de base des fonctionnalités de sécurité \_ \_ \_ (0x00000003L) et le \_ nombre RID de capacités builtin de sécurité \_ \_ \_ (2L).</span><span class="sxs-lookup"><span data-stu-id="fc343-137">Additionally, you need the base RID and RID count for the built-in capabilities, SECURITY\_CAPABILITY\_BASE\_RID (0x00000003L) and SECURITY\_BUILTIN\_CAPABILITY\_RID\_COUNT (2L).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc343-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc343-138">Requirements</span></span>



| <span data-ttu-id="fc343-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc343-139">Requirement</span></span> | <span data-ttu-id="fc343-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc343-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc343-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc343-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fc343-142">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc343-142">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fc343-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc343-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fc343-144">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc343-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fc343-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc343-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc343-146"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc343-146"><dt>Winnt.h</dt></span></span> </dl> |



 

