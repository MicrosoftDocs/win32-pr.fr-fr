---
title: Structure TSMF_SUPPORT_NODEDATA_IN
description: Utilisé à l’intérieur des \_ données de prise en charge TSMF \_ dans la \_ structure pour contenir des informations sur les formats multimédias pris en charge.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_IN structure Services Bureau à distance
- Pointeur de structure PTSMF_SUPPORT_NODEDATA_IN Services Bureau à distance
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c36d18ea0e97da8df60475855c93755727fa87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510147"
---
# <a name="tsmf_support_nodedata_in-structure"></a><span data-ttu-id="b4232-105">TSMF \_ prend en charge \_ NODEDATA \_ dans la structure</span><span class="sxs-lookup"><span data-stu-id="b4232-105">TSMF\_SUPPORT\_NODEDATA\_IN structure</span></span>

<span data-ttu-id="b4232-106">Utilisé à l’intérieur des [**\_ \_ données \_ de prise en charge TSMF dans**](tsmf-support-data-in.md) la structure pour contenir des informations sur les formats multimédias pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b4232-106">Used inside the [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure to contain information about supported media formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4232-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4232-107">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_IN {
  UINT32           byteCount;
  INT64            nodeId;
  UINT32           numMediaTypes;
  TS_AM_MEDIA_TYPE ...;
} TSMF_SUPPORT_NODEDATA_IN, *PTSMF_SUPPORT_NODEDATA_IN;
```



## <a name="members"></a><span data-ttu-id="b4232-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b4232-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4232-109">**byteCount**</span><span class="sxs-lookup"><span data-stu-id="b4232-109">**byteCount**</span></span>
</dt> <dd>

<span data-ttu-id="b4232-110">Taille de la structure en octets.</span><span class="sxs-lookup"><span data-stu-id="b4232-110">The size of the structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b4232-111">**ID**</span><span class="sxs-lookup"><span data-stu-id="b4232-111">**nodeId**</span></span>
</dt> <dd>

<span data-ttu-id="b4232-112">Nœud.</span><span class="sxs-lookup"><span data-stu-id="b4232-112">The node.</span></span>

</dd> <dt>

<span data-ttu-id="b4232-113">**numMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="b4232-113">**numMediaTypes**</span></span>
</dt> <dd>

<span data-ttu-id="b4232-114">Nombre de structures de format de média.</span><span class="sxs-lookup"><span data-stu-id="b4232-114">The number of media format structures.</span></span>

</dd> <dt>

<span data-ttu-id="b4232-115">**...**</span><span class="sxs-lookup"><span data-stu-id="b4232-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="b4232-116">Nombre variable de structures définissant les formats de média audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="b4232-116">A variable number of structures defining audio or video media formats.</span></span> <span data-ttu-id="b4232-117">Le **type de fichier** est **\_ WaveFormatEx** pour le format audio ou **\_ MFVideoFormat** pour la vidéo.</span><span class="sxs-lookup"><span data-stu-id="b4232-117">The **FormatType** is either **FORMAT\_WaveFormatEx** for audio or **FORMAT\_MFVideoFormat** for video.</span></span>

<span data-ttu-id="b4232-118">Pour plus d’informations sur cette structure, consultez [ \_ structure du \_ \_ type de média TS](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).</span><span class="sxs-lookup"><span data-stu-id="b4232-118">For details of this structure, see [TS\_AM\_MEDIA\_TYPE Structure](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4232-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4232-119">Requirements</span></span>



| <span data-ttu-id="b4232-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4232-120">Requirement</span></span> | <span data-ttu-id="b4232-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4232-121">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="b4232-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4232-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b4232-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4232-123">None supported</span></span><br/>         |
| <span data-ttu-id="b4232-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4232-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b4232-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4232-125">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4232-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4232-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4232-127">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="b4232-127">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="b4232-128">**\_ \_ données de support TSMF \_ dans**</span><span class="sxs-lookup"><span data-stu-id="b4232-128">**TSMF\_SUPPORT\_DATA\_IN**</span></span>](tsmf-support-data-in.md)
</dt> </dl>

 

