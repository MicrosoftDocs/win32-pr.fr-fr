---
description: La méthode Set définit une propriété identifiée par un GUID de jeu de propriétés et un ID de propriété.
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: 'IKsPropertySet :: Set, méthode (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Set
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: b233cea7e131919d94b00afeb5a6e2ea3703c738
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392604"
---
# <a name="ikspropertysetset-method"></a><span data-ttu-id="1ab59-103">IKsPropertySet :: Set, méthode</span><span class="sxs-lookup"><span data-stu-id="1ab59-103">IKsPropertySet::Set method</span></span>

<span data-ttu-id="1ab59-104">La `Set` méthode définit une propriété identifiée par un GUID de jeu de propriétés et un ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="1ab59-104">The `Set` method sets a property identified by a property set GUID and a property ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ab59-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ab59-105">Syntax</span></span>


```C++
HRESULT Set(
  [in] REFGUID guidPropSet,
  [in] DWORD   dwPropID,
  [in] LPVOID  pInstanceData,
  [in] DWORD   cbInstanceData,
  [in] LPVOID  pPropData,
  [in] DWORD   cbPropData
);
```



## <a name="parameters"></a><span data-ttu-id="1ab59-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ab59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ab59-107">*guidPropSet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ab59-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ab59-108">GUID du jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="1ab59-108">Property set GUID.</span></span>

</dd> <dt>

<span data-ttu-id="1ab59-109">*dwPropID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ab59-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ab59-110">Identificateur de la propriété dans le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="1ab59-110">Identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="1ab59-111">*pInstanceData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ab59-111">*pInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ab59-112">Pointeur vers une mémoire tampon qui contient les données d’instance pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="1ab59-112">Pointer to a buffer that contains instance data for the property.</span></span>

</dd> <dt>

<span data-ttu-id="1ab59-113">*cbInstanceData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ab59-113">*cbInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ab59-114">Taille de la mémoire tampon *pInstanceData* , en octets.</span><span class="sxs-lookup"><span data-stu-id="1ab59-114">Size of the *pInstanceData* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1ab59-115">*pPropData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ab59-115">*pPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ab59-116">Pointeur vers une mémoire tampon qui contient la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="1ab59-116">Pointer to a buffer that contains the value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="1ab59-117">*cbPropData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ab59-117">*cbPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ab59-118">Sise de la mémoire tampon *pPropData* , en octets.</span><span class="sxs-lookup"><span data-stu-id="1ab59-118">Sise of the *pPropData* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ab59-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ab59-119">Return value</span></span>

<span data-ttu-id="1ab59-120">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1ab59-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1ab59-121">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="1ab59-121">Possible values include the following.</span></span>



| <span data-ttu-id="1ab59-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1ab59-122">Return code</span></span>                                                                                              | <span data-ttu-id="1ab59-123">Description</span><span class="sxs-lookup"><span data-stu-id="1ab59-123">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1ab59-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1ab59-124"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="1ab59-125">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="1ab59-125">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="1ab59-126"><dt>**jeu d’E \_ props \_ \_ non pris en charge**</dt></span><span class="sxs-lookup"><span data-stu-id="1ab59-126"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="1ab59-127">Le jeu de propriétés n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1ab59-127">The property set is not supported.</span></span><br/>                               |
| <dl> <span data-ttu-id="1ab59-128"><dt>**\_ID prop \_ \_ non pris en charge**</dt></span><span class="sxs-lookup"><span data-stu-id="1ab59-128"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="1ab59-129">L’ID de propriété n’est pas pris en charge pour le jeu de propriétés spécifié.</span><span class="sxs-lookup"><span data-stu-id="1ab59-129">The property ID is not supported for the specified property set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1ab59-130">Notes</span><span class="sxs-lookup"><span data-stu-id="1ab59-130">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1ab59-131">Une autre interface portant ce nom existe dans le fichier d’en-tête dsound. h.</span><span class="sxs-lookup"><span data-stu-id="1ab59-131">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="1ab59-132">Les deux interfaces ne sont pas compatibles.</span><span class="sxs-lookup"><span data-stu-id="1ab59-132">The two interfaces are not compatible.</span></span> <span data-ttu-id="1ab59-133">L’interface **IKsControl** , documentée dans le DDK DirectShow, est désormais l’interface recommandée pour passer des jeux de propriétés entre les pilotes WDM et les composants en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1ab59-133">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="1ab59-134">Vous devez inclure KS. h avant ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="1ab59-134">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ab59-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ab59-135">Requirements</span></span>



| <span data-ttu-id="1ab59-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ab59-136">Requirement</span></span> | <span data-ttu-id="1ab59-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ab59-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab59-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ab59-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1ab59-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ab59-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1ab59-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ab59-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1ab59-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ab59-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1ab59-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ab59-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ab59-143"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ab59-143"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="1ab59-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1ab59-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ab59-145"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ab59-145"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ab59-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ab59-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ab59-147">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="1ab59-147">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="1ab59-148">**Interface IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="1ab59-148">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="1ab59-149">Jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="1ab59-149">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




