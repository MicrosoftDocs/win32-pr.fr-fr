---
description: Notez que cette interface est dépréciée.
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: 'IAMFilterData :: CreateFilterData, méthode (fil \_ Data. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.CreateFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 4c83f19de8e709f9890b23957f730fbbac12dd7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540242"
---
# <a name="iamfilterdatacreatefilterdata-method"></a><span data-ttu-id="8c8e1-103">IAMFilterData :: CreateFilterData, méthode</span><span class="sxs-lookup"><span data-stu-id="8c8e1-103">IAMFilterData::CreateFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="8c8e1-104">Cette interface a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-104">This interface has been deprecated.</span></span> <span data-ttu-id="8c8e1-105">Les nouvelles applications ne doivent pas l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-105">New applications should not use it.</span></span>

 

<span data-ttu-id="8c8e1-106">La `CreateFilterData` méthode crée des données de Registre binaires pour un filtre.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-106">The `CreateFilterData` method creates binary registry data for a filter.</span></span> <span data-ttu-id="8c8e1-107">Ces données peuvent être écrites dans le Registre sous la forme d’une \_ sous-clé binaire reg nommée FilterData, sous la clé CLSID du filtre.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-107">This data can be written to the registry as a REG\_BINARY subkey named FilterData, under the filter's CLSID key.</span></span>

<span data-ttu-id="8c8e1-108">Il n’y a généralement aucune raison pour qu’une application appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-108">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="8c8e1-109">La méthode [**IFilterMapper2 :: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) crée automatiquement les données binaires et les ajoute à l’emplacement approprié dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-109">The [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method automatically creates the binary data and adds it to the correct location in the registry.</span></span> <span data-ttu-id="8c8e1-110">Pour plus d’informations, consultez [comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="8c8e1-110">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8c8e1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c8e1-111">Syntax</span></span>


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a><span data-ttu-id="8c8e1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c8e1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c8e1-113">*prf2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c8e1-113">*prf2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c8e1-114">Pointeur vers une structure [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) qui contient les informations de filtre.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-114">Pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure that contains the filter information.</span></span>

</dd> <dt>

<span data-ttu-id="8c8e1-115">*prgbFilterData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8c8e1-115">*prgbFilterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c8e1-116">Adresse d’une variable qui reçoit un pointeur vers les données binaires.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-116">Address of a variable that receives a pointer to the binary data.</span></span> <span data-ttu-id="8c8e1-117">La méthode alloue la mémoire pour les données.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-117">The method allocates the memory for the data.</span></span> <span data-ttu-id="8c8e1-118">L’appelant doit libérer la mémoire en appelant la méthode **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="8c8e1-118">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> <dt>

<span data-ttu-id="8c8e1-119">*PCB* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8c8e1-119">*pcb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c8e1-120">Pointeur vers une variable qui reçoit la taille des données binaires, en octets.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-120">Pointer to a variable that receives the size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c8e1-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c8e1-121">Return value</span></span>

<span data-ttu-id="8c8e1-122">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-122">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="8c8e1-123">En cas d'échec, retourne un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-123">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c8e1-124">Notes</span><span class="sxs-lookup"><span data-stu-id="8c8e1-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8c8e1-125">L’en-tête de \_ données. h se trouve dans le répertoire de l' [exemple du mappeur](mapper-sample.md) dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="8c8e1-125">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8c8e1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c8e1-126">Requirements</span></span>



| <span data-ttu-id="8c8e1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c8e1-127">Requirement</span></span> | <span data-ttu-id="8c8e1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c8e1-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c8e1-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c8e1-129">Header</span></span><br/> | <dl> <span data-ttu-id="8c8e1-130"><dt>Données de fil \_ . h</dt></span><span class="sxs-lookup"><span data-stu-id="8c8e1-130"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="8c8e1-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8c8e1-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="8c8e1-132"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c8e1-132"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8c8e1-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c8e1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c8e1-134">**Interface IAMFilterData**</span><span class="sxs-lookup"><span data-stu-id="8c8e1-134">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




