---
title: Méthode ISoftKbd EnumSoftKeyboard (Softkbdc. h)
description: La méthode ISoftKbd EnumSoftKeyboard énumère les claviers logiciels possibles qui prennent en charge le langage spécifié.
ms.assetid: c71f99e5-c4c2-4b09-a58f-d3f4348d0c5d
keywords:
- Infrastructure des services de texte de méthode EnumSoftKeyboard
- EnumSoftKeyboard méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode EnumSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.EnumSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecdb083684163798a68674628a8b1abc2460268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466163"
---
# <a name="isoftkbdenumsoftkeyboard-method"></a><span data-ttu-id="a5623-106">ISoftKbd :: EnumSoftKeyboard, méthode</span><span class="sxs-lookup"><span data-stu-id="a5623-106">ISoftKbd::EnumSoftKeyboard method</span></span>

<span data-ttu-id="a5623-107">La méthode **ISoftKbd :: EnumSoftKeyboard** énumère les claviers logiciels possibles qui prennent en charge le langage spécifié.</span><span class="sxs-lookup"><span data-stu-id="a5623-107">The **ISoftKbd::EnumSoftKeyboard** method enumerates the possible soft keyboards that support the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5623-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5623-108">Syntax</span></span>


```C++
HRESULT EnumSoftKeyboard(
  [in]  LANGID langid,
  [out] DWORD  *lpdwKeyboard
);
```



## <a name="parameters"></a><span data-ttu-id="a5623-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5623-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5623-110">*LangID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a5623-110">*langid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5623-111">Identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="a5623-111">Language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a5623-112">*lpdwKeyboard* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a5623-112">*lpdwKeyboard* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5623-113">Pointeur vers une mémoire tampon dans laquelle cette méthode récupère les identificateurs des claviers logiciels disponibles.</span><span class="sxs-lookup"><span data-stu-id="a5623-113">Pointer to a buffer in which this method retrieves identifiers of the available soft keyboards.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5623-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5623-114">Return value</span></span>

<span data-ttu-id="a5623-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a5623-115">This method can return one of these values.</span></span>



| <span data-ttu-id="a5623-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5623-116">Value</span></span>                                                                                        | <span data-ttu-id="a5623-117">Description</span><span class="sxs-lookup"><span data-stu-id="a5623-117">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="a5623-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a5623-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a5623-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a5623-119">The method was successful.</span></span><br/>         |
| <dl> <span data-ttu-id="a5623-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a5623-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a5623-121">Le paramètre *LangID* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a5623-121">The *langid* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a5623-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5623-122">Requirements</span></span>



| <span data-ttu-id="a5623-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5623-123">Requirement</span></span> | <span data-ttu-id="a5623-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5623-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5623-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5623-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a5623-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5623-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a5623-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5623-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a5623-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5623-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a5623-129">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a5623-129">Redistributable</span></span><br/>          | <span data-ttu-id="a5623-130">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="a5623-130">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="a5623-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5623-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5623-132"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5623-132"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="a5623-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="a5623-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a5623-134"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a5623-134"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="a5623-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a5623-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5623-136"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5623-136"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5623-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5623-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5623-138">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="a5623-138">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





