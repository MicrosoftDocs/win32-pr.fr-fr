---
description: Spécifie si le flux de bits vidéo encodé contient une valeur de saturation de la mémoire tampon avec chaque image clé.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: MFPKEY_BUFFERFULLNESSINFIRSTBYTE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fbcdb6306faeb7481f1cc7be20088ff0cedd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521977"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a><span data-ttu-id="d7e3e-103">MFPKEY \_ propriété BUFFERFULLNESSINFIRSTBYTE</span><span class="sxs-lookup"><span data-stu-id="d7e3e-103">MFPKEY\_BUFFERFULLNESSINFIRSTBYTE Property</span></span>

<span data-ttu-id="d7e3e-104">Spécifie si le flux de bits vidéo encodé contient une valeur de saturation de la mémoire tampon avec chaque image clé.</span><span class="sxs-lookup"><span data-stu-id="d7e3e-104">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d7e3e-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d7e3e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d7e3e-106">\_wszWMVCBufferFullnessInFirstByte g</span><span class="sxs-lookup"><span data-stu-id="d7e3e-106">g\_wszWMVCBufferFullnessInFirstByte</span></span>

## <a name="data-type"></a><span data-ttu-id="d7e3e-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="d7e3e-107">Data Type</span></span>

<span data-ttu-id="d7e3e-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="d7e3e-108">VT\_BOOL</span></span>

## <a name="remarks"></a><span data-ttu-id="d7e3e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d7e3e-109">Remarks</span></span>

<span data-ttu-id="d7e3e-110">Vous devez définir un type de sortie avant d’obtenir cette valeur.</span><span class="sxs-lookup"><span data-stu-id="d7e3e-110">You must set an output type before getting this value.</span></span>

<span data-ttu-id="d7e3e-111">Vous pouvez récupérer la valeur de cette propriété à l’aide de [IWMCodecProps :: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span><span class="sxs-lookup"><span data-stu-id="d7e3e-111">You can get the value of this property using [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span></span> <span data-ttu-id="d7e3e-112">Si vous utilisez **IPropertyBag**, vous devez d’abord définir la valeur FourCC du format compressé souhaité avec la [propriété \_ FourCC MFPKEY](mfpkey-fourccproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="d7e3e-112">If you use **IPropertyBag**, you must first set the FOURCC value of the desired compressed format with the [MFPKEY\_FOURCC](mfpkey-fourccproperty.md) property.</span></span>

<span data-ttu-id="d7e3e-113">La saturation de la mémoire tampon dans le premier octet de toutes les images clés vous permet de déterminer la taille de mémoire tampon requise lors de la concaténation de flux vidéo compressés.</span><span class="sxs-lookup"><span data-stu-id="d7e3e-113">Having the buffer fullness in the first byte of all key frames enables you to determine the buffer size required when concatenating compressed video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7e3e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7e3e-114">Requirements</span></span>



| <span data-ttu-id="d7e3e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7e3e-115">Requirement</span></span> | <span data-ttu-id="d7e3e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7e3e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7e3e-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7e3e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d7e3e-118">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7e3e-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d7e3e-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7e3e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d7e3e-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7e3e-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7e3e-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7e3e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7e3e-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7e3e-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7e3e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7e3e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7e3e-124">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d7e3e-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




