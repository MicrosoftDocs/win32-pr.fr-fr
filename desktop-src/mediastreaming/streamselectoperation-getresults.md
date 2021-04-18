---
title: StreamSelectOperation. GetResults, méthode
description: Retourne les résultats de l’opération asynchrone démarrée par SelectBestStreamAsync.
ms.assetid: 2D9887E7-17C8-4161-984F-FA44591D2052
keywords:
- Méthode GetResults API de diffusion multimédia en continu
- Méthode GetResults API de diffusion multimédia en continu, interface StreamSelectOperation
- API de diffusion multimédia en continu de l’interface StreamSelectOperation, méthode GetResults
topic_type:
- apiref
api_name:
- StreamSelectOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c52479949413d32ca54654f355a06a2dee70866e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512497"
---
# <a name="streamselectoperationgetresults-method"></a><span data-ttu-id="9522a-106">StreamSelectOperation. GetResults, méthode</span><span class="sxs-lookup"><span data-stu-id="9522a-106">StreamSelectOperation.GetResults method</span></span>

<span data-ttu-id="9522a-107">Retourne les résultats de l’opération asynchrone démarrée par [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9522a-107">Returns the results of the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span>

## <a name="syntax"></a><span data-ttu-id="9522a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9522a-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="9522a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9522a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9522a-110">*valeur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9522a-110">*value* \[out, retval\]</span></span>
<span data-ttu-id="9522a-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9522a-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="9522a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9522a-112">Return value</span></span>

<span data-ttu-id="9522a-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9522a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9522a-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9522a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9522a-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9522a-115">Return code</span></span>                                                                          | <span data-ttu-id="9522a-116">Description</span><span class="sxs-lookup"><span data-stu-id="9522a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9522a-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9522a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9522a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="9522a-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="9522a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9522a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9522a-120">**StreamSelectOperation**</span><span class="sxs-lookup"><span data-stu-id="9522a-120">**StreamSelectOperation**</span></span>](streamselectoperation.md)
</dt> </dl>

 

