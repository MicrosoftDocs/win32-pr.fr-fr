---
title: WMDRMShutdown, fonction (wmdrmsdk. h)
description: La fonction WMDRMShutdown libère les ressources utilisées par les API étendues du client Windows Media DRM.
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- WMDRMShutdown fonction Windows Media format
topic_type:
- apiref
api_name:
- WMDRMShutdown
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb49049a593699a4071eefea9c5cf7c61571fc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537332"
---
# <a name="wmdrmshutdown-function"></a><span data-ttu-id="d26e7-104">WMDRMShutdown fonction)</span><span class="sxs-lookup"><span data-stu-id="d26e7-104">WMDRMShutdown function</span></span>

<span data-ttu-id="d26e7-105">La fonction **WMDRMShutdown** libère les ressources utilisées par les API étendues du client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="d26e7-105">The **WMDRMShutdown** function releases resources used by the Windows Media DRM Client Extended APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="d26e7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d26e7-106">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a><span data-ttu-id="d26e7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d26e7-107">Parameters</span></span>

<span data-ttu-id="d26e7-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d26e7-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d26e7-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d26e7-109">Return value</span></span>

<span data-ttu-id="d26e7-110">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d26e7-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d26e7-111">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d26e7-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d26e7-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d26e7-112">Return code</span></span>                                                                          | <span data-ttu-id="d26e7-113">Description</span><span class="sxs-lookup"><span data-stu-id="d26e7-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d26e7-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d26e7-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d26e7-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="d26e7-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d26e7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d26e7-116">Remarks</span></span>

<span data-ttu-id="d26e7-117">Pour éviter les fuites de mémoire, vous devez appeler cette fonction pour chaque appel de la fonction [**WMDRMStartup**](wmdrmstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="d26e7-117">To avoid memory leaks, you must call this function for every call of the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d26e7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d26e7-118">Requirements</span></span>



| <span data-ttu-id="d26e7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d26e7-119">Requirement</span></span> | <span data-ttu-id="d26e7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d26e7-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d26e7-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="d26e7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d26e7-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d26e7-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="d26e7-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d26e7-123">Library</span></span><br/> | <dl> <span data-ttu-id="d26e7-124"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d26e7-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="d26e7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d26e7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="d26e7-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d26e7-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d26e7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d26e7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d26e7-128">**Fonctions**</span><span class="sxs-lookup"><span data-stu-id="d26e7-128">**Functions**</span></span>](drm-functions.md)
</dt> </dl>

 

 





