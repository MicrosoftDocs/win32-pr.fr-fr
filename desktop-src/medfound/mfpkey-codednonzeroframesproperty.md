---
description: Spécifie le nombre de trames vidéo encodées par le codec qui contiennent réellement des données.
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: MFPKEY_CODEDNONZEROFRAMES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ca5fb26288e2ea9ff801ba13aa7bef570ca95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529815"
---
# <a name="mfpkey_codednonzeroframes-property"></a><span data-ttu-id="56e16-103">MFPKEY \_ propriété CODEDNONZEROFRAMES</span><span class="sxs-lookup"><span data-stu-id="56e16-103">MFPKEY\_CODEDNONZEROFRAMES Property</span></span>

<span data-ttu-id="56e16-104">Spécifie le nombre de trames vidéo encodées par le codec qui contiennent réellement des données.</span><span class="sxs-lookup"><span data-stu-id="56e16-104">Specifies the number of video frames encoded by the codec that actually contain data.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="56e16-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="56e16-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="56e16-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="56e16-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="56e16-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="56e16-107">Data Type</span></span>

<span data-ttu-id="56e16-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="56e16-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="56e16-109">Notes</span><span class="sxs-lookup"><span data-stu-id="56e16-109">Remarks</span></span>

<span data-ttu-id="56e16-110">Cette valeur est égale à [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) moins les images qui ont été supprimées en raison de contraintes de vitesse de transmission, moins les images de zéro octet.</span><span class="sxs-lookup"><span data-stu-id="56e16-110">This value is equal to [MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) minus any frames that were dropped due to bit-rate constraints, minus any zero-byte frames.</span></span> <span data-ttu-id="56e16-111">Vous pouvez récupérer cette valeur une fois que vous avez terminé de passer des exemples.</span><span class="sxs-lookup"><span data-stu-id="56e16-111">You can get this value after you are finished passing samples.</span></span> <span data-ttu-id="56e16-112">Des frames de zéro octet peuvent être créés pour des frames en double.</span><span class="sxs-lookup"><span data-stu-id="56e16-112">Zero-byte frames can be created for duplicate frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="56e16-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56e16-113">Requirements</span></span>



| <span data-ttu-id="56e16-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56e16-114">Requirement</span></span> | <span data-ttu-id="56e16-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="56e16-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56e16-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56e16-116">Minimum supported client</span></span><br/> | <span data-ttu-id="56e16-117">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56e16-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="56e16-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56e16-118">Minimum supported server</span></span><br/> | <span data-ttu-id="56e16-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56e16-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="56e16-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="56e16-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="56e16-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="56e16-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56e16-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56e16-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e16-123">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="56e16-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
