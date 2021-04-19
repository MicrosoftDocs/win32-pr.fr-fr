---
title: Méthode ISoftKbd SetSoftKeyboardTextFont (Softkbdc. h)
description: La méthode ISoftKbd SetSoftKeyboardTextFont définit la police de texte utilisée par un clavier conditionnel.
ms.assetid: 14705723-4592-40ef-9ebb-1c44c10c3cda
keywords:
- Infrastructure des services de texte de méthode SetSoftKeyboardTextFont
- SetSoftKeyboardTextFont méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode SetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff0a9adce61bc1a671d28c6e5d6ac5b6d329b42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511167"
---
# <a name="isoftkbdsetsoftkeyboardtextfont-method"></a><span data-ttu-id="33564-106">ISoftKbd :: SetSoftKeyboardTextFont, méthode</span><span class="sxs-lookup"><span data-stu-id="33564-106">ISoftKbd::SetSoftKeyboardTextFont method</span></span>

<span data-ttu-id="33564-107">La méthode **ISoftKbd :: SetSoftKeyboardTextFont** définit la police de texte utilisée par un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="33564-107">The **ISoftKbd::SetSoftKeyboardTextFont** method sets the text font used by a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="33564-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33564-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardTextFont(
  [in] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a><span data-ttu-id="33564-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33564-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33564-110">*pLogFont* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33564-110">*pLogFont* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33564-111">Pointeur vers une structure [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) définissant la police du texte pour le clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="33564-111">Pointer to a [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure defining the text font for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33564-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33564-112">Return value</span></span>

<span data-ttu-id="33564-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="33564-113">This method can return one of these values.</span></span>



| <span data-ttu-id="33564-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="33564-114">Value</span></span>                                                                                        | <span data-ttu-id="33564-115">Description</span><span class="sxs-lookup"><span data-stu-id="33564-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="33564-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="33564-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="33564-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="33564-117">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="33564-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="33564-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="33564-119">Le paramètre *pLogFont* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="33564-119">The *pLogFont* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="33564-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33564-120">Requirements</span></span>



| <span data-ttu-id="33564-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33564-121">Requirement</span></span> | <span data-ttu-id="33564-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="33564-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33564-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33564-123">Minimum supported client</span></span><br/> | <span data-ttu-id="33564-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33564-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="33564-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33564-125">Minimum supported server</span></span><br/> | <span data-ttu-id="33564-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33564-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="33564-127">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="33564-127">Redistributable</span></span><br/>          | <span data-ttu-id="33564-128">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="33564-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="33564-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="33564-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="33564-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="33564-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="33564-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="33564-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="33564-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="33564-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="33564-133">DLL</span><span class="sxs-lookup"><span data-stu-id="33564-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33564-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33564-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33564-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33564-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33564-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="33564-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="33564-137">**ISoftKbd::GetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="33564-137">**ISoftKbd::GetSoftKeyboardTextFont**</span></span>](isoftkbd-getsoftkeyboardtextfont.md)
</dt> </dl>

 

