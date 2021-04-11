---
title: Méthode ISoftKbd ShowSoftKeyboard (Softkbdc. h)
description: La méthode ISoftKbd ShowSoftKeyboard affiche un clavier conditionnel.
ms.assetid: 7e24bef1-accb-40f6-a549-fb676abf9971
keywords:
- Infrastructure des services de texte de méthode ShowSoftKeyboard
- ShowSoftKeyboard méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode ShowSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.ShowSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b319e7782a19571cf827175566e1af056c34cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032314"
---
# <a name="isoftkbdshowsoftkeyboard-method"></a><span data-ttu-id="3b18c-106">ISoftKbd :: ShowSoftKeyboard, méthode</span><span class="sxs-lookup"><span data-stu-id="3b18c-106">ISoftKbd::ShowSoftKeyboard method</span></span>

<span data-ttu-id="3b18c-107">La méthode **ISoftKbd :: ShowSoftKeyboard** affiche un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="3b18c-107">The **ISoftKbd::ShowSoftKeyboard** method displays a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b18c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b18c-108">Syntax</span></span>


```C++
HRESULT ShowSoftKeyboard(
  [in] INT iShow
);
```



## <a name="parameters"></a><span data-ttu-id="3b18c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b18c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b18c-110">*iShow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b18c-110">*iShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b18c-111">Entier indiquant le type de clavier logiciel à afficher.</span><span class="sxs-lookup"><span data-stu-id="3b18c-111">Integer indicating the type of soft keyboard to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b18c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b18c-112">Return value</span></span>

<span data-ttu-id="3b18c-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="3b18c-113">This method can return one of these values.</span></span>



| <span data-ttu-id="3b18c-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b18c-114">Value</span></span>                                                                                | <span data-ttu-id="3b18c-115">Description</span><span class="sxs-lookup"><span data-stu-id="3b18c-115">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="3b18c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3b18c-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3b18c-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="3b18c-117">The method was successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3b18c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b18c-118">Requirements</span></span>



| <span data-ttu-id="3b18c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b18c-119">Requirement</span></span> | <span data-ttu-id="3b18c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b18c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b18c-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b18c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3b18c-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b18c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3b18c-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b18c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3b18c-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b18c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3b18c-125">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="3b18c-125">Redistributable</span></span><br/>          | <span data-ttu-id="3b18c-126">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="3b18c-126">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="3b18c-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b18c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b18c-128"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b18c-128"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="3b18c-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="3b18c-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b18c-130"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b18c-130"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="3b18c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3b18c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b18c-132"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b18c-132"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b18c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b18c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b18c-134">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="3b18c-134">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





