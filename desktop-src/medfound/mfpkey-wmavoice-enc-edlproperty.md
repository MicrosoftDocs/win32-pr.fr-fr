---
description: Spécifie les portions de contenu à encoder en musique par le codec vocal.
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: MFPKEY_WMAVOICE_ENC_EDL, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f3ac85ebd3a0542fbcf6554205d0b2f2623957c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755308"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a><span data-ttu-id="e6a5e-103">\_ \_ Propriété EDL MFPKEY WMAVOICE enc \_</span><span class="sxs-lookup"><span data-stu-id="e6a5e-103">MFPKEY\_WMAVOICE\_ENC\_EDL Property</span></span>

<span data-ttu-id="e6a5e-104">Spécifie les portions de contenu à encoder en musique par le codec vocal.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-104">Specifies the portions of content to be encoded as music by the voice codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e6a5e-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e6a5e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e6a5e-106">\_wszWMACVoiceBuffer g</span><span class="sxs-lookup"><span data-stu-id="e6a5e-106">g\_wszWMACVoiceBuffer</span></span>

## <a name="data-type"></a><span data-ttu-id="e6a5e-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="e6a5e-107">Data Type</span></span>

<span data-ttu-id="e6a5e-108">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="e6a5e-108">VT\_BSTR</span></span>

## <a name="default-value"></a><span data-ttu-id="e6a5e-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e6a5e-109">Default Value</span></span>

<span data-ttu-id="e6a5e-110">Pas de valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-110">No default value.</span></span> <span data-ttu-id="e6a5e-111">Si cette propriété n’est pas définie, le codec utilise la valeur de la propriété [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) pour déterminer le mode d’encodage du contenu.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-111">If this property is not set, the codec will use the value of the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property to determine how to encode the content.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6a5e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e6a5e-112">Remarks</span></span>

<span data-ttu-id="e6a5e-113">Vous pouvez utiliser cette propriété si le mode automatique du codec ne donne pas de résultats satisfaisants.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-113">You can use this property if the automatic mode of the codec is not giving satisfactory results.</span></span>

<span data-ttu-id="e6a5e-114">Cette valeur est une chaîne délimitée par des virgules contenant au moins quatre entiers.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-114">This value is a comma-delimited string containing at least four integers.</span></span> <span data-ttu-id="e6a5e-115">Le premier entier est le numéro de version ; Utilisez toujours 1 pour cette valeur.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-115">The first integer is the version number; always use 1 for this value.</span></span> <span data-ttu-id="e6a5e-116">Le deuxième entier est le nombre de sections qui doivent être encodées en tant que musique.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-116">The second integer is the number of sections that need to be encoded as music.</span></span> <span data-ttu-id="e6a5e-117">Le deuxième entier est un nombre de paires de valeurs représentant des plages en millisecondes, une paire pour chaque section de contenu qui doit être encodée en musique.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-117">Following the second integer are a number of pairs of values representing ranges in milliseconds, one pair for each section of content that needs to be encoded as music.</span></span>

<span data-ttu-id="e6a5e-118">Par exemple, « 1, 2100200500600 » indique à l’encodeur d’utiliser la version 1 avec 2 sections de musique.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-118">For example, "1,2,100,200,500,600" informs the encoder to use version 1 with 2 sections of music.</span></span> <span data-ttu-id="e6a5e-119">La première section musicale commence à 100 ms et se termine à 200 ms.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-119">The first music section starts at 100 ms and ends at 200 ms.</span></span> <span data-ttu-id="e6a5e-120">La deuxième section musique commence à 500 ms et se termine à 600 ms.</span><span class="sxs-lookup"><span data-stu-id="e6a5e-120">The second music section starts at 500 ms and ends at 600 ms.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a5e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6a5e-121">Requirements</span></span>



| <span data-ttu-id="e6a5e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6a5e-122">Requirement</span></span> | <span data-ttu-id="e6a5e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6a5e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a5e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6a5e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e6a5e-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6a5e-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e6a5e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6a5e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e6a5e-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6a5e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e6a5e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6a5e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6a5e-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6a5e-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6a5e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6a5e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a5e-131">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e6a5e-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




