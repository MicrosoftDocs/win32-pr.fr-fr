---
description: La méthode QuerySupported détermine si un objet prend en charge un jeu de propriétés spécifié.
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: 'IKsPropertySet :: QuerySupported, méthode (KS. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.QuerySupported
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: a13c8523d45278ad403ee08d0822fb853b301520
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200741"
---
# <a name="ikspropertysetquerysupported-method"></a><span data-ttu-id="9bdc0-103">IKsPropertySet :: QuerySupported, méthode</span><span class="sxs-lookup"><span data-stu-id="9bdc0-103">IKsPropertySet::QuerySupported method</span></span>

<span data-ttu-id="9bdc0-104">La `QuerySupported` méthode détermine si un objet prend en charge un jeu de propriétés spécifié.</span><span class="sxs-lookup"><span data-stu-id="9bdc0-104">The `QuerySupported` method determines whether an object supports a specified property set.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bdc0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9bdc0-105">Syntax</span></span>


```C++
HRESULT QuerySupported(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [out] DWORD   *pTypeSupport
);
```



## <a name="parameters"></a><span data-ttu-id="9bdc0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9bdc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bdc0-107">*guidPropSet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9bdc0-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bdc0-108">GUID du jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="9bdc0-108">Property set GUID.</span></span>

</dd> <dt>

<span data-ttu-id="9bdc0-109">*dwPropID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9bdc0-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bdc0-110">Identificateur de la propriété dans le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="9bdc0-110">Identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="9bdc0-111">*pTypeSupport* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9bdc0-111">*pTypeSupport* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bdc0-112">Pointeur vers une valeur dans laquelle stocker des indicateurs indiquant la prise en charge fournie par le pilote.</span><span class="sxs-lookup"><span data-stu-id="9bdc0-112">Pointer to a value in which to store flags indicating the support provided by the driver.</span></span> <span data-ttu-id="9bdc0-113">Les indicateurs pris en charge sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="9bdc0-113">Supported flags include the following.</span></span>



| <span data-ttu-id="9bdc0-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bdc0-114">Value</span></span>                    | <span data-ttu-id="9bdc0-115">Description</span><span class="sxs-lookup"><span data-stu-id="9bdc0-115">Description</span></span>                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bdc0-116">\_prise en charge de KSPROPERTY \_</span><span class="sxs-lookup"><span data-stu-id="9bdc0-116">KSPROPERTY\_SUPPORT\_GET</span></span> | <span data-ttu-id="9bdc0-117">Vous pouvez récupérer la propriété en appelant la méthode [**IKsPropertySet :: obtenir**](ikspropertyset-get.md) .</span><span class="sxs-lookup"><span data-stu-id="9bdc0-117">You can retrieve the property by calling the [**IKsPropertySet::Get**](ikspropertyset-get.md) method.</span></span> |
| <span data-ttu-id="9bdc0-118">\_ensemble de support KSPROPERTY \_</span><span class="sxs-lookup"><span data-stu-id="9bdc0-118">KSPROPERTY\_SUPPORT\_SET</span></span> | <span data-ttu-id="9bdc0-119">Vous pouvez modifier la propriété en appelant [**IKsPropertySet :: Set**](ikspropertyset-set.md).</span><span class="sxs-lookup"><span data-stu-id="9bdc0-119">You can change the property by calling [**IKsPropertySet::Set**](ikspropertyset-set.md).</span></span>              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bdc0-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9bdc0-120">Return value</span></span>

<span data-ttu-id="9bdc0-121">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9bdc0-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9bdc0-122">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="9bdc0-122">Possible values include the following.</span></span>



| <span data-ttu-id="9bdc0-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9bdc0-123">Return code</span></span>                                                                                              | <span data-ttu-id="9bdc0-124">Description</span><span class="sxs-lookup"><span data-stu-id="9bdc0-124">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9bdc0-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9bdc0-125"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="9bdc0-126">Le jeu de propriétés et la combinaison d’ID de propriété spécifiés sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9bdc0-126">The specified property set and property ID combination is supported.</span></span><br/> |
| <dl> <span data-ttu-id="9bdc0-127"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="9bdc0-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                | <span data-ttu-id="9bdc0-128">Le jeu de propriétés n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9bdc0-128">Property set is not supported.</span></span><br/>                                       |
| <dl> <span data-ttu-id="9bdc0-129"><dt>**\_ID prop \_ \_ non pris en charge**</dt></span><span class="sxs-lookup"><span data-stu-id="9bdc0-129"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="9bdc0-130">L’ID de propriété n’est pas pris en charge pour le jeu de propriétés spécifié.</span><span class="sxs-lookup"><span data-stu-id="9bdc0-130">Property ID is not supported for the specified property set.</span></span><br/>         |
| <dl> <span data-ttu-id="9bdc0-131"><dt>**jeu d’E \_ props \_ \_ non pris en charge**</dt></span><span class="sxs-lookup"><span data-stu-id="9bdc0-131"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="9bdc0-132">Le jeu de propriétés n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9bdc0-132">Property set is not supported.</span></span><br/>                                       |



 

## <a name="remarks"></a><span data-ttu-id="9bdc0-133">Notes</span><span class="sxs-lookup"><span data-stu-id="9bdc0-133">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9bdc0-134">Une autre interface portant ce nom existe dans le fichier d’en-tête dsound. h.</span><span class="sxs-lookup"><span data-stu-id="9bdc0-134">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="9bdc0-135">Les deux interfaces ne sont pas compatibles.</span><span class="sxs-lookup"><span data-stu-id="9bdc0-135">The two interfaces are not compatible.</span></span> <span data-ttu-id="9bdc0-136">L’interface **IKsControl** , documentée dans le DDK DirectShow, est désormais l’interface recommandée pour passer des jeux de propriétés entre les pilotes WDM et les composants en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9bdc0-136">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="9bdc0-137">Vous devez inclure KS. h avant ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="9bdc0-137">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bdc0-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9bdc0-138">Requirements</span></span>



| <span data-ttu-id="9bdc0-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9bdc0-139">Requirement</span></span> | <span data-ttu-id="9bdc0-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bdc0-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bdc0-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9bdc0-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9bdc0-142">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9bdc0-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                       |
| <span data-ttu-id="9bdc0-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9bdc0-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9bdc0-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9bdc0-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                             |
| <span data-ttu-id="9bdc0-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="9bdc0-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bdc0-146"><dt>KS. h ; </dt> <dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bdc0-146"><dt>Ks.h; </dt> <dt>Ksproxy.h</dt></span></span> </dl> |
| <span data-ttu-id="9bdc0-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9bdc0-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="9bdc0-148"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bdc0-148"><dt>Strmiids.lib</dt></span></span> </dl>                                                          |



## <a name="see-also"></a><span data-ttu-id="9bdc0-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bdc0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bdc0-150">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="9bdc0-150">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="9bdc0-151">**Interface IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="9bdc0-151">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="9bdc0-152">Jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="9bdc0-152">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




