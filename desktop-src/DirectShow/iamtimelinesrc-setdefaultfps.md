---
description: La méthode SetDefaultFPS définit la fréquence d’images par défaut de l’objet source.
ms.assetid: ea93acde-3e05-43d5-8130-9ab2ee841b4e
title: 'IAMTimelineSrc :: SetDefaultFPS, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd15f0606b1a4e4ee1aacdb1b3f56d63a024708b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534786"
---
# <a name="iamtimelinesrcsetdefaultfps-method"></a><span data-ttu-id="7501c-103">IAMTimelineSrc :: SetDefaultFPS, méthode</span><span class="sxs-lookup"><span data-stu-id="7501c-103">IAMTimelineSrc::SetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="7501c-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7501c-104">\[Deprecated.</span></span> <span data-ttu-id="7501c-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7501c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7501c-106">La `SetDefaultFPS` méthode définit la fréquence d’images par défaut de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="7501c-106">The `SetDefaultFPS` method sets the source object's default frame rate.</span></span>

## <a name="syntax"></a><span data-ttu-id="7501c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7501c-107">Syntax</span></span>


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="7501c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7501c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7501c-109">*i/s*</span><span class="sxs-lookup"><span data-stu-id="7501c-109">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="7501c-110">Fréquence d’images par défaut, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="7501c-110">Default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7501c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7501c-111">Return value</span></span>

<span data-ttu-id="7501c-112">Retourne S \_ OK en cas de réussite, ou E \_ INVALIDARG si la fréquence d’images spécifiée est inférieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="7501c-112">Returns S\_OK if successful, or E\_INVALIDARG if the specified frame rate is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7501c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7501c-113">Remarks</span></span>

<span data-ttu-id="7501c-114">Le moteur de rendu utilise cette valeur s’il ne parvient pas à déterminer la fréquence d’images à partir du fichier source d’origine.</span><span class="sxs-lookup"><span data-stu-id="7501c-114">The render engine uses this value if it cannot determine the frame rate from the original source file.</span></span>

<span data-ttu-id="7501c-115">Appelez cette méthode uniquement pour les fichiers sources sans fréquence d’images prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="7501c-115">Call this method only for source files without a predefined frame rate.</span></span> <span data-ttu-id="7501c-116">Pour les fichiers bitmap et JPEG, la fréquence d’images par défaut est zéro, ce qui entraîne le rendu de la source sous la forme d’une image continue.</span><span class="sxs-lookup"><span data-stu-id="7501c-116">For bitmap and JPEG files, the default frame rate is zero, which causes the source to be rendered as a still image.</span></span> <span data-ttu-id="7501c-117">Pour utiliser l’image comme première image dans une séquence DIB, définissez la fréquence d’images sur une valeur supérieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="7501c-117">To use the image as the first frame in a DIB sequence set the frame rate to a value greater than zero.</span></span> <span data-ttu-id="7501c-118">Pour plus d’informations, consultez [utilisation des sources](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="7501c-118">For more information, see [Working with Sources](working-with-sources.md).</span></span>

> [!Note]  
> <span data-ttu-id="7501c-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="7501c-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7501c-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7501c-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7501c-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7501c-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7501c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7501c-122">Requirements</span></span>



| <span data-ttu-id="7501c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7501c-123">Requirement</span></span> | <span data-ttu-id="7501c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7501c-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7501c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="7501c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7501c-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7501c-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7501c-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7501c-127">Library</span></span><br/> | <dl> <span data-ttu-id="7501c-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7501c-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7501c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7501c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7501c-130">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="7501c-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="7501c-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="7501c-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




