---
description: La fonction SceSvcAttachmentAnalyze est appelée par le moteur de configuration de sécurité lors de l’analyse du système.
ms.assetid: 8e8a39b9-c4e2-446e-8e0c-eb2113234c1a
title: SceSvcAttachmentAnalyze fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentAnalyze
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 296d755a0b082b46122432936d30614019b8b9a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750876"
---
# <a name="scesvcattachmentanalyze-callback-function"></a><span data-ttu-id="f4c22-103">SceSvcAttachmentAnalyze fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="f4c22-103">SceSvcAttachmentAnalyze callback function</span></span>

<span data-ttu-id="f4c22-104">La fonction **SceSvcAttachmentAnalyze** est appelée par le moteur de configuration de sécurité lors de l’analyse du système.</span><span class="sxs-lookup"><span data-stu-id="f4c22-104">The **SceSvcAttachmentAnalyze** function is called by the Security Configuration Engine when the system is analyzed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4c22-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4c22-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f4c22-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4c22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4c22-107">*pSceCbInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4c22-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4c22-108">Pointeur vers une structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) qui contient un handle de base de données opaque et des pointeurs de fonction de rappel pour interroger, définir et libérer des informations.</span><span class="sxs-lookup"><span data-stu-id="f4c22-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure which contains an opaque database handle and callback function pointers to query, set, and free information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4c22-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f4c22-109">Return value</span></span>

<span data-ttu-id="f4c22-110">Si cette fonction réussit, elle retourne SCESTATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="f4c22-110">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="f4c22-111">Sinon, elle retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f4c22-111">Otherwise it returns an error code.</span></span> <span data-ttu-id="f4c22-112">Pour plus d’informations sur les codes d’erreur de configuration de la sécurité, consultez [Attachment Return values](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f4c22-112">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f4c22-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f4c22-113">Remarks</span></span>

<span data-ttu-id="f4c22-114">La fonction **SceSvcAttachmentAnalyze** doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4c22-114">The **SceSvcAttachmentAnalyze** function must do the following:</span></span>

-   <span data-ttu-id="f4c22-115">Interroger directement les informations de configuration à partir du service.</span><span class="sxs-lookup"><span data-stu-id="f4c22-115">Directly query configuration information from the service.</span></span>
-   <span data-ttu-id="f4c22-116">Appelez la fonction de rappel vers laquelle pointe le membre **pfQueryInfo** de la structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) pour récupérer les informations de la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f4c22-116">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve information from the security database.</span></span>
-   <span data-ttu-id="f4c22-117">Calcule les différences entre les informations en fonction du type et de la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="f4c22-117">Compute the differences between the information based on type and syntax.</span></span>
-   <span data-ttu-id="f4c22-118">Appelez la fonction de rappel vers laquelle pointe le membre **pfSetInfo** de la structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) pour mettre à jour la base de données de sécurité avec les informations de service récupérées différentes.</span><span class="sxs-lookup"><span data-stu-id="f4c22-118">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo) to update the security database with the retrieved service information that is different.</span></span>

<span data-ttu-id="f4c22-119">Pour plus d’informations, consultez [implémentation de SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="f4c22-119">For more information, see [Implementing SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4c22-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4c22-120">Requirements</span></span>



| <span data-ttu-id="f4c22-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4c22-121">Requirement</span></span> | <span data-ttu-id="f4c22-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4c22-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f4c22-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4c22-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f4c22-124">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4c22-124">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f4c22-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4c22-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f4c22-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4c22-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4c22-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4c22-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4c22-128">Implémentation de SceSvcAttachmentAnalyze</span><span class="sxs-lookup"><span data-stu-id="f4c22-128">Implementing SceSvcAttachmentAnalyze</span></span>](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[<span data-ttu-id="f4c22-129">**\_informations de rappel SCESVC \_**</span><span class="sxs-lookup"><span data-stu-id="f4c22-129">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="f4c22-130">**SceSvcAttachmentConfig**</span><span class="sxs-lookup"><span data-stu-id="f4c22-130">**SceSvcAttachmentConfig**</span></span>](scesvcattachmentconfig.md)
</dt> </dl>

 

 




