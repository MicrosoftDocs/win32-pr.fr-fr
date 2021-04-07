---
title: Méthode ITfContextRenderingMarkup GetRenderingMarkup
description: La méthode ITfContextRenderingMarkup GetRenderingMarkup récupère un énumérateur des balises de rendu pour la plage donnée.
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- Infrastructure des services de texte de méthode GetRenderingMarkup
- GetRenderingMarkup méthode Text Services Framework, interface ITfContextRenderingMarkup
- ITfContextRenderingMarkup interface Text Services Framework, méthode GetRenderingMarkup
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f3ccfb97af6a6657c33982359640a2a924cad2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728556"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a><span data-ttu-id="e6266-106">ITfContextRenderingMarkup :: GetRenderingMarkup, méthode</span><span class="sxs-lookup"><span data-stu-id="e6266-106">ITfContextRenderingMarkup::GetRenderingMarkup method</span></span>

<span data-ttu-id="e6266-107">La méthode **ITfContextRenderingMarkup :: GetRenderingMarkup** récupère un énumérateur des balises de rendu pour la plage donnée.</span><span class="sxs-lookup"><span data-stu-id="e6266-107">The **ITfContextRenderingMarkup::GetRenderingMarkup** method retrieves an enumerator of the rendering markups for the given range.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6266-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6266-108">Syntax</span></span>


```C++
HRESULT GetRenderingMarkup(
  [in]  TfEditCookie           ec,
  [in]  DWORD                  dwFlags,
  [in]  ITfRange               *pRangeCover,
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="e6266-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6266-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6266-110">*EC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6266-110">*ec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6266-111">\[dans \] un cookie de modification en lecture seule pour accéder au contexte.</span><span class="sxs-lookup"><span data-stu-id="e6266-111">\[in\] A read only edit cookie to access the context.</span></span>

</dd> <dt>

<span data-ttu-id="e6266-112">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6266-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6266-113">\[in\]</span><span class="sxs-lookup"><span data-stu-id="e6266-113">\[in\]</span></span>



| <span data-ttu-id="e6266-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6266-114">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="e6266-115">Signification</span><span class="sxs-lookup"><span data-stu-id="e6266-115">Meaning</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <span data-ttu-id="e6266-116"><dt>**\_ \_ propriété include GRM TF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e6266-116"><dt>**TF\_GRM\_INCLUDE\_PROPERTY**</dt></span></span> </dl> | <span data-ttu-id="e6266-117">Si ce bit est 1, l’énumérateur inclut la propriété d' \_ attribut prop GUID \_ .</span><span class="sxs-lookup"><span data-stu-id="e6266-117">If this bit is 1, the enumerator will include the GUID\_PROP\_ATTRIBUTE property.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e6266-118">*pRangeCover* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6266-118">*pRangeCover* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6266-119">\[dans \] un pointeur vers une interface [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) de la plage pour énumérer les balises de rendu.</span><span class="sxs-lookup"><span data-stu-id="e6266-119">\[in\] A pointer to an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) interface of the range to enumerate the rendering markups.</span></span>

</dd> <dt>

<span data-ttu-id="e6266-120">*ppEnum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e6266-120">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6266-121">\[\]un pointeur pour récupérer le pointeur d’interface [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .</span><span class="sxs-lookup"><span data-stu-id="e6266-121">\[out\] A pointer to retrieve [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6266-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6266-122">Return value</span></span>

<span data-ttu-id="e6266-123">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="e6266-123">This method can return one of these values.</span></span>



| <span data-ttu-id="e6266-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6266-124">Value</span></span>                                                                                | <span data-ttu-id="e6266-125">Description</span><span class="sxs-lookup"><span data-stu-id="e6266-125">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e6266-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e6266-126"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e6266-127">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="e6266-127">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e6266-128">Notes</span><span class="sxs-lookup"><span data-stu-id="e6266-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e6266-129">Cette méthode n’est pas actuellement dans les fichiers d’en-tête publics.</span><span class="sxs-lookup"><span data-stu-id="e6266-129">This method is not currently in the public header files.</span></span> <span data-ttu-id="e6266-130">Pour utiliser cette API, vous devez effectuer une compilation MIDL du [prototype](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="e6266-130">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

