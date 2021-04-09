---
description: La fonction SceSvcAttachmentUpdate est appelée par les composants logiciels enfichables de configuration de la sécurité pour transmettre les modifications de configuration à la base de données de sécurité.
ms.assetid: 2b5b3718-8ccb-480a-97fb-c8115d8f3a5c
title: SceSvcAttachmentUpdate fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentUpdate
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5bc4c9426f6a085c72f2fc3d872de4d7da59156b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750868"
---
# <a name="scesvcattachmentupdate-callback-function"></a><span data-ttu-id="06595-103">SceSvcAttachmentUpdate fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="06595-103">SceSvcAttachmentUpdate callback function</span></span>

<span data-ttu-id="06595-104">La fonction **SceSvcAttachmentUpdate** est appelée par les composants logiciels enfichables de configuration de la sécurité pour transmettre les modifications de configuration à la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="06595-104">The **SceSvcAttachmentUpdate** function is called by the Security Configuration snap-ins to pass configuration changes to the security database.</span></span>

## <a name="syntax"></a><span data-ttu-id="06595-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06595-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate(
  _In_ PSCESVC_CALLBACK_INFO     pSceCbInfo,
  _In_ SCESVC_CONFIGURATION_INFO *ServiceInfo
);
```



## <a name="parameters"></a><span data-ttu-id="06595-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06595-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06595-107">*pSceCbInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06595-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06595-108">Pointeur vers une structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) qui contient le handle de rappel et les pointeurs de fonction vers SCE.</span><span class="sxs-lookup"><span data-stu-id="06595-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure which contains the callback handle and function pointers to SCE.</span></span>

</dd> <dt>

<span data-ttu-id="06595-109">*ServiceInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06595-109">*ServiceInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06595-110">Informations de configuration mises à jour.</span><span class="sxs-lookup"><span data-stu-id="06595-110">Updated configuration information.</span></span> <span data-ttu-id="06595-111">La structure de données utilisée pour ces informations [**est \_ SCESVC \_ informations de configuration**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).</span><span class="sxs-lookup"><span data-stu-id="06595-111">The data structure used for this information is [**SCESVC\_CONFIGURATION\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06595-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06595-112">Return value</span></span>

<span data-ttu-id="06595-113">Si cette fonction réussit, elle retourne SCESTATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="06595-113">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="06595-114">Sinon, elle retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="06595-114">Otherwise it returns an error code.</span></span> <span data-ttu-id="06595-115">Pour plus d’informations sur les codes d’erreur de configuration de la sécurité, consultez [Attachment Return values](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="06595-115">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="06595-116">Notes</span><span class="sxs-lookup"><span data-stu-id="06595-116">Remarks</span></span>

<span data-ttu-id="06595-117">La fonction **SceSvcAttachmentUpdate** doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="06595-117">The **SceSvcAttachmentUpdate** function must do the following:</span></span>

-   <span data-ttu-id="06595-118">Appelez la fonction de rappel vers laquelle pointe le membre **pfQueryInfo** de la structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) pour récupérer les informations de configuration de base actuelles de la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="06595-118">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve the current base configuration information from the security database.</span></span>
-   <span data-ttu-id="06595-119">Appelez la fonction de rappel vers laquelle pointe le membre **pfQueryInfo** de la structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) pour récupérer le dernier jeu de différences (informations d’analyse) de la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="06595-119">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve the last set of differences (analysis information) from the security database.</span></span>
-   <span data-ttu-id="06595-120">Utilisez les informations de service fournies (voir *serviceInfo*) pour calculer la nouvelle configuration de base.</span><span class="sxs-lookup"><span data-stu-id="06595-120">Use the supplied service information (see *ServiceInfo*) to compute the new base configuration.</span></span>
-   <span data-ttu-id="06595-121">Utilisez les informations de service fournies (voir *serviceInfo*) et l’analyse pour calculer les nouvelles informations relatives aux différences.</span><span class="sxs-lookup"><span data-stu-id="06595-121">Use the supplied service information (see *ServiceInfo*) and the analysis to compute the new difference information.</span></span>
-   <span data-ttu-id="06595-122">Appelez la fonction de rappel vers laquelle pointe le membre **pfSetInfo** de la structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) pour définir la nouvelle configuration de base dans la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="06595-122">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo)to set the new base configuration in the security database.</span></span>
-   <span data-ttu-id="06595-123">Appelez la fonction de rappel vers laquelle pointe le membre **pfSetInfo** de la structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) pour définir les nouvelles informations d’analyse dans la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="06595-123">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo) to set the new analysis information in the security database.</span></span>

<span data-ttu-id="06595-124">Pour plus d’informations, consultez [implémentation de SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)</span><span class="sxs-lookup"><span data-stu-id="06595-124">For more information, see [Implementing SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="06595-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06595-125">Requirements</span></span>



| <span data-ttu-id="06595-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06595-126">Requirement</span></span> | <span data-ttu-id="06595-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="06595-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="06595-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06595-128">Minimum supported client</span></span><br/> | <span data-ttu-id="06595-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06595-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="06595-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06595-130">Minimum supported server</span></span><br/> | <span data-ttu-id="06595-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06595-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06595-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06595-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06595-133">**\_informations de rappel SCESVC \_**</span><span class="sxs-lookup"><span data-stu-id="06595-133">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="06595-134">**\_informations de configuration de SCESVC \_**</span><span class="sxs-lookup"><span data-stu-id="06595-134">**SCESVC\_CONFIGURATION\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info)
</dt> </dl>

 

 




