---
description: Notez que cette interface est dépréciée.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: IAMFilterData ::P méthode arseFilterData (fil \_ Data. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.ParseFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 18e1367813adff6b0debdfb698644731668bfc5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542529"
---
# <a name="iamfilterdataparsefilterdata-method"></a><span data-ttu-id="b4951-103">IAMFilterData ::P méthode arseFilterData</span><span class="sxs-lookup"><span data-stu-id="b4951-103">IAMFilterData::ParseFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="b4951-104">Cette interface a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b4951-104">This interface has been deprecated.</span></span> <span data-ttu-id="b4951-105">Les nouvelles applications ne doivent pas l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="b4951-105">New applications should not use it.</span></span>

 

<span data-ttu-id="b4951-106">La `ParseFilterData` méthode décompresse les données de Registre binaires pour un filtre.</span><span class="sxs-lookup"><span data-stu-id="b4951-106">The `ParseFilterData` method unpacks the binary registry data for a filter.</span></span>

<span data-ttu-id="b4951-107">Il n’y a généralement aucune raison pour qu’une application appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b4951-107">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="b4951-108">La méthode [**IFilterMapper2 :: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) offre un moyen plus pratique d’accéder aux données de registre de filtre.</span><span class="sxs-lookup"><span data-stu-id="b4951-108">The [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method provides a more convenient way to access the filter registry data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4951-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4951-109">Syntax</span></span>


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a><span data-ttu-id="b4951-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4951-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4951-111">*rgbFilterData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4951-111">*rgbFilterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4951-112">Pointeur vers les données de Registre binaires.</span><span class="sxs-lookup"><span data-stu-id="b4951-112">Pointer to the binary registry data.</span></span> <span data-ttu-id="b4951-113">Vous pouvez récupérer ces données en extrayant la propriété « FilterData » du moniker de filtre.</span><span class="sxs-lookup"><span data-stu-id="b4951-113">You can get this data by retrieving the "FilterData" property from the filter moniker.</span></span> <span data-ttu-id="b4951-114">Les données sont stockées sous la forme d’un **SAFEARRAY** d’octets ( \_ tableau VT UI1 \| VT \_ ).</span><span class="sxs-lookup"><span data-stu-id="b4951-114">The data is stored as a **SAFEARRAY** of bytes (VT\_UI1 \| VT\_ARRAY).</span></span>

</dd> <dt>

<span data-ttu-id="b4951-115">*CB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4951-115">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4951-116">Spécifie la taille des données binaires, en octets.</span><span class="sxs-lookup"><span data-stu-id="b4951-116">Specifies the size of the binary data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b4951-117">*prgbRegFilter2* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b4951-117">*prgbRegFilter2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4951-118">Adresse d’une variable qui reçoit un pointeur vers les données décompressées.</span><span class="sxs-lookup"><span data-stu-id="b4951-118">Address of a variable that receives a pointer to the unpacked data.</span></span> <span data-ttu-id="b4951-119">Lorsque la méthode retourne, effectuez un cast de ce pointeur vers un type [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) pour accéder aux données de filtre.</span><span class="sxs-lookup"><span data-stu-id="b4951-119">When the method returns, cast this pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) type to access the filter data.</span></span> <span data-ttu-id="b4951-120">L’appelant doit libérer la mémoire en appelant la méthode **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="b4951-120">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4951-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4951-121">Return value</span></span>

<span data-ttu-id="b4951-122">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b4951-122">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="b4951-123">En cas d'échec, retourne un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="b4951-123">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4951-124">Notes</span><span class="sxs-lookup"><span data-stu-id="b4951-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b4951-125">L’en-tête de \_ données. h se trouve dans le répertoire de l' [exemple du mappeur](mapper-sample.md) dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="b4951-125">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b4951-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4951-126">Requirements</span></span>



| <span data-ttu-id="b4951-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4951-127">Requirement</span></span> | <span data-ttu-id="b4951-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4951-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4951-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4951-129">Header</span></span><br/> | <dl> <span data-ttu-id="b4951-130"><dt>Données de fil \_ . h</dt></span><span class="sxs-lookup"><span data-stu-id="b4951-130"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="b4951-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b4951-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="b4951-132"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4951-132"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b4951-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4951-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4951-134">**Interface IAMFilterData**</span><span class="sxs-lookup"><span data-stu-id="b4951-134">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




