---
title: Méthode IConfigAsfWriter2 SetParam
description: La méthode SetParam définit la valeur du paramètre de configuration de filtre spécifié.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- Méthode SetParam format Windows Media
- Méthode SetParam format Windows Media, interface IConfigAsfWriter2
- Interface IConfigAsfWriter2 Windows Media format, méthode SetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f123bf11c8297f3a7ce0d4b0047874d8d7b31b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511301"
---
# <a name="iconfigasfwriter2setparam-method"></a><span data-ttu-id="51c71-106">IConfigAsfWriter2 :: SetParam, méthode</span><span class="sxs-lookup"><span data-stu-id="51c71-106">IConfigAsfWriter2::SetParam method</span></span>

<span data-ttu-id="51c71-107">La méthode **setParam** définit la valeur du paramètre de configuration de filtre spécifié.</span><span class="sxs-lookup"><span data-stu-id="51c71-107">The **SetParam** method sets the value of the specified filter configuration parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="51c71-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51c71-108">Syntax</span></span>


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a><span data-ttu-id="51c71-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51c71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51c71-110">*dwParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="51c71-110">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51c71-111">Spécifie le paramètre à définir.</span><span class="sxs-lookup"><span data-stu-id="51c71-111">Specifies the parameter to set.</span></span> <span data-ttu-id="51c71-112">Il doit s’agir d’une valeur définie dans l’énumération [ \_ am \_ ASFWRITERCONFIG \_ param](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="51c71-112">It must be a value defined in the [\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="51c71-113">*dwParam1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="51c71-113">*dwParam1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51c71-114">Spécifie la valeur à assigner au paramètre *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="51c71-114">Specifies the value to assign to the *dwParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="51c71-115">*dwParam2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="51c71-115">*dwParam2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51c71-116">Non utilisé ; doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="51c71-116">Not used; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51c71-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51c71-117">Return value</span></span>

<span data-ttu-id="51c71-118">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="51c71-118">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="51c71-119">En cas d’échec, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="51c71-119">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="51c71-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51c71-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="51c71-121">[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51c71-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="51c71-122">**IConfigAsfWriter2 :: GetParam**</span><span class="sxs-lookup"><span data-stu-id="51c71-122">**IConfigAsfWriter2::GetParam**</span></span>](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 