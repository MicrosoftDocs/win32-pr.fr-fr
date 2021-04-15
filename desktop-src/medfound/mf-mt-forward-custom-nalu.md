---
description: Spécifie que les types d’unités NAL (Network Abstraction Layer) doivent être transférés sur les exemples de sortie par le décodeur.
ms.assetid: 2A1D8629-EB66-4F72-9AD7-93123D941BB0
title: Attribut MF_MT_FORWARD_CUSTOM_NALU (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a318523f52ab7d65450c4c2f35b7bfbf63d5f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529949"
---
# <a name="mf_mt_forward_custom_nalu-attribute"></a><span data-ttu-id="466ec-103">\_ \_ \_ Attribut Nalu personnalisé MF MT Forward \_</span><span class="sxs-lookup"><span data-stu-id="466ec-103">MF\_MT\_FORWARD\_CUSTOM\_NALU attribute</span></span>

<span data-ttu-id="466ec-104">Spécifie que les types d’unités NAL (Network Abstraction Layer) doivent être transférés sur les exemples de sortie par le décodeur.</span><span class="sxs-lookup"><span data-stu-id="466ec-104">Specifies that network abstraction layer (NAL) unit types should be forwarded on output samples by the decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="466ec-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="466ec-105">Data type</span></span>

<span data-ttu-id="466ec-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="466ec-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="466ec-107">Notes</span><span class="sxs-lookup"><span data-stu-id="466ec-107">Remarks</span></span>

<span data-ttu-id="466ec-108">Si le décodeur analyse un NALU, il ne sera pas transféré.</span><span class="sxs-lookup"><span data-stu-id="466ec-108">If the decoder parses a NALU then it will not be forwarded.</span></span>

## <a name="requirements"></a><span data-ttu-id="466ec-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="466ec-109">Requirements</span></span>



| <span data-ttu-id="466ec-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="466ec-110">Requirement</span></span> | <span data-ttu-id="466ec-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="466ec-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="466ec-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="466ec-112">Minimum supported client</span></span><br/> | <span data-ttu-id="466ec-113">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="466ec-113">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="466ec-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="466ec-114">Minimum supported server</span></span><br/> | <span data-ttu-id="466ec-115">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="466ec-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="466ec-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="466ec-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="466ec-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="466ec-117"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




