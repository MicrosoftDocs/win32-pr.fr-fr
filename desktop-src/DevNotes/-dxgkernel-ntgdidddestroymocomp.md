---
description: Informe le pilote que cet objet de compensation de mouvement ne sera plus utilisé. Le pilote doit maintenant effectuer tout nettoyage nécessaire.
ms.assetid: 1d86a564-efe1-4971-99ec-2c9a6aa59c89
title: NtGdiDdDestroyMoComp, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: b7bc5915fe43bd4d48495b2b1beda8ee38f05fe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860914"
---
# <a name="ntgdidddestroymocomp-function"></a><span data-ttu-id="2a8eb-104">NtGdiDdDestroyMoComp fonction)</span><span class="sxs-lookup"><span data-stu-id="2a8eb-104">NtGdiDdDestroyMoComp function</span></span>

<span data-ttu-id="2a8eb-105">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2a8eb-105">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="2a8eb-106">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="2a8eb-106">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="2a8eb-107">Informe le pilote que cet objet de compensation de mouvement ne sera plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="2a8eb-107">Notifies the driver that this motion compensation object will no longer be used.</span></span> <span data-ttu-id="2a8eb-108">Le pilote doit maintenant effectuer tout nettoyage nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2a8eb-108">The driver now needs to perform any necessary cleanup.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a8eb-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a8eb-109">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroyMoComp(
  _In_    HANDLE                hMoComp,
  _Inout_ PDD_DESTROYMOCOMPDATA puBeginFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="2a8eb-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a8eb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a8eb-111">*hMoComp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2a8eb-111">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a8eb-112">Handle vers une [**structure \_ \_ locale MOTIONCOMP DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) qui contient une description de l’objet de compensation de mouvement à détruire.</span><span class="sxs-lookup"><span data-stu-id="2a8eb-112">Handle to a [**DD\_MOTIONCOMP\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) structure that contains a description of the motion compensation object to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="2a8eb-113">*puBeginFrameData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2a8eb-113">*puBeginFrameData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a8eb-114">Pointeur vers une [**structure \_ DESTROYMOCOMPDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroymocompdata) qui contient les informations nécessaires pour terminer la compensation de mouvement.</span><span class="sxs-lookup"><span data-stu-id="2a8eb-114">Pointer to a [**DD\_DESTROYMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroymocompdata) structure that contains the information needed to finish motion compensation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a8eb-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2a8eb-115">Return value</span></span>

<span data-ttu-id="2a8eb-116">**NtGdiDdDestroyMoComp** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="2a8eb-116">**NtGdiDdDestroyMoComp** returns one of the following callback codes.</span></span>



| <span data-ttu-id="2a8eb-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2a8eb-117">Return code</span></span>                                                                                              | <span data-ttu-id="2a8eb-118">Description</span><span class="sxs-lookup"><span data-stu-id="2a8eb-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a8eb-119"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="2a8eb-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="2a8eb-120">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="2a8eb-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="2a8eb-121">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="2a8eb-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="2a8eb-122">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="2a8eb-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="2a8eb-123"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="2a8eb-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="2a8eb-124">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="2a8eb-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="2a8eb-125">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2a8eb-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="2a8eb-126">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2a8eb-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2a8eb-127">Notes</span><span class="sxs-lookup"><span data-stu-id="2a8eb-127">Remarks</span></span>

<span data-ttu-id="2a8eb-128">Pour plus d’informations, consultez Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="2a8eb-128">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a8eb-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a8eb-129">Requirements</span></span>



| <span data-ttu-id="2a8eb-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a8eb-130">Requirement</span></span> | <span data-ttu-id="2a8eb-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a8eb-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a8eb-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a8eb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2a8eb-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a8eb-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="2a8eb-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a8eb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2a8eb-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a8eb-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2a8eb-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a8eb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a8eb-137"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a8eb-137"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a8eb-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a8eb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a8eb-139">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="2a8eb-139">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
