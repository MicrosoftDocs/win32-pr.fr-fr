---
title: Énumération MrmResourceIndexerMessageSeverity (MrmResourceIndexer. h)
description: Définit des constantes qui spécifient la gravité d’un message d’indexeur de ressource. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: A4734256-94BD-43BE-B93C-55B98DF8A9BF
keywords:
- Menus de l’énumération MrmResourceIndexerMessageSeverity et autres ressources
topic_type:
- apiref
api_name:
- MrmResourceIndexerMessageSeverity
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdcbb42291ab88e91eca6c16c0a6c95c3e89fd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106542857"
---
# <a name="mrmresourceindexermessageseverity-enumeration"></a><span data-ttu-id="51382-105">Énumération MrmResourceIndexerMessageSeverity</span><span class="sxs-lookup"><span data-stu-id="51382-105">MrmResourceIndexerMessageSeverity enumeration</span></span>

<span data-ttu-id="51382-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="51382-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="51382-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="51382-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="51382-108">Définit des constantes qui spécifient la gravité d’un message d’indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="51382-108">Defines constants that specify the severity of an resource indexer message.</span></span> <span data-ttu-id="51382-109">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="51382-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="51382-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51382-110">Syntax</span></span>


```C++
typedef enum _MrmResourceIndexerMessageSeverity { 
  MrmResourceIndexerMessageSeverityVerbose  = 1,
  MrmResourceIndexerMessageSeverityInfo     = 2,
  MrmResourceIndexerMessageSeverityWarning  = 3,
  MrmResourceIndexerMessageSeverityError    = 4
} MrmResourceIndexerMessageSeverity;
```



## <a name="constants"></a><span data-ttu-id="51382-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="51382-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="51382-112"><span id="MrmResourceIndexerMessageSeverityVerbose"></span><span id="mrmresourceindexermessageseverityverbose"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYVERBOSE"></span>**MrmResourceIndexerMessageSeverityVerbose**</span><span class="sxs-lookup"><span data-stu-id="51382-112"><span id="MrmResourceIndexerMessageSeverityVerbose"></span><span id="mrmresourceindexermessageseverityverbose"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYVERBOSE"></span>**MrmResourceIndexerMessageSeverityVerbose**</span></span>
</dt> <dd>

<span data-ttu-id="51382-113">Indique que le message est détaillé.</span><span class="sxs-lookup"><span data-stu-id="51382-113">Indicates that the message is verbose.</span></span>

</dd> <dt>

<span data-ttu-id="51382-114"><span id="MrmResourceIndexerMessageSeverityInfo"></span><span id="mrmresourceindexermessageseverityinfo"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYINFO"></span>**MrmResourceIndexerMessageSeverityInfo**</span><span class="sxs-lookup"><span data-stu-id="51382-114"><span id="MrmResourceIndexerMessageSeverityInfo"></span><span id="mrmresourceindexermessageseverityinfo"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYINFO"></span>**MrmResourceIndexerMessageSeverityInfo**</span></span>
</dt> <dd>

<span data-ttu-id="51382-115">Indique que le message est à titre d’information.</span><span class="sxs-lookup"><span data-stu-id="51382-115">Indicates that the message is informational.</span></span>

</dd> <dt>

<span data-ttu-id="51382-116"><span id="MrmResourceIndexerMessageSeverityWarning"></span><span id="mrmresourceindexermessageseveritywarning"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYWARNING"></span>**MrmResourceIndexerMessageSeverityWarning**</span><span class="sxs-lookup"><span data-stu-id="51382-116"><span id="MrmResourceIndexerMessageSeverityWarning"></span><span id="mrmresourceindexermessageseveritywarning"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYWARNING"></span>**MrmResourceIndexerMessageSeverityWarning**</span></span>
</dt> <dd>

<span data-ttu-id="51382-117">Indique que le message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="51382-117">Indicates that the message is a warning.</span></span>

</dd> <dt>

<span data-ttu-id="51382-118"><span id="MrmResourceIndexerMessageSeverityError"></span><span id="mrmresourceindexermessageseverityerror"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYERROR"></span>**MrmResourceIndexerMessageSeverityError**</span><span class="sxs-lookup"><span data-stu-id="51382-118"><span id="MrmResourceIndexerMessageSeverityError"></span><span id="mrmresourceindexermessageseverityerror"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYERROR"></span>**MrmResourceIndexerMessageSeverityError**</span></span>
</dt> <dd>

<span data-ttu-id="51382-119">Indique que le message est une erreur.</span><span class="sxs-lookup"><span data-stu-id="51382-119">Indicates that the message is an error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51382-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51382-120">Requirements</span></span>



| <span data-ttu-id="51382-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51382-121">Requirement</span></span> | <span data-ttu-id="51382-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="51382-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51382-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51382-123">Minimum supported client</span></span><br/> | <span data-ttu-id="51382-124">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51382-124">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="51382-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51382-125">Minimum supported server</span></span><br/> | <span data-ttu-id="51382-126">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51382-126">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="51382-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="51382-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="51382-128"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="51382-128"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51382-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51382-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51382-130">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="51382-130">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

