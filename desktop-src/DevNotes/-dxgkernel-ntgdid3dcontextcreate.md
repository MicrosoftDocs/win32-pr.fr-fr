---
description: Crée un contexte.
ms.assetid: f972ab40-c9e9-4d2a-88f6-4c7817d5533f
title: NtGdiD3DContextCreate, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextCreate
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: f59a80d3efd5e077bc1eadea66255ff5e6ea7523
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110143"
---
# <a name="ntgdid3dcontextcreate-function"></a><span data-ttu-id="a1025-103">NtGdiD3DContextCreate fonction)</span><span class="sxs-lookup"><span data-stu-id="a1025-103">NtGdiD3DContextCreate function</span></span>

<span data-ttu-id="a1025-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a1025-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="a1025-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="a1025-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="a1025-106">Crée un contexte.</span><span class="sxs-lookup"><span data-stu-id="a1025-106">Creates a context.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1025-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1025-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiD3DContextCreate(
  _In_    HANDLE                  hDirectDrawLocal,
  _In_    HANDLE                  hSurfColor,
  _In_    HANDLE                  hSurfZ,
  _Inout_ D3DNTHAL_CONTEXTCREATEI *pdcci
);
```



## <a name="parameters"></a><span data-ttu-id="a1025-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1025-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1025-109">*hDirectDrawLocal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1025-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1025-110">Handle vers un objet DirectDraw en mode noyau, créé précédemment avec [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md), représentant l’appareil sur lequel le contexte Direct3D doit être créé.</span><span class="sxs-lookup"><span data-stu-id="a1025-110">Handle to a kernel-mode DirectDraw object, previously created with [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md), representing the device on which the Direct3D context is to be created.</span></span>

</dd> <dt>

<span data-ttu-id="a1025-111">*hSurfColor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1025-111">*hSurfColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1025-112">Handle vers une structure de [**\_ surface \_ locale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui décrit la surface DirectDraw à utiliser comme cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="a1025-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the DirectDraw surface to be used as the rendering target.</span></span>

</dd> <dt>

<span data-ttu-id="a1025-113">*hSurfZ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1025-113">*hSurfZ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1025-114">Handle vers une structure de [**\_ surface \_ locale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui décrit la surface DirectDraw à utiliser comme mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="a1025-114">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the DirectDraw surface to be used as a depth buffer.</span></span> <span data-ttu-id="a1025-115">Si ce membre a la **valeur null**, aucune mise en mémoire tampon de profondeur ne doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="a1025-115">If this member is **NULL**, no depth buffering is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="a1025-116">*pdcci* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a1025-116">*pdcci* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1025-117">Pointeur vers une structure [**D3DNTHAL \_ CONTEXTCREATEDATA**](/windows-hardware/drivers/ddi/) qui contient les informations requises pour créer un contexte et les données que le pilote doit stocker dans le nouveau contexte.</span><span class="sxs-lookup"><span data-stu-id="a1025-117">Pointer to a [**D3DNTHAL\_CONTEXTCREATEDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required to create a context and the data that the driver should store in the new context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1025-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1025-118">Return value</span></span>

<span data-ttu-id="a1025-119">**NtGdiD3DContextCreate** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="a1025-119">**NtGdiD3DContextCreate** returns one of the following callback codes.</span></span>



| <span data-ttu-id="a1025-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a1025-120">Return code</span></span>                                                                                              | <span data-ttu-id="a1025-121">Description</span><span class="sxs-lookup"><span data-stu-id="a1025-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a1025-122"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="a1025-122"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="a1025-123">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="a1025-123">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="a1025-124">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="a1025-124">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="a1025-125">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="a1025-125">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="a1025-126"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="a1025-126"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="a1025-127">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="a1025-127">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="a1025-128">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="a1025-128">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="a1025-129">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a1025-129">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a1025-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1025-130">Requirements</span></span>



| <span data-ttu-id="a1025-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1025-131">Requirement</span></span> | <span data-ttu-id="a1025-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1025-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1025-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1025-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a1025-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1025-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="a1025-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1025-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a1025-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1025-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a1025-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1025-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1025-138"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1025-138"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1025-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1025-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1025-140">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="a1025-140">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
