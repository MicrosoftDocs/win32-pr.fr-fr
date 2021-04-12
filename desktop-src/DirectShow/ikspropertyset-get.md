---
description: La méthode obtenir récupère une propriété identifiée par un GUID de jeu de propriétés et un ID de propriété.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: 'IKsPropertySet :: méthode d’extraction (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Get
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 9c4461e8c5886d84bcf3b7faa6675b749bc0c37d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481761"
---
# <a name="ikspropertysetget-method"></a><span data-ttu-id="182d1-103">IKsPropertySet :: méthode d’extraction</span><span class="sxs-lookup"><span data-stu-id="182d1-103">IKsPropertySet::Get method</span></span>

<span data-ttu-id="182d1-104">La méthode **obtenir** récupère une propriété identifiée par un GUID de jeu de propriétés et un ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="182d1-104">The **Get** method retrieves a property identified by a property set GUID and a property ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="182d1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="182d1-105">Syntax</span></span>


```C++
HRESULT Get(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [in]  LPVOID  pInstanceData,
  [in]  DWORD   cbInstanceData,
  [out] LPVOID  pPropData,
  [in]  DWORD   cbPropData,
  [out] DWORD   *pcbReturned
);
```



## <a name="parameters"></a><span data-ttu-id="182d1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="182d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="182d1-107">*guidPropSet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="182d1-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182d1-108">GUID de la propriété définie.</span><span class="sxs-lookup"><span data-stu-id="182d1-108">The GUID of the property set .</span></span>

</dd> <dt>

<span data-ttu-id="182d1-109">*dwPropID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="182d1-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182d1-110">Identificateur de la propriété dans la propriété définie.</span><span class="sxs-lookup"><span data-stu-id="182d1-110">The identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="182d1-111">*pInstanceData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="182d1-111">*pInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182d1-112">Pointeur vers un tableau d’octets qui contient les données d’instance de la propriété.</span><span class="sxs-lookup"><span data-stu-id="182d1-112">A pointer to an array of bytes that contains instance data for the property.</span></span>

</dd> <dt>

<span data-ttu-id="182d1-113">*cbInstanceData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="182d1-113">*cbInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182d1-114">Taille du tableau donnée dans *pInstanceData*, en octets.</span><span class="sxs-lookup"><span data-stu-id="182d1-114">The size of the array given in *pInstanceData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="182d1-115">*pPropData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="182d1-115">*pPropData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="182d1-116">Pointeur vers un tableau d’octets qui reçoit les données de propriété.</span><span class="sxs-lookup"><span data-stu-id="182d1-116">A pointer to an array of bytes that receives the property data.</span></span>

</dd> <dt>

<span data-ttu-id="182d1-117">*cbPropData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="182d1-117">*cbPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182d1-118">Taille du tableau donnée dans *pPropData*, en octets.</span><span class="sxs-lookup"><span data-stu-id="182d1-118">The size of the array given in *pPropData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="182d1-119">*pcbReturned* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="182d1-119">*pcbReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="182d1-120">Reçoit le nombre d’octets que la méthode copie dans le tableau *pPropData* .</span><span class="sxs-lookup"><span data-stu-id="182d1-120">Receives the number of bytes the method copies to the *pPropData* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="182d1-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="182d1-121">Return value</span></span>

<span data-ttu-id="182d1-122">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="182d1-122">Returns an **HRESULT** value.</span></span> <span data-ttu-id="182d1-123">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="182d1-123">Possible values include the following.</span></span>



| <span data-ttu-id="182d1-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="182d1-124">Return code</span></span>                                                                                              | <span data-ttu-id="182d1-125">Description</span><span class="sxs-lookup"><span data-stu-id="182d1-125">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="182d1-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="182d1-126"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="182d1-127">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="182d1-127">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="182d1-128"><dt>**jeu d’E \_ props \_ \_ non pris en charge**</dt></span><span class="sxs-lookup"><span data-stu-id="182d1-128"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="182d1-129">Le jeu de propriétés n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="182d1-129">The property set is not supported.</span></span><br/>                               |
| <dl> <span data-ttu-id="182d1-130"><dt>**\_ID prop \_ \_ non pris en charge**</dt></span><span class="sxs-lookup"><span data-stu-id="182d1-130"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="182d1-131">L’ID de propriété n’est pas pris en charge pour le jeu de propriétés spécifié.</span><span class="sxs-lookup"><span data-stu-id="182d1-131">The property ID is not supported for the specified property set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="182d1-132">Notes</span><span class="sxs-lookup"><span data-stu-id="182d1-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="182d1-133">Une autre interface portant ce nom existe dans le fichier d’en-tête dsound. h.</span><span class="sxs-lookup"><span data-stu-id="182d1-133">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="182d1-134">Les deux interfaces ne sont pas compatibles.</span><span class="sxs-lookup"><span data-stu-id="182d1-134">The two interfaces are not compatible.</span></span> <span data-ttu-id="182d1-135">L’interface [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) , documentée dans le DDK DirectShow, est désormais l’interface recommandée pour passer des jeux de propriétés entre les pilotes WDM et les composants en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="182d1-135">The [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="182d1-136">Pour récupérer une propriété, allouez une mémoire tampon dans laquelle cette méthode sera remplie.</span><span class="sxs-lookup"><span data-stu-id="182d1-136">To retrieve a property, allocate a buffer which this method will then fill in.</span></span> <span data-ttu-id="182d1-137">Pour déterminer la taille de mémoire tampon nécessaire, spécifiez **null** pour *pPropData* et zéro (0) pour *cbPropData*.</span><span class="sxs-lookup"><span data-stu-id="182d1-137">To determine the necessary buffer size, specify **NULL** for *pPropData* and zero (0) for *cbPropData*.</span></span> <span data-ttu-id="182d1-138">Cette méthode retourne la taille de mémoire tampon nécessaire dans *pcbReturned*.</span><span class="sxs-lookup"><span data-stu-id="182d1-138">This method returns the necessary buffer size in *pcbReturned*.</span></span>

<span data-ttu-id="182d1-139">Vous devez inclure KS. h avant ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="182d1-139">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="examples"></a><span data-ttu-id="182d1-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="182d1-140">Examples</span></span>

<span data-ttu-id="182d1-141">L’exemple suivant interroge un code confidentiel pour sa catégorie de code confidentiel, en extrayant la propriété de **\_ \_ catégorie de code confidentiel AMPROPERTY** .</span><span class="sxs-lookup"><span data-stu-id="182d1-141">The following example queries a pin for its pin category, by retrieving the **AMPROPERTY\_PIN\_CATEGORY** property.</span></span> <span data-ttu-id="182d1-142">(Consultez [pin Property Set](pin-property-set.md).)</span><span class="sxs-lookup"><span data-stu-id="182d1-142">(See [Pin Property Set](pin-property-set.md).)</span></span>


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="182d1-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="182d1-143">Requirements</span></span>



| <span data-ttu-id="182d1-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="182d1-144">Requirement</span></span> | <span data-ttu-id="182d1-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="182d1-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="182d1-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="182d1-146">Minimum supported client</span></span><br/> | <span data-ttu-id="182d1-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="182d1-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="182d1-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="182d1-148">Minimum supported server</span></span><br/> | <span data-ttu-id="182d1-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="182d1-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="182d1-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="182d1-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="182d1-151"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="182d1-151"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="182d1-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="182d1-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="182d1-153"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="182d1-153"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="182d1-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="182d1-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="182d1-155">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="182d1-155">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="182d1-156">**Interface IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="182d1-156">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="182d1-157">Jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="182d1-157">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 
