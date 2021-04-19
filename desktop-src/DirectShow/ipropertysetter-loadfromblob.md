---
description: La méthode LoadFromBlob charge les données de propriété à partir d’un format de persistance.
ms.assetid: b314a844-2190-469a-a030-4494e2140ce6
title: 'IPropertySetter :: LoadFromBlob, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadFromBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a1e58aa5802e8fcb05c2464fc1f121ee1e86f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542479"
---
# <a name="ipropertysetterloadfromblob-method"></a><span data-ttu-id="200ca-103">IPropertySetter :: LoadFromBlob, méthode</span><span class="sxs-lookup"><span data-stu-id="200ca-103">IPropertySetter::LoadFromBlob method</span></span>

> [!Note]  
> <span data-ttu-id="200ca-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="200ca-104">\[Deprecated.</span></span> <span data-ttu-id="200ca-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="200ca-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="200ca-106">La `LoadFromBlob` méthode charge des données de propriété à partir d’un format de persistance.</span><span class="sxs-lookup"><span data-stu-id="200ca-106">The `LoadFromBlob` method loads property data from a persistence format.</span></span>

## <a name="syntax"></a><span data-ttu-id="200ca-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="200ca-107">Syntax</span></span>


```C++
HRESULT LoadFromBlob(
  [in] LONG cSize,
  [in] BYTE *pb
);
```



## <a name="parameters"></a><span data-ttu-id="200ca-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="200ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="200ca-109">*cSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="200ca-109">*cSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="200ca-110">Taille des données, en octets.</span><span class="sxs-lookup"><span data-stu-id="200ca-110">Size of the data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="200ca-111">*PB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="200ca-111">*pb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="200ca-112">Pointeur vers un tableau d’octets qui contient les données.</span><span class="sxs-lookup"><span data-stu-id="200ca-112">Pointer to an array of bytes that contains the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="200ca-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="200ca-113">Return value</span></span>

<span data-ttu-id="200ca-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="200ca-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="200ca-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="200ca-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="200ca-116">Notes</span><span class="sxs-lookup"><span data-stu-id="200ca-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="200ca-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="200ca-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="200ca-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="200ca-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="200ca-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="200ca-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="200ca-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="200ca-120">Requirements</span></span>



| <span data-ttu-id="200ca-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="200ca-121">Requirement</span></span> | <span data-ttu-id="200ca-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="200ca-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="200ca-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="200ca-123">Header</span></span><br/>  | <dl> <span data-ttu-id="200ca-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="200ca-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="200ca-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="200ca-125">Library</span></span><br/> | <dl> <span data-ttu-id="200ca-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="200ca-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="200ca-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="200ca-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="200ca-128">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="200ca-128">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="200ca-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="200ca-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




