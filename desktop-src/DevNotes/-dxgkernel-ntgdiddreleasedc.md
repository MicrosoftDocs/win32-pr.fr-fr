---
description: Libère le contexte de périphérique (DC) créé précédemment pour l’objet surface Microsoft DirectDraw en mode noyau indiqué.
ms.assetid: 98def2a1-878d-4776-a519-32cb70107338
title: NtGdiDdReleaseDC, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReleaseDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a7319b423f12d7e4415d78d995bfb1d7cd0341a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847033"
---
# <a name="ntgdiddreleasedc-function"></a><span data-ttu-id="dca7e-103">NtGdiDdReleaseDC fonction)</span><span class="sxs-lookup"><span data-stu-id="dca7e-103">NtGdiDdReleaseDC function</span></span>

<span data-ttu-id="dca7e-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dca7e-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="dca7e-105">Utilisez à la place DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="dca7e-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="dca7e-106">Libère le contexte de périphérique (DC) créé précédemment pour l’objet surface Microsoft DirectDraw en mode noyau indiqué.</span><span class="sxs-lookup"><span data-stu-id="dca7e-106">Releases the previously created device context (DC) for the indicated kernel-mode Microsoft DirectDraw surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dca7e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dca7e-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdReleaseDC(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="dca7e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dca7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dca7e-109">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dca7e-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dca7e-110">Handle vers l’objet de surface DirectDraw en mode noyau précédemment créé.</span><span class="sxs-lookup"><span data-stu-id="dca7e-110">Handle to the previously created kernel-mode DirectDraw surface object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dca7e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dca7e-111">Return value</span></span>

<span data-ttu-id="dca7e-112">En cas de réussite, cette fonction retourne la **valeur true**; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="dca7e-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dca7e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="dca7e-113">Remarks</span></span>

<span data-ttu-id="dca7e-114">Les applications qui doivent obtenir un contrôleur de réseau pour une surface DirectDraw peuvent utiliser [IDirectDrawSurface7 :: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), qui expose cette fonctionnalité de façon indépendante du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dca7e-114">Applications that need to obtain a DC for a DirectDraw surface may use [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), which exposes this functionality in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="dca7e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dca7e-115">Requirements</span></span>



| <span data-ttu-id="dca7e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dca7e-116">Requirement</span></span> | <span data-ttu-id="dca7e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="dca7e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dca7e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dca7e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dca7e-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dca7e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="dca7e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dca7e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dca7e-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dca7e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dca7e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="dca7e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dca7e-123"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dca7e-123"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dca7e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dca7e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dca7e-125">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="dca7e-125">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="dca7e-126">**DdReleaseDC**</span><span class="sxs-lookup"><span data-stu-id="dca7e-126">**DdReleaseDC**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
