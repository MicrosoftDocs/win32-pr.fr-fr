---
description: Utilisé pour permettre au mode utilisateur de mieux comprendre la zone de découpage pour Windows sur le bureau. Ce découpage peut changer de façon asynchrone du point de vue des threads en mode utilisateur.
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: NtGdiDdResetVisrgn, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdResetVisrgn
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dd83bcfd6c1f3dec31fb80cf78750bfdfef5e7a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847029"
---
# <a name="ntgdiddresetvisrgn-function"></a><span data-ttu-id="dac91-104">NtGdiDdResetVisrgn fonction)</span><span class="sxs-lookup"><span data-stu-id="dac91-104">NtGdiDdResetVisrgn function</span></span>

<span data-ttu-id="dac91-105">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dac91-105">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="dac91-106">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="dac91-106">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="dac91-107">Utilisé pour permettre au mode utilisateur de mieux comprendre la zone de découpage pour Windows sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="dac91-107">Used to enable the user mode to gain a valid understanding of the clipping region for windows on the desktop.</span></span> <span data-ttu-id="dac91-108">Ce découpage peut changer de façon asynchrone du point de vue des threads en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dac91-108">This clipping can change asynchronously from the point of view of user-mode threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="dac91-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dac91-109">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="dac91-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dac91-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dac91-111">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dac91-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dac91-112">Pointeur vers l’objet en mode utilisateur de toute surface appartenant au périphérique DirectDraw pour lequel le découpage doit être réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="dac91-112">Pointer to the user-mode object of any surface belonging to the DirectDraw device for which clipping is to be reset.</span></span> <span data-ttu-id="dac91-113">Pour plus d’informations, consultez la documentation du DDK.</span><span class="sxs-lookup"><span data-stu-id="dac91-113">For details, see the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="dac91-114">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dac91-114">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dac91-115">Réservé.</span><span class="sxs-lookup"><span data-stu-id="dac91-115">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dac91-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dac91-116">Return value</span></span>

<span data-ttu-id="dac91-117">En cas de réussite, cette fonction retourne la **valeur true**; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="dac91-117">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dac91-118">Notes</span><span class="sxs-lookup"><span data-stu-id="dac91-118">Remarks</span></span>

<span data-ttu-id="dac91-119">Le découpage peut changer de façon asynchrone du point de vue des threads en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dac91-119">Clipping can change asynchronously from the point of view of user-mode threads.</span></span> <span data-ttu-id="dac91-120">Les parties en mode noyau de DirectDraw et de Windows Graphics Device Interface (GDI) maintiennent un compteur qui est incrémenté chaque fois que la liste de découpage de l’ensemble du bureau change.</span><span class="sxs-lookup"><span data-stu-id="dac91-120">The kernel-mode parts of DirectDraw and Windows Graphics Device Interface (GDI) maintain a counter that is incremented whenever the clipping list for the entire desktop changes.</span></span> <span data-ttu-id="dac91-121">Un appel à cette fonction enregistre ce compteur avec chaque surface principale DirectDraw existante sur le système.</span><span class="sxs-lookup"><span data-stu-id="dac91-121">A call to this function records this counter with every existing DirectDraw primary surface on the system.</span></span>

<span data-ttu-id="dac91-122">À un moment ultérieur, lorsque l’une de ces surfaces principales est modifiée par une opération [IDirectDrawSurface7 :: BLT](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) ou [IDirectDrawSurface7 :: Lock](/previous-versions/ms858221(v=msdn.10)) (voir la documentation du DDK), le compteur enregistré avec la surface est comparé au compteur global.</span><span class="sxs-lookup"><span data-stu-id="dac91-122">At any later time when one of these primary surfaces is modified by a [IDirectDrawSurface7::Blt](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) or [IDirectDrawSurface7::Lock](/previous-versions/ms858221(v=msdn.10)) operation (see DDK documentation), then the counter recorded with the surface is compared with the global counter.</span></span> <span data-ttu-id="dac91-123">Si ces valeurs sont différentes, un code d’erreur DDERR \_ VISRGNCHANGED est renvoyé au code du mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dac91-123">If these values are different, an error code DDERR\_VISRGNCHANGED is returned to the user-mode code.</span></span> <span data-ttu-id="dac91-124">Le code en mode utilisateur réinterroge ensuite le découpage actuel du bureau, appelle **NtGdiDdResetVisrgn** et réessaye le IDirectDrawSurface7 :: BLT appliqué à la surface principale, en respectant le nouveau découpage.</span><span class="sxs-lookup"><span data-stu-id="dac91-124">The user-mode code will then re-query the current clipping for the desktop, call **NtGdiDdResetVisrgn**, and re-try the IDirectDrawSurface7::Blt applied to the primary surface, respecting the new clipping.</span></span> <span data-ttu-id="dac91-125">Finalement, le découpage échantillonné par le code en mode utilisateur sera le même que le découpage actuel possédé par le mode noyau, et IDirectDrawSurface7 :: BLT sera autorisé à continuer.</span><span class="sxs-lookup"><span data-stu-id="dac91-125">Eventually, the clipping that was sampled by the user-mode code will be the same as the current clipping owned by kernel mode, and the IDirectDrawSurface7::Blt will be allowed to continue.</span></span>

<span data-ttu-id="dac91-126">Il est conseillé aux applications d’utiliser l’interface [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) ou [IDirect3DDevice8 ::P](/previous-versions/ms889707(v=msdn.10)) méthode renouvely pour gérer les modifications de découpage asynchrones.</span><span class="sxs-lookup"><span data-stu-id="dac91-126">Applications are advised to use the [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) interface or [IDirect3DDevice8::Present](/previous-versions/ms889707(v=msdn.10)) method to handle asynchronous clipping changes.</span></span> <span data-ttu-id="dac91-127">Ces constructions implémentent le découpage asynchrone selon une méthode automatisée et indépendante du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dac91-127">These constructs implement asynchronous clipping in an automated and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="dac91-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dac91-128">Requirements</span></span>



| <span data-ttu-id="dac91-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dac91-129">Requirement</span></span> | <span data-ttu-id="dac91-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="dac91-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dac91-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dac91-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dac91-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dac91-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="dac91-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dac91-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dac91-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dac91-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dac91-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="dac91-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dac91-136"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dac91-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dac91-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dac91-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac91-138">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="dac91-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="dac91-139">**DdResetVisrgn**</span><span class="sxs-lookup"><span data-stu-id="dac91-139">**DdResetVisrgn**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
