---
title: Méthode IWMDRMLicense GetInclusionList (wmdrmsdk. h)
description: La méthode GetInclusionList récupère la liste d’inclusion entière pour la licence ou la chaîne de licences actuelle.
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- Méthode GetInclusionList format Windows Media
- Méthode GetInclusionList format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode GetInclusionList
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetInclusionList
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f0d2837a4bb84c07214cce3e4fbc3d4d96b9583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523465"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a><span data-ttu-id="38cc4-106">IWMDRMLicense :: GetInclusionList, méthode</span><span class="sxs-lookup"><span data-stu-id="38cc4-106">IWMDRMLicense::GetInclusionList method</span></span>

<span data-ttu-id="38cc4-107">La méthode **GetInclusionList** récupère la liste d’inclusion entière pour la licence ou la chaîne de licences actuelle.</span><span class="sxs-lookup"><span data-stu-id="38cc4-107">The **GetInclusionList** method retrieves the entire inclusion list for the current license or license chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="38cc4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38cc4-108">Syntax</span></span>


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a><span data-ttu-id="38cc4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38cc4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38cc4-110">*ppGuids* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="38cc4-110">*ppGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38cc4-111">Reçoit un tableau de GUID identifiant les technologies incluses.</span><span class="sxs-lookup"><span data-stu-id="38cc4-111">Receives an array of GUIDs identifying the included technologies.</span></span>

</dd> <dt>

<span data-ttu-id="38cc4-112">*pcGuids* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="38cc4-112">*pcGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38cc4-113">Reçoit le nombre d’éléments dans le tableau *ppGuids* .</span><span class="sxs-lookup"><span data-stu-id="38cc4-113">Receives the number of elements in the *ppGuids* array.</span></span> <span data-ttu-id="38cc4-114">Le tableau est alloué à l’aide de **CoTaskMemAlloc**.</span><span class="sxs-lookup"><span data-stu-id="38cc4-114">The array is allocated by using **CoTaskMemAlloc**.</span></span> <span data-ttu-id="38cc4-115">Lorsque vous avez terminé avec la liste, libérez de la mémoire en appelant **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="38cc4-115">When finished with the list, release the memory by calling **CoTaskMemFree**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38cc4-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="38cc4-116">Return value</span></span>

<span data-ttu-id="38cc4-117">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="38cc4-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="38cc4-118">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="38cc4-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="38cc4-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="38cc4-119">Return code</span></span>                                                                          | <span data-ttu-id="38cc4-120">Description</span><span class="sxs-lookup"><span data-stu-id="38cc4-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="38cc4-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="38cc4-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="38cc4-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="38cc4-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="38cc4-123">Notes</span><span class="sxs-lookup"><span data-stu-id="38cc4-123">Remarks</span></span>

<span data-ttu-id="38cc4-124">L’émetteur de licence peut spécifier d’autres systèmes de protection sur lesquels le contenu chiffré peut être converti.</span><span class="sxs-lookup"><span data-stu-id="38cc4-124">The license issuer can specify other protection systems to which the encrypted content may be converted.</span></span> <span data-ttu-id="38cc4-125">La liste des GUID récupérés par cette méthode identifie les systèmes de protection autorisés.</span><span class="sxs-lookup"><span data-stu-id="38cc4-125">The list of GUIDs retrieved by this method identifies the allowed protection systems.</span></span> <span data-ttu-id="38cc4-126">Lorsque vous entrez dans un contrat de licence avec Microsoft pour obtenir la bibliothèque stub, vous recevrez une liste des systèmes de protection actuellement pris en charge et les GUID utilisés pour les identifier.</span><span class="sxs-lookup"><span data-stu-id="38cc4-126">When you enter into a license agreement with Microsoft to get the stub library, you will receive a list of currently supported protection systems and the GUIDs used to identify them.</span></span>

## <a name="requirements"></a><span data-ttu-id="38cc4-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38cc4-127">Requirements</span></span>



| <span data-ttu-id="38cc4-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38cc4-128">Requirement</span></span> | <span data-ttu-id="38cc4-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="38cc4-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38cc4-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="38cc4-130">Header</span></span><br/>  | <dl> <span data-ttu-id="38cc4-131"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="38cc4-131"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="38cc4-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="38cc4-132">Library</span></span><br/> | <dl> <span data-ttu-id="38cc4-133"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38cc4-133"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38cc4-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38cc4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38cc4-135">**Listes d’autorisations et d’inclusion explicites**</span><span class="sxs-lookup"><span data-stu-id="38cc4-135">**Explicit Authorization and Inclusion Lists**</span></span>](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[<span data-ttu-id="38cc4-136">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="38cc4-136">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





