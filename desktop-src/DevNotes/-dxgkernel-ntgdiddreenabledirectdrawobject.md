---
description: Réactive un objet périphérique en mode noyau Microsoft DirectDraw après un changement de mode.
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: NtGdiDdReenableDirectDrawObject, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReenableDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: afd736317ecdf802cb418e81063b622db43f0651
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111167"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a><span data-ttu-id="62af0-103">NtGdiDdReenableDirectDrawObject fonction)</span><span class="sxs-lookup"><span data-stu-id="62af0-103">NtGdiDdReenableDirectDrawObject function</span></span>

<span data-ttu-id="62af0-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="62af0-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="62af0-105">Utilisez à la place DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="62af0-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="62af0-106">Réactive un objet périphérique en mode noyau Microsoft DirectDraw après un changement de mode.</span><span class="sxs-lookup"><span data-stu-id="62af0-106">Re-enables a Microsoft DirectDraw kernel-mode device object after a mode switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="62af0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62af0-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a><span data-ttu-id="62af0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62af0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62af0-109">*hDirectDrawLocal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62af0-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62af0-110">Objet DirectDraw qui doit être réactivé.</span><span class="sxs-lookup"><span data-stu-id="62af0-110">DirectDraw object that needs to be re-enabled.</span></span>

</dd> <dt>

<span data-ttu-id="62af0-111">*pubNewMode* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="62af0-111">*pubNewMode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="62af0-112">Pointeur vers une valeur BOOLÉENNE qui sera remplie avec une valeur qui indique si le mode d’affichage a changé.</span><span class="sxs-lookup"><span data-stu-id="62af0-112">Pointer to a BOOL that will be filled with a value that represents whether the display mode changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62af0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62af0-113">Return value</span></span>

<span data-ttu-id="62af0-114">En cas de réussite (l’appareil peut être réactivé), cette fonction retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="62af0-114">If successful (the device can be re-enabled), this function returns **TRUE**.</span></span> <span data-ttu-id="62af0-115">Sinon (par exemple, le pilote d’affichage a été modifié), la **valeur false** est retournée.</span><span class="sxs-lookup"><span data-stu-id="62af0-115">Otherwise (for example, the display driver was changed), it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="62af0-116">Notes</span><span class="sxs-lookup"><span data-stu-id="62af0-116">Remarks</span></span>

<span data-ttu-id="62af0-117">Une fois l’objet réactivé, les fonctionnalités de l’appareil peuvent être interrogées à nouveau via un appel à [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).</span><span class="sxs-lookup"><span data-stu-id="62af0-117">Once the object has been re-enabled, the capabilities for the device can be re-queried via a call to [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).</span></span>

<span data-ttu-id="62af0-118">Il est recommandé aux applications d’utiliser les API DirectDraw ou [Direct3D](../direct3d10/d3d10-graphics-reference.md) version 8, qui automatisent et résument ce processus de manière indépendante du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="62af0-118">Applications are advised to use the DirectDraw or [Direct3D](../direct3d10/d3d10-graphics-reference.md) version 8 APIs, which automate and abstract this process in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="62af0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62af0-119">Requirements</span></span>



| <span data-ttu-id="62af0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62af0-120">Requirement</span></span> | <span data-ttu-id="62af0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="62af0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62af0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62af0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="62af0-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62af0-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="62af0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62af0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="62af0-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62af0-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="62af0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="62af0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="62af0-127"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="62af0-127"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62af0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62af0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62af0-129">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="62af0-129">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="62af0-130">**DdReenableDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="62af0-130">**DdReenableDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
