---
description: Indique au pilote le blocs macros à afficher en spécifiant les surfaces contenant les blocs macros, les décalages dans chaque surface où le blocs macros existe et la taille des données bloc macro à restituer.
ms.assetid: c49d9dfa-a3db-4572-a474-72c7d4e80940
title: NtGdiDdRenderMoComp, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdRenderMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 6e1dd0942a6996264e02531f7e21b2a99f059143
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847030"
---
# <a name="ntgdiddrendermocomp-function"></a><span data-ttu-id="b9989-103">NtGdiDdRenderMoComp fonction)</span><span class="sxs-lookup"><span data-stu-id="b9989-103">NtGdiDdRenderMoComp function</span></span>

<span data-ttu-id="b9989-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b9989-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="b9989-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="b9989-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="b9989-106">Indique au pilote le blocs macros à afficher en spécifiant les surfaces contenant les blocs macros, les décalages dans chaque surface où le blocs macros existe et la taille des données bloc macro à restituer.</span><span class="sxs-lookup"><span data-stu-id="b9989-106">Tells the driver what macroblocks to render by specifying the surfaces containing the macroblocks, the offsets in each surface where the macroblocks exist, and the size of the macroblock data to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9989-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9989-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdRenderMoComp(
  _In_    HANDLE               hMoComp,
  _Inout_ PDD_RENDERMOCOMPDATA puRenderMoCompData
);
```



## <a name="parameters"></a><span data-ttu-id="b9989-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9989-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9989-109">*hMoComp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9989-109">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9989-110">Handle vers une [**structure \_ \_ locale DD MOTIONCOMP**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) qui contient une description de la compensation de mouvement demandée.</span><span class="sxs-lookup"><span data-stu-id="b9989-110">Handle to a [**DD\_MOTIONCOMP\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) structure that contains a description of the motion compensation being requested.</span></span>

</dd> <dt>

<span data-ttu-id="b9989-111">*puRenderMoCompData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b9989-111">*puRenderMoCompData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9989-112">Pointeur vers une [**structure \_ RENDERMOCOMPDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_rendermocompdata) qui contient les informations nécessaires pour restituer un frame.</span><span class="sxs-lookup"><span data-stu-id="b9989-112">Pointer to a [**DD\_RENDERMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_rendermocompdata) structure that contains the information needed to render a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9989-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b9989-113">Return value</span></span>

<span data-ttu-id="b9989-114">**NtGdiDdRenderMoComp** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="b9989-114">**NtGdiDdRenderMoComp** returns one of the following callback codes.</span></span>



| <span data-ttu-id="b9989-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b9989-115">Return code</span></span>                                                                                              | <span data-ttu-id="b9989-116">Description</span><span class="sxs-lookup"><span data-stu-id="b9989-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b9989-117"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="b9989-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="b9989-118">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="b9989-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="b9989-119">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="b9989-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="b9989-120">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="b9989-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b9989-121"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="b9989-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="b9989-122">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="b9989-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="b9989-123">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b9989-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="b9989-124">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b9989-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b9989-125">Notes</span><span class="sxs-lookup"><span data-stu-id="b9989-125">Remarks</span></span>

<span data-ttu-id="b9989-126">Pour plus d’informations, consultez Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="b9989-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9989-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9989-127">Requirements</span></span>



| <span data-ttu-id="b9989-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9989-128">Requirement</span></span> | <span data-ttu-id="b9989-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9989-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9989-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9989-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b9989-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9989-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b9989-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9989-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b9989-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9989-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b9989-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9989-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9989-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9989-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9989-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9989-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9989-137">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="b9989-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
