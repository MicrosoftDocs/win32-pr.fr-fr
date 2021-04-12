---
title: Méthode ISoftKbd GetSoftKeyboardTextFont (Softkbdc. h)
description: La méthode ISoftKbd GetSoftKeyboardTextFont récupère la police de texte utilisée par un clavier conditionnel.
ms.assetid: 73239359-70b4-47d6-abc5-9fee279ed3a6
keywords:
- Infrastructure des services de texte de méthode GetSoftKeyboardTextFont
- GetSoftKeyboardTextFont méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode GetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce939347042415a9060459102cd8a56665ac2de0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105250"
---
# <a name="isoftkbdgetsoftkeyboardtextfont-method"></a><span data-ttu-id="9f70b-106">ISoftKbd :: GetSoftKeyboardTextFont, méthode</span><span class="sxs-lookup"><span data-stu-id="9f70b-106">ISoftKbd::GetSoftKeyboardTextFont method</span></span>

<span data-ttu-id="9f70b-107">La méthode **ISoftKbd :: GetSoftKeyboardTextFont** récupère la police de texte utilisée par un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="9f70b-107">The **ISoftKbd::GetSoftKeyboardTextFont** method retrieves the text font used by a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f70b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f70b-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardTextFont(
  [out] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a><span data-ttu-id="9f70b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f70b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f70b-110">*pLogFont* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9f70b-110">*pLogFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f70b-111">Pointeur vers une mémoire tampon dans laquelle cette méthode récupère une structure [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) définissant la police du texte pour le clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="9f70b-111">Pointer to a buffer in which this method retrieves a [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure defining the text font for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f70b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f70b-112">Return value</span></span>

<span data-ttu-id="9f70b-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="9f70b-113">This method can return one of these values.</span></span>



| <span data-ttu-id="9f70b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f70b-114">Value</span></span>                                                                                        | <span data-ttu-id="9f70b-115">Description</span><span class="sxs-lookup"><span data-stu-id="9f70b-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="9f70b-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9f70b-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9f70b-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="9f70b-117">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="9f70b-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9f70b-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9f70b-119">Le paramètre *pLogFont* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9f70b-119">The *pLogFont* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9f70b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f70b-120">Requirements</span></span>



| <span data-ttu-id="9f70b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f70b-121">Requirement</span></span> | <span data-ttu-id="9f70b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f70b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f70b-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f70b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9f70b-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f70b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9f70b-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f70b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9f70b-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f70b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9f70b-127">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="9f70b-127">Redistributable</span></span><br/>          | <span data-ttu-id="9f70b-128">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="9f70b-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="9f70b-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f70b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f70b-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f70b-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="9f70b-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="9f70b-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f70b-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f70b-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="9f70b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9f70b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f70b-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f70b-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f70b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f70b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f70b-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="9f70b-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="9f70b-137">**ISoftKbd::SetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="9f70b-137">**ISoftKbd::SetSoftKeyboardTextFont**</span></span>](isoftkbd-setsoftkeyboardtextfont.md)
</dt> </dl>

 

