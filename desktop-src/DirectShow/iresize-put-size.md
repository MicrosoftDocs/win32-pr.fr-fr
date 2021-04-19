---
description: La \_ méthode put Size définit la taille de sortie et le mode Stretch.
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: IResize ::p ut_Size, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 579cee086798e64abd07b25cc4f7bb14405157dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537458"
---
# <a name="iresizeput_size-method"></a><span data-ttu-id="bfd52-103">IResize : méthode de taille de :p ut \_</span><span class="sxs-lookup"><span data-stu-id="bfd52-103">IResize::put\_Size method</span></span>

> [!Note]  
> <span data-ttu-id="bfd52-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="bfd52-104">\[Deprecated.</span></span> <span data-ttu-id="bfd52-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bfd52-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bfd52-106">La `put_Size` méthode définit la taille de sortie et le mode Stretch.</span><span class="sxs-lookup"><span data-stu-id="bfd52-106">The `put_Size` method sets the output size and stretch mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfd52-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfd52-107">Syntax</span></span>


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a><span data-ttu-id="bfd52-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfd52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfd52-109">*Hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bfd52-109">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfd52-110">Hauteur vidéo, en pixels.</span><span class="sxs-lookup"><span data-stu-id="bfd52-110">The video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="bfd52-111">*Largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bfd52-111">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfd52-112">Largeur de la vidéo, en pixels.</span><span class="sxs-lookup"><span data-stu-id="bfd52-112">The video width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="bfd52-113">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="bfd52-113">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfd52-114">Mode Stretch.</span><span class="sxs-lookup"><span data-stu-id="bfd52-114">The stretch mode.</span></span> <span data-ttu-id="bfd52-115">Pour connaître les valeurs possibles, consultez [**indicateurs de redimensionnement**](resize-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="bfd52-115">See [**Resize Flags**](resize-flags.md) for possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfd52-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bfd52-116">Return value</span></span>

<span data-ttu-id="bfd52-117">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bfd52-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfd52-118">Notes</span><span class="sxs-lookup"><span data-stu-id="bfd52-118">Remarks</span></span>

<span data-ttu-id="bfd52-119">DES peuvent appeler cette méthode avant ou après l’appel à **put \_ MediaType**.</span><span class="sxs-lookup"><span data-stu-id="bfd52-119">DES may call this method before or after calling **put\_MediaType**.</span></span> <span data-ttu-id="bfd52-120">Si la méthode DES appelle cette méthode avant d’appeler **put \_ MediaType**, le filtre doit sélectionner une valeur par défaut pour la profondeur de bits et utiliser les valeurs size pour construire un type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="bfd52-120">If DES calls this method before calling **put\_MediaType**, the filter should select a default value for the bit depth and use the size values to construct an output media type.</span></span> <span data-ttu-id="bfd52-121">Si la méthode DES appelle cette méthode après avoir appelé **put \_ MediaType**, le filtre doit modifier son type de sortie actuel avec les nouvelles tailles.</span><span class="sxs-lookup"><span data-stu-id="bfd52-121">If DES calls this method after calling **put\_MediaType**, the filter should modify its current output type with the new sizes.</span></span>

<span data-ttu-id="bfd52-122">DES peuvent également appeler cette méthode une fois que la broche de sortie est connectée.</span><span class="sxs-lookup"><span data-stu-id="bfd52-122">DES may also call this method after the output pin is connected.</span></span> <span data-ttu-id="bfd52-123">Dans ce cas, modifiez le type de sortie et reconnectez la broche de sortie avec le nouveau type.</span><span class="sxs-lookup"><span data-stu-id="bfd52-123">In that case, modify the output type and reconnect the output pin with the new type.</span></span> <span data-ttu-id="bfd52-124">Pour plus d’informations, consultez [reconnexion des codes confidentiels](reconnecting-pins.md) .</span><span class="sxs-lookup"><span data-stu-id="bfd52-124">See [Reconnecting Pins](reconnecting-pins.md) for more information.</span></span>

<span data-ttu-id="bfd52-125">Le paramètre *Flags* spécifie la manière dont le filtre doit effectuer l’opération de redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="bfd52-125">The *Flags* parameter specifies how the filter should perform the resizing operation.</span></span>

> [!Note]  
> <span data-ttu-id="bfd52-126">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="bfd52-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bfd52-127">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bfd52-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bfd52-128">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bfd52-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bfd52-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfd52-129">Requirements</span></span>



| <span data-ttu-id="bfd52-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfd52-130">Requirement</span></span> | <span data-ttu-id="bfd52-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfd52-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfd52-132">Version</span><span class="sxs-lookup"><span data-stu-id="bfd52-132">Version</span></span><br/> | <span data-ttu-id="bfd52-133">DirectX 9,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="bfd52-133">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="bfd52-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="bfd52-134">Header</span></span><br/>  | <dl> <span data-ttu-id="bfd52-135"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfd52-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bfd52-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bfd52-136">Library</span></span><br/> | <dl> <span data-ttu-id="bfd52-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfd52-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfd52-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfd52-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfd52-139">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="bfd52-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="bfd52-140">**Interface IResize**</span><span class="sxs-lookup"><span data-stu-id="bfd52-140">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




