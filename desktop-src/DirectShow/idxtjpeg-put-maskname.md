---
description: La \_ méthode put MaskName spécifie le nom d’un fichier JPEG à utiliser comme masque de réinitialisation.
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: IDxtJpeg ::p ut_MaskName, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f74fe09572b95ff1508021b3fa2ae4f9888f2d5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520982"
---
# <a name="idxtjpegput_maskname-method"></a><span data-ttu-id="6809f-103">IDxtJpeg ::p ut \_ MaskName, méthode</span><span class="sxs-lookup"><span data-stu-id="6809f-103">IDxtJpeg::put\_MaskName method</span></span>

> [!Note]  
> <span data-ttu-id="6809f-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="6809f-104">\[Deprecated.</span></span> <span data-ttu-id="6809f-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6809f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6809f-106">La `put_MaskName` méthode spécifie le nom d’un fichier JPEG à utiliser comme masque de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="6809f-106">The `put_MaskName` method specifies the name of a JPEG file to use as the wipe mask.</span></span> <span data-ttu-id="6809f-107">Ce masque sera utilisé à la place de l’un des masques de réinitialisation intégrés.</span><span class="sxs-lookup"><span data-stu-id="6809f-107">This mask will be used instead of one of the built-in wipe masks.</span></span> <span data-ttu-id="6809f-108">Le fichier doit contenir un dégradé monochrome, 8 bits par pixel.</span><span class="sxs-lookup"><span data-stu-id="6809f-108">The file must contain a monochrome, 8-bits-per-pixel gradient.</span></span> <span data-ttu-id="6809f-109">Le dégradé est utilisé comme masque pour définir la progression de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="6809f-109">The gradient is used as a mask to define the wipe's progression.</span></span>

## <a name="syntax"></a><span data-ttu-id="6809f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6809f-110">Syntax</span></span>


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="6809f-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6809f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6809f-112">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6809f-112">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6809f-113">Spécifie le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="6809f-113">Specifies the name of the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6809f-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6809f-114">Return value</span></span>

<span data-ttu-id="6809f-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6809f-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6809f-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6809f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6809f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6809f-117">Remarks</span></span>

<span data-ttu-id="6809f-118">Pour revenir à un masque intégré, définissez la propriété **MaskNum** .</span><span class="sxs-lookup"><span data-stu-id="6809f-118">To revert to a built-in mask, set the **MaskNum** property.</span></span>

> [!Note]  
> <span data-ttu-id="6809f-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="6809f-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6809f-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6809f-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6809f-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6809f-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6809f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6809f-122">Requirements</span></span>



| <span data-ttu-id="6809f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6809f-123">Requirement</span></span> | <span data-ttu-id="6809f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6809f-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6809f-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6809f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6809f-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6809f-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6809f-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6809f-127">Library</span></span><br/> | <dl> <span data-ttu-id="6809f-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6809f-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6809f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6809f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6809f-130">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="6809f-130">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> <dt>

[<span data-ttu-id="6809f-131">**IDxtJpeg ::p ut \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="6809f-131">**IDxtJpeg::put\_MaskNum**</span></span>](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 




