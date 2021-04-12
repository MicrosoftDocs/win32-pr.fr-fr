---
title: GetStreamPropertiesOperation. GetResults, méthode
description: Retourne les résultats de l’opération asynchrone démarrée par GetStreamPropertiesAsync.
ms.assetid: D09DCDF5-2B9E-4E03-908B-AEEC7DC228C1
keywords:
- Méthode GetResults API de diffusion multimédia en continu
- Méthode GetResults API de diffusion multimédia en continu, interface GetStreamPropertiesOperation
- API de diffusion multimédia en continu de l’interface GetStreamPropertiesOperation, méthode GetResults
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 312703c28f5cdbb888b46d6ccd312dd358aa6b6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381874"
---
# <a name="getstreampropertiesoperationgetresults-method"></a><span data-ttu-id="93901-106">GetStreamPropertiesOperation. GetResults, méthode</span><span class="sxs-lookup"><span data-stu-id="93901-106">GetStreamPropertiesOperation.GetResults method</span></span>

<span data-ttu-id="93901-107">Retourne les résultats de l’opération asynchrone démarrée par [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93901-107">Returns the results of the asynchronous operation started by [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span>

## <a name="syntax"></a><span data-ttu-id="93901-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93901-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="93901-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93901-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93901-110">*valeur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="93901-110">*value* \[out, retval\]</span></span>
<span data-ttu-id="93901-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="93901-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="93901-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="93901-112">Return value</span></span>

<span data-ttu-id="93901-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="93901-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="93901-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="93901-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="93901-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="93901-115">Return code</span></span>                                                                          | <span data-ttu-id="93901-116">Description</span><span class="sxs-lookup"><span data-stu-id="93901-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="93901-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="93901-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="93901-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="93901-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="93901-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93901-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93901-120">**GetStreamPropertiesOperation**</span><span class="sxs-lookup"><span data-stu-id="93901-120">**GetStreamPropertiesOperation**</span></span>](getstreampropertiesoperation.md)
</dt> </dl>

 

