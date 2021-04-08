---
description: La fonction SceSvcAttachmentConfig est appelée par le moteur de configuration de sécurité lorsque le système est configuré.
ms.assetid: ad20649a-2391-421b-a08c-a4ea6a882abc
title: SceSvcAttachmentConfig fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentConfig
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c78caa3b8e08ade9c674a11d113a8b91b8f5fad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750869"
---
# <a name="scesvcattachmentconfig-callback-function"></a><span data-ttu-id="7b4cb-103">SceSvcAttachmentConfig fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="7b4cb-103">SceSvcAttachmentConfig callback function</span></span>

<span data-ttu-id="7b4cb-104">La fonction **SceSvcAttachmentConfig** est appelée par le moteur de configuration de sécurité lorsque le système est configuré.</span><span class="sxs-lookup"><span data-stu-id="7b4cb-104">The **SceSvcAttachmentConfig** function is called by the Security Configuration Engine when the system is configured.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b4cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b4cb-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a><span data-ttu-id="7b4cb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b4cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b4cb-107">*pSceCbInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7b4cb-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4cb-108">Pointeur vers une structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) qui contient le handle de base de données et les fonctions de rappel pour interroger, définir et libérer des informations.</span><span class="sxs-lookup"><span data-stu-id="7b4cb-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure that contains the database handle and the callback functions to query, set, and free information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b4cb-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b4cb-109">Return value</span></span>

<span data-ttu-id="7b4cb-110">Si cette fonction réussit, elle retourne SCESTATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="7b4cb-110">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="7b4cb-111">Sinon, elle retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7b4cb-111">Otherwise it returns an error code.</span></span> <span data-ttu-id="7b4cb-112">Pour plus d’informations sur les codes d’erreur de configuration de la sécurité, consultez [Attachment Return values](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7b4cb-112">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7b4cb-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7b4cb-113">Remarks</span></span>

<span data-ttu-id="7b4cb-114">Lors de l’implémentation de cette fonction, utilisez la fonction de rappel vers laquelle pointe le membre **pfQueryInfo** de la structure d’informations de [**\_ rappel \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) pour récupérer les informations de configuration.</span><span class="sxs-lookup"><span data-stu-id="7b4cb-114">When implementing this function, use the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve configuration information.</span></span> <span data-ttu-id="7b4cb-115">Configurez ensuite le service à l’aide des informations retournées.</span><span class="sxs-lookup"><span data-stu-id="7b4cb-115">Then configure the service using the returned information.</span></span>

<span data-ttu-id="7b4cb-116">Cette fonction doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7b4cb-116">This function must do the following:</span></span>

-   <span data-ttu-id="7b4cb-117">Interroger les informations de configuration à partir de l’outil de configuration de la sécurité défini à l’aide de la fonction de rappel désignée par le membre **pfQueryInfo** de la structure SCESVC (pSceCbInfo->pfQueryInfo). [**\_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)</span><span class="sxs-lookup"><span data-stu-id="7b4cb-117">Query configuration information from the Security Configuration tool set using the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo).</span></span>
-   <span data-ttu-id="7b4cb-118">Configurez le service à l’aide des informations de configuration.</span><span class="sxs-lookup"><span data-stu-id="7b4cb-118">Configure the service using the configuration information.</span></span>

<span data-ttu-id="7b4cb-119">Pour plus d’informations, consultez [implémentation de SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)</span><span class="sxs-lookup"><span data-stu-id="7b4cb-119">For more information, see [Implementing SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="7b4cb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b4cb-120">Requirements</span></span>



| <span data-ttu-id="7b4cb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b4cb-121">Requirement</span></span> | <span data-ttu-id="7b4cb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b4cb-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7b4cb-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b4cb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7b4cb-124">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b4cb-124">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7b4cb-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b4cb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7b4cb-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b4cb-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b4cb-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b4cb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b4cb-128">**\_informations de rappel SCESVC \_**</span><span class="sxs-lookup"><span data-stu-id="7b4cb-128">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="7b4cb-129">**SceSvcAttachmentAnalyze**</span><span class="sxs-lookup"><span data-stu-id="7b4cb-129">**SceSvcAttachmentAnalyze**</span></span>](scesvcattachmentanalyze.md)
</dt> </dl>

 

 




