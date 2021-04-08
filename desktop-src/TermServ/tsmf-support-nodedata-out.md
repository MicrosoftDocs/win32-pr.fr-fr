---
title: Structure TSMF_SUPPORT_NODEDATA_OUT
description: Utilisé dans la \_ \_ structure de données de prise en charge \_ de TSMF pour contenir des informations sur les formats multimédias pris en charge.
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_OUT structure Services Bureau à distance
- Pointeur de structure PTSMF_SUPPORT_NODEDATA_OUT Services Bureau à distance
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 517170e9d6580f69b59f71e0994351ebe0484ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843841"
---
# <a name="tsmf_support_nodedata_out-structure"></a><span data-ttu-id="2a191-105">TSMF \_ prise en charge de la \_ \_ structure NODEDATA out</span><span class="sxs-lookup"><span data-stu-id="2a191-105">TSMF\_SUPPORT\_NODEDATA\_OUT structure</span></span>

<span data-ttu-id="2a191-106">Utilisé dans la structure de [**données de prise en charge de TSMF pour contenir des informations sur \_ \_ \_ les**](tsmf-support-data-out.md) formats multimédias pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2a191-106">Used inside the [**TSMF\_SUPPORT\_DATA\_OUT**](tsmf-support-data-out.md) structure to contain information about supported media formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a191-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a191-107">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_OUT {
  INT64   nodeId;
  HRESULT hrSupportStatus;
  CLSID   clsidNewSink;
  UINT32  supportedMediaTypeIndex;
} TSMF_SUPPORT_NODEDATA_OUT, *PTSMF_SUPPORT_NODEDATA_OUT;
```



## <a name="members"></a><span data-ttu-id="2a191-108">Membres</span><span class="sxs-lookup"><span data-stu-id="2a191-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2a191-109">**ID**</span><span class="sxs-lookup"><span data-stu-id="2a191-109">**nodeId**</span></span>
</dt> <dd>

<span data-ttu-id="2a191-110">Nœud.</span><span class="sxs-lookup"><span data-stu-id="2a191-110">The node.</span></span>

</dd> <dt>

<span data-ttu-id="2a191-111">**hrSupportStatus**</span><span class="sxs-lookup"><span data-stu-id="2a191-111">**hrSupportStatus**</span></span>
</dt> <dd>

<span data-ttu-id="2a191-112">Indique si le récepteur identifié par le paramètre *clsidNewSink* est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2a191-112">Whether the sink identified by the *clsidNewSink* parameter is supported.</span></span>

<span data-ttu-id="2a191-113">Les valeurs possibles sont.</span><span class="sxs-lookup"><span data-stu-id="2a191-113">The possible values are.</span></span>

<dt>

<span data-ttu-id="2a191-114">0</span><span class="sxs-lookup"><span data-stu-id="2a191-114">0</span></span>
</dt> <dd>

<span data-ttu-id="2a191-115">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a191-115">Not supported</span></span>

</dd> <dt>

<span data-ttu-id="2a191-116">1</span><span class="sxs-lookup"><span data-stu-id="2a191-116">1</span></span>
</dt> <dd>

<span data-ttu-id="2a191-117">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a191-117">Supported</span></span>

</dd> </dl>

<span data-ttu-id="2a191-118">Les autres valeurs ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="2a191-118">Other values are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="2a191-119">**clsidNewSink**</span><span class="sxs-lookup"><span data-stu-id="2a191-119">**clsidNewSink**</span></span>
</dt> <dd>

<span data-ttu-id="2a191-120">Récepteur associé au type de média.</span><span class="sxs-lookup"><span data-stu-id="2a191-120">The sink associated with the media type.</span></span>

</dd> <dt>

<span data-ttu-id="2a191-121">**supportedMediaTypeIndex**</span><span class="sxs-lookup"><span data-stu-id="2a191-121">**supportedMediaTypeIndex**</span></span>
</dt> <dd>

<span data-ttu-id="2a191-122">Index de base zéro du type de média pris en charge par le récepteur.</span><span class="sxs-lookup"><span data-stu-id="2a191-122">The zero-based index of the media type supported by the sink.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a191-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a191-123">Requirements</span></span>



| <span data-ttu-id="2a191-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a191-124">Requirement</span></span> | <span data-ttu-id="2a191-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a191-125">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="2a191-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a191-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2a191-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a191-127">None supported</span></span><br/>         |
| <span data-ttu-id="2a191-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a191-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2a191-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2a191-129">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a191-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a191-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a191-131">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="2a191-131">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="2a191-132">**TSMF \_ prennent en charge \_ \_ les données sortantes**</span><span class="sxs-lookup"><span data-stu-id="2a191-132">**TSMF\_SUPPORT\_DATA\_OUT**</span></span>](tsmf-support-data-out.md)
</dt> </dl>

 

 





