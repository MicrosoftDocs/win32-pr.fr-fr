---
description: Représente le type de la source du frame.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: Attribut MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8823a828a81290fe3b039c8959d694c62331622f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524115"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a><span data-ttu-id="01e01-103">\_Attribut de \_ \_ types FRAMESOURCE \_ de l’attribut DEVICESTREAM MF</span><span class="sxs-lookup"><span data-stu-id="01e01-103">MF\_DEVICESTREAM\_ATTRIBUTE\_FRAMESOURCE\_TYPES attribute</span></span>

<span data-ttu-id="01e01-104">Représente le type de la source du frame.</span><span class="sxs-lookup"><span data-stu-id="01e01-104">Represents the frame source type.</span></span>

## <a name="data-type"></a><span data-ttu-id="01e01-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="01e01-105">Data type</span></span>

<span data-ttu-id="01e01-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="01e01-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="01e01-107">Notes</span><span class="sxs-lookup"><span data-stu-id="01e01-107">Remarks</span></span>

<span data-ttu-id="01e01-108">Cette valeur de cet attribut doit être un masque de masque d’une ou de plusieurs valeurs de l’énumération [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) .</span><span class="sxs-lookup"><span data-stu-id="01e01-108">This value of this attribute should be a bitmask of one or more values from the [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) enumeration.</span></span> <span data-ttu-id="01e01-109">Pour prendre en charge la compatibilité descendante, lorsque cet attribut n’est pas défini pour un type de média, il est supposé avoir la valeur **MFFrameSourceTypes :: Color**.</span><span class="sxs-lookup"><span data-stu-id="01e01-109">To support backward compatibility, when this attribute is not defined for a media type, it is assumed to have the value **MFFrameSourceTypes::Color**.</span></span>

## <a name="requirements"></a><span data-ttu-id="01e01-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01e01-110">Requirements</span></span>



| <span data-ttu-id="01e01-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01e01-111">Requirement</span></span> | <span data-ttu-id="01e01-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="01e01-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01e01-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01e01-113">Minimum supported client</span></span><br/> | <span data-ttu-id="01e01-114">Applications de bureau Windows 10, version 1607 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01e01-114">Windows 10, version 1607 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="01e01-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01e01-115">Minimum supported server</span></span><br/> | <span data-ttu-id="01e01-116">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01e01-116">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="01e01-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="01e01-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="01e01-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="01e01-118"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




