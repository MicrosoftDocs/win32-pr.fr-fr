---
description: La méthode GetDefaultFPS récupère la fréquence d’images par défaut de l’objet source. Le moteur de rendu utilise cette valeur s’il ne parvient pas à déterminer la fréquence d’images à partir de la source d’origine.
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: 'IAMTimelineSrc :: GetDefaultFPS, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e48ee38f385ba5ff06b2ede9b27b4558dac65270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540141"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a><span data-ttu-id="174ab-104">IAMTimelineSrc :: GetDefaultFPS, méthode</span><span class="sxs-lookup"><span data-stu-id="174ab-104">IAMTimelineSrc::GetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="174ab-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="174ab-105">\[Deprecated.</span></span> <span data-ttu-id="174ab-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="174ab-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="174ab-107">La `GetDefaultFPS` méthode récupère la fréquence d’images par défaut de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="174ab-107">The `GetDefaultFPS` method retrieves the source object's default frame rate.</span></span> <span data-ttu-id="174ab-108">Le moteur de rendu utilise cette valeur s’il ne parvient pas à déterminer la fréquence d’images à partir de la source d’origine.</span><span class="sxs-lookup"><span data-stu-id="174ab-108">The render engine uses this value if it cannot determine the frame rate from the original source.</span></span>

## <a name="syntax"></a><span data-ttu-id="174ab-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="174ab-109">Syntax</span></span>


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="174ab-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="174ab-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="174ab-111">*pFPS*</span><span class="sxs-lookup"><span data-stu-id="174ab-111">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="174ab-112">Reçoit la fréquence d’images par défaut, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="174ab-112">Receives the default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="174ab-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="174ab-113">Return value</span></span>

<span data-ttu-id="174ab-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="174ab-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="174ab-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="174ab-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="174ab-116">Notes</span><span class="sxs-lookup"><span data-stu-id="174ab-116">Remarks</span></span>

<span data-ttu-id="174ab-117">La fréquence d’images par défaut n’est pas requise si le format de fichier spécifie la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="174ab-117">The default frame rate is not required if the file format specifies the frame rate.</span></span> <span data-ttu-id="174ab-118">C’est le cas pour les formats audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="174ab-118">This is the case for audio and video formats.</span></span>

<span data-ttu-id="174ab-119">Si la source est une image bitmap ou JPEG, le moteur de rendu l’utilise comme première image dans une séquence de bitmaps indépendantes du périphérique (DIB, Device-Independent Bitmap), avec une fréquence d’images égale à la fréquence d’images par défaut.</span><span class="sxs-lookup"><span data-stu-id="174ab-119">If the source is a bitmap or JPEG image, the render engine uses it as the first image in a device-independent bitmap (DIB) sequence, with a frame rate equal to the default frame rate.</span></span> <span data-ttu-id="174ab-120">Pour afficher une image statique plutôt qu’une séquence DIB, définissez la fréquence d’images par défaut sur 0.</span><span class="sxs-lookup"><span data-stu-id="174ab-120">To render a static image, rather than a DIB sequence, set the default frame rate to 0.</span></span>

<span data-ttu-id="174ab-121">Si la source est une image GIF, ne définissez pas la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="174ab-121">If the source is a GIF, do not set the frame rate.</span></span> <span data-ttu-id="174ab-122">Pour les images GIF animées, le fichier GIF spécifie le délai entre chaque image.</span><span class="sxs-lookup"><span data-stu-id="174ab-122">For animated GIFs, the GIF file specifies the delay between each image.</span></span>

> [!Note]  
> <span data-ttu-id="174ab-123">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="174ab-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="174ab-124">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="174ab-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="174ab-125">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="174ab-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="174ab-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="174ab-126">Requirements</span></span>



| <span data-ttu-id="174ab-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="174ab-127">Requirement</span></span> | <span data-ttu-id="174ab-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="174ab-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="174ab-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="174ab-129">Header</span></span><br/>  | <dl> <span data-ttu-id="174ab-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="174ab-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="174ab-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="174ab-131">Library</span></span><br/> | <dl> <span data-ttu-id="174ab-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="174ab-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="174ab-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="174ab-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="174ab-134">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="174ab-134">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="174ab-135">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="174ab-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




