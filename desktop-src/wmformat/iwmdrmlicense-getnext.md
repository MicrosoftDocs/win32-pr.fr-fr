---
title: IWMDRMLicense GetNext, méthode (wmdrmsdk. h)
description: La méthode GetNext charge les informations relatives à l’élément suivant de la liste.
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- Méthode GetNext Windows Media format
- Méthode GetNext Windows Media format, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, GetNext, méthode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetNext
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1dd1f8ce41648c7a67730d909058d10d616e7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528681"
---
# <a name="iwmdrmlicensegetnext-method"></a><span data-ttu-id="91df4-106">IWMDRMLicense :: GetNext, méthode</span><span class="sxs-lookup"><span data-stu-id="91df4-106">IWMDRMLicense::GetNext method</span></span>

<span data-ttu-id="91df4-107">La méthode **GetNext** charge les informations relatives à l’élément suivant de la liste.</span><span class="sxs-lookup"><span data-stu-id="91df4-107">The **GetNext** method loads the information about the next item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="91df4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91df4-108">Syntax</span></span>


```C++
HRESULT GetNext();
```



## <a name="parameters"></a><span data-ttu-id="91df4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91df4-109">Parameters</span></span>

<span data-ttu-id="91df4-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="91df4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91df4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91df4-111">Return value</span></span>

<span data-ttu-id="91df4-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="91df4-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="91df4-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="91df4-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="91df4-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="91df4-114">Return code</span></span>                                                                                                | <span data-ttu-id="91df4-115">Description</span><span class="sxs-lookup"><span data-stu-id="91df4-115">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="91df4-116"><dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt></span><span class="sxs-lookup"><span data-stu-id="91df4-116"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="91df4-117">Une liste de révocation de contenu mise à jour est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="91df4-117">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="91df4-118"><dt>**ERREUR \_ aucun \_ autre \_ élément**</dt></span><span class="sxs-lookup"><span data-stu-id="91df4-118"><dt>**ERROR\_NO\_MORE\_ITEMS**</dt></span></span> </dl>      | <span data-ttu-id="91df4-119">Il n’y a plus d’élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="91df4-119">There are no more items in the list.</span></span><br/>          |
| <dl> <span data-ttu-id="91df4-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="91df4-120"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="91df4-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="91df4-121">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="91df4-122">Notes</span><span class="sxs-lookup"><span data-stu-id="91df4-122">Remarks</span></span>

<span data-ttu-id="91df4-123">Les méthodes de l’interface [**IWMDRMLicense**](iwmdrmlicense.md) fournissent des données sur une licence unique à la fois.</span><span class="sxs-lookup"><span data-stu-id="91df4-123">The methods of the [**IWMDRMLicense**](iwmdrmlicense.md) interface provide data about a single license at a time.</span></span> <span data-ttu-id="91df4-124">L’objet sous-jacent contient une liste d’une ou de plusieurs licences.</span><span class="sxs-lookup"><span data-stu-id="91df4-124">The underlying object contains a list of one or more licenses.</span></span> <span data-ttu-id="91df4-125">Lorsque vous appelez cette méthode, l’interface déplace ses références internes à la licence suivante dans la liste.</span><span class="sxs-lookup"><span data-stu-id="91df4-125">When you call this method, the interface moves its internal references to the next license in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="91df4-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91df4-126">Requirements</span></span>



| <span data-ttu-id="91df4-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91df4-127">Requirement</span></span> | <span data-ttu-id="91df4-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="91df4-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91df4-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="91df4-129">Header</span></span><br/>  | <dl> <span data-ttu-id="91df4-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="91df4-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="91df4-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="91df4-131">Library</span></span><br/> | <dl> <span data-ttu-id="91df4-132"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91df4-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91df4-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91df4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91df4-134">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="91df4-134">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





