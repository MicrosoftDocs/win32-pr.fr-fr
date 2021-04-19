---
title: Méthode IConfigAsfWriter2 GetParam
description: La méthode GetParam récupère la valeur actuelle du paramètre de configuration de filtre spécifié.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- Méthode GetParam format Windows Media
- Méthode GetParam format Windows Media, interface IConfigAsfWriter2
- Interface IConfigAsfWriter2 Windows Media format, méthode GetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d72b8011072424679729686dd5a14c92bae90f66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513731"
---
# <a name="iconfigasfwriter2getparam-method"></a><span data-ttu-id="d5c4e-106">IConfigAsfWriter2 :: GetParam, méthode</span><span class="sxs-lookup"><span data-stu-id="d5c4e-106">IConfigAsfWriter2::GetParam method</span></span>

<span data-ttu-id="d5c4e-107">La méthode **GetParam** récupère la valeur actuelle du paramètre de configuration de filtre spécifié.</span><span class="sxs-lookup"><span data-stu-id="d5c4e-107">The **GetParam** method retrieves the current value of the specified filter configuration parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c4e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5c4e-108">Syntax</span></span>


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a><span data-ttu-id="d5c4e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5c4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c4e-110">*dwParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5c4e-110">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c4e-111">Spécifie le paramètre à récupérer.</span><span class="sxs-lookup"><span data-stu-id="d5c4e-111">Specifies the parameter to retrieve.</span></span> <span data-ttu-id="d5c4e-112">Il doit s’agir d’une valeur définie dans l’énumération [ \_ am \_ ASFWRITERCONFIG \_ param](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d5c4e-112">It must be a value defined in the [\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="d5c4e-113">*pdwParam1* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d5c4e-113">*pdwParam1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c4e-114">Pointeur vers une variable qui récupère la valeur du paramètre spécifié dans *dwParam*.</span><span class="sxs-lookup"><span data-stu-id="d5c4e-114">Pointer to a variable that retrieves the value of the parameter specified in *dwParam*.</span></span>

</dd> <dt>

<span data-ttu-id="d5c4e-115">*pdwParam2* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d5c4e-115">*pdwParam2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c4e-116">Non utilisé, doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="d5c4e-116">Not used, must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5c4e-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5c4e-117">Return value</span></span>

<span data-ttu-id="d5c4e-118">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d5c4e-118">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="d5c4e-119">En cas d’échec, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d5c4e-119">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5c4e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5c4e-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5c4e-121">[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d5c4e-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d5c4e-122">**IConfigAsfWriter2::SetParam**</span><span class="sxs-lookup"><span data-stu-id="d5c4e-122">**IConfigAsfWriter2::SetParam**</span></span>](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 