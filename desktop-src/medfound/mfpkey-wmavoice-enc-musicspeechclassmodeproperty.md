---
description: Spécifie le mode du codec vocal.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9776c76f2a8863afe73626f5a2940de2c0ccb7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531833"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a><span data-ttu-id="963c9-103">MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode, propriété</span><span class="sxs-lookup"><span data-stu-id="963c9-103">MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode Property</span></span>

<span data-ttu-id="963c9-104">Spécifie le mode du codec vocal.</span><span class="sxs-lookup"><span data-stu-id="963c9-104">Specifies the mode of the voice codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="963c9-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="963c9-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="963c9-106">\_wszWMACMusicSpeechClassMode g</span><span class="sxs-lookup"><span data-stu-id="963c9-106">g\_wszWMACMusicSpeechClassMode</span></span>

## <a name="data-type"></a><span data-ttu-id="963c9-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="963c9-107">Data Type</span></span>

<span data-ttu-id="963c9-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="963c9-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="963c9-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="963c9-109">Default Value</span></span>

<span data-ttu-id="963c9-110">1</span><span class="sxs-lookup"><span data-stu-id="963c9-110">1</span></span>

## <a name="remarks"></a><span data-ttu-id="963c9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="963c9-111">Remarks</span></span>

<span data-ttu-id="963c9-112">La valeur 1 indique au codec que le contenu est uniquement vocal, la valeur 2 le codec détermine le mode automatiquement et toute autre valeur informe le codec pour qu’il utilise le mode musique.</span><span class="sxs-lookup"><span data-stu-id="963c9-112">A value of 1 informs the codec that the content is voice-only, a value of 2 has the codec determine the mode automatically, and any other value informs the codec to use music mode.</span></span>

<span data-ttu-id="963c9-113">Si le mode automatique n’encode pas correctement la voix mixte et la musique, vous pouvez spécifier l’encodage pour des sections individuelles du fichier à l’aide de la propriété [ \_ \_ \_ EDL MFPKEY WMAVOICE enc](mfpkey-wmavoice-enc-edlproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="963c9-113">If automatic mode is not encoding mixed voice and music properly, you can specify encoding for individual sections of the file by using the [MFPKEY\_WMAVOICE\_ENC\_EDL](mfpkey-wmavoice-enc-edlproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="963c9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="963c9-114">Requirements</span></span>



| <span data-ttu-id="963c9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="963c9-115">Requirement</span></span> | <span data-ttu-id="963c9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="963c9-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="963c9-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="963c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="963c9-118">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="963c9-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="963c9-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="963c9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="963c9-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="963c9-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="963c9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="963c9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="963c9-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="963c9-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="963c9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="963c9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="963c9-124">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="963c9-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




