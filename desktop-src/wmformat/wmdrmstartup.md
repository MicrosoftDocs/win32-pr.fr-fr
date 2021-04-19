---
title: WMDRMStartup, fonction (wmdrmsdk. h)
description: La fonction WMDRMStartup initialise les ressources utilisées par les API étendues du client Windows Media DRM.
ms.assetid: 2fd26bcc-8106-4356-933a-d4cf3536f4fb
keywords:
- WMDRMStartup fonction Windows Media format
topic_type:
- apiref
api_name:
- WMDRMStartup
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c152a5160750f3c1943b455a8877b4615781b6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541658"
---
# <a name="wmdrmstartup-function"></a><span data-ttu-id="f71f4-104">WMDRMStartup fonction)</span><span class="sxs-lookup"><span data-stu-id="f71f4-104">WMDRMStartup function</span></span>

<span data-ttu-id="f71f4-105">La fonction **WMDRMStartup** initialise les ressources utilisées par les API étendues du client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="f71f4-105">The **WMDRMStartup** function initializes resources used by the Windows Media DRM Client Extended APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f71f4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f71f4-106">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMStartup(void);
```



## <a name="parameters"></a><span data-ttu-id="f71f4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f71f4-107">Parameters</span></span>

<span data-ttu-id="f71f4-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="f71f4-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f71f4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f71f4-109">Return value</span></span>

<span data-ttu-id="f71f4-110">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f71f4-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f71f4-111">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f71f4-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f71f4-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f71f4-112">Return code</span></span>                                                                          | <span data-ttu-id="f71f4-113">Description</span><span class="sxs-lookup"><span data-stu-id="f71f4-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f71f4-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f71f4-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f71f4-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="f71f4-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f71f4-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f71f4-116">Remarks</span></span>

<span data-ttu-id="f71f4-117">Pour chaque appel de cette fonction, vous devez appeler [**WMDRMShutdown**](wmdrmshutdown.md) pour libérer les ressources utilisées.</span><span class="sxs-lookup"><span data-stu-id="f71f4-117">For every call of this function, you must call [**WMDRMShutdown**](wmdrmshutdown.md) to release the resources used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f71f4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f71f4-118">Requirements</span></span>



| <span data-ttu-id="f71f4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f71f4-119">Requirement</span></span> | <span data-ttu-id="f71f4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f71f4-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f71f4-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f71f4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f71f4-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f71f4-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="f71f4-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f71f4-123">Library</span></span><br/> | <dl> <span data-ttu-id="f71f4-124"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f71f4-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="f71f4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f71f4-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="f71f4-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f71f4-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f71f4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f71f4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f71f4-128">**Fonctions**</span><span class="sxs-lookup"><span data-stu-id="f71f4-128">**Functions**</span></span>](drm-functions.md)
</dt> </dl>

 

 





