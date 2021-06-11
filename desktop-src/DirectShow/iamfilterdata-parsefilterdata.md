---
description: En savoir plus sur la méthode IAMFilterData ::P arseFilterData, décompresse les données de Registre binaires pour un filtre. Cette interface a été déconseillée.
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
ms.openlocfilehash: 9560280fa6f16699af907cdb5cf682b9c4bb1277
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989444"
---
# <a name="iamfilterdataparsefilterdata-method"></a><span data-ttu-id="ffb18-104">IAMFilterData ::P méthode arseFilterData</span><span class="sxs-lookup"><span data-stu-id="ffb18-104">IAMFilterData::ParseFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="ffb18-105">Cette interface a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="ffb18-105">This interface has been deprecated.</span></span> <span data-ttu-id="ffb18-106">Les nouvelles applications ne doivent pas l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="ffb18-106">New applications should not use it.</span></span>

 

<span data-ttu-id="ffb18-107">La `ParseFilterData` méthode décompresse les données de Registre binaires pour un filtre.</span><span class="sxs-lookup"><span data-stu-id="ffb18-107">The `ParseFilterData` method unpacks the binary registry data for a filter.</span></span>

<span data-ttu-id="ffb18-108">Il n’y a généralement aucune raison pour qu’une application appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="ffb18-108">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="ffb18-109">La méthode [**IFilterMapper2 :: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) offre un moyen plus pratique d’accéder aux données de registre de filtre.</span><span class="sxs-lookup"><span data-stu-id="ffb18-109">The [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method provides a more convenient way to access the filter registry data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffb18-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffb18-110">Syntax</span></span>


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a><span data-ttu-id="ffb18-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffb18-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffb18-112">*rgbFilterData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ffb18-112">*rgbFilterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb18-113">Pointeur vers les données de Registre binaires.</span><span class="sxs-lookup"><span data-stu-id="ffb18-113">Pointer to the binary registry data.</span></span> <span data-ttu-id="ffb18-114">Vous pouvez récupérer ces données en extrayant la propriété « FilterData » du moniker de filtre.</span><span class="sxs-lookup"><span data-stu-id="ffb18-114">You can get this data by retrieving the "FilterData" property from the filter moniker.</span></span> <span data-ttu-id="ffb18-115">Les données sont stockées sous la forme d’un **SAFEARRAY** d’octets ( \_ tableau VT UI1 \| VT \_ ).</span><span class="sxs-lookup"><span data-stu-id="ffb18-115">The data is stored as a **SAFEARRAY** of bytes (VT\_UI1 \| VT\_ARRAY).</span></span>

</dd> <dt>

<span data-ttu-id="ffb18-116">*CB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ffb18-116">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb18-117">Spécifie la taille des données binaires, en octets.</span><span class="sxs-lookup"><span data-stu-id="ffb18-117">Specifies the size of the binary data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ffb18-118">*prgbRegFilter2* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ffb18-118">*prgbRegFilter2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb18-119">Adresse d’une variable qui reçoit un pointeur vers les données décompressées.</span><span class="sxs-lookup"><span data-stu-id="ffb18-119">Address of a variable that receives a pointer to the unpacked data.</span></span> <span data-ttu-id="ffb18-120">Lorsque la méthode retourne, effectuez un cast de ce pointeur vers un type [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) pour accéder aux données de filtre.</span><span class="sxs-lookup"><span data-stu-id="ffb18-120">When the method returns, cast this pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) type to access the filter data.</span></span> <span data-ttu-id="ffb18-121">L’appelant doit libérer la mémoire en appelant la méthode **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="ffb18-121">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffb18-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ffb18-122">Return value</span></span>

<span data-ttu-id="ffb18-123">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ffb18-123">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="ffb18-124">En cas d'échec, retourne un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="ffb18-124">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffb18-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="ffb18-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ffb18-126">L’en-tête de \_ données. h se trouve dans le répertoire de l' [exemple du mappeur](mapper-sample.md) dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="ffb18-126">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ffb18-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ffb18-127">Requirements</span></span>



| <span data-ttu-id="ffb18-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffb18-128">Requirement</span></span> | <span data-ttu-id="ffb18-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffb18-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffb18-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffb18-130">Header</span></span><br/> | <dl> <span data-ttu-id="ffb18-131"><dt>Données de fil \_ . h</dt></span><span class="sxs-lookup"><span data-stu-id="ffb18-131"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="ffb18-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ffb18-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="ffb18-133"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffb18-133"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ffb18-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffb18-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffb18-135">**Interface IAMFilterData**</span><span class="sxs-lookup"><span data-stu-id="ffb18-135">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




