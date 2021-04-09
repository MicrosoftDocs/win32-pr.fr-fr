---
description: Génère le rendu des primitives et retourne l’état de rendu mis à jour.
ms.assetid: ef28ee62-a7ad-406c-a892-ffee14123d16
title: NtGdiD3DDrawPrimitives2, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DDrawPrimitives2
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: ebde2fd5adf3b0892606d0ebbc1c7d5f6b55d9cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033623"
---
# <a name="ntgdid3ddrawprimitives2-function"></a><span data-ttu-id="fa00c-103">NtGdiD3DDrawPrimitives2 fonction)</span><span class="sxs-lookup"><span data-stu-id="fa00c-103">NtGdiD3DDrawPrimitives2 function</span></span>

<span data-ttu-id="fa00c-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fa00c-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="fa00c-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="fa00c-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="fa00c-106">Génère le rendu des primitives et retourne l’état de rendu mis à jour.</span><span class="sxs-lookup"><span data-stu-id="fa00c-106">Renders primitives and returns the updated render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa00c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa00c-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DDrawPrimitives2(
  _In_    HANDLE                         hCmdBuf,
  _In_    HANDLE                         hVBuf,
  _Inout_ LPD3DNTHAL_DRAWPRIMITIVES2DATA pded,
  _Inout_ FLATPTR                        *pfpVidMemCmd,
  _Inout_ DWORD                          *pdwSizeCmd,
  _Inout_ FLATPTR                        *pfpVidMemVtx,
  _Inout_ DWORD                          *pdwSizeVtx
);
```



## <a name="parameters"></a><span data-ttu-id="fa00c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa00c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa00c-109">*hCmdBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa00c-109">*hCmdBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa00c-110">Handle de la [**structure \_ \_ locale de la surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui identifie la surface DirectDraw contenant les données de commande.</span><span class="sxs-lookup"><span data-stu-id="fa00c-110">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that identifies the DirectDraw surface containing the command data.</span></span>

</dd> <dt>

<span data-ttu-id="fa00c-111">*hVBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa00c-111">*hVBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa00c-112">Handle vers la structure de [**\_ surface \_ locale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui identifie la surface DirectDraw contenant les données de vertex.</span><span class="sxs-lookup"><span data-stu-id="fa00c-112">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that identifies the DirectDraw surface containing the vertex data.</span></span>

</dd> <dt>

<span data-ttu-id="fa00c-113">*PDED* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fa00c-113">*pded* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa00c-114">Pointeur vers une structure [**D3DNTHAL \_ DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/) qui contient les informations requises pour que le pilote restitue une ou plusieurs Primitives.</span><span class="sxs-lookup"><span data-stu-id="fa00c-114">Pointer to a [**D3DNTHAL\_DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to render one or more primitives.</span></span>

</dd> <dt>

<span data-ttu-id="fa00c-115">*pfpVidMemCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fa00c-115">*pfpVidMemCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa00c-116">Nouveau pointeur vers la mémoire vidéo si le pilote a remplacé le tampon de commande.</span><span class="sxs-lookup"><span data-stu-id="fa00c-116">New pointer to video memory if the driver swapped the command buffer.</span></span>

</dd> <dt>

<span data-ttu-id="fa00c-117">*pdwSizeCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fa00c-117">*pdwSizeCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa00c-118">Spécifie le nombre minimal d’octets par lequel le pilote doit augmenter la mémoire tampon de la commande swap.</span><span class="sxs-lookup"><span data-stu-id="fa00c-118">Specifies the minimum number of bytes that the driver must increase the swap command buffer by.</span></span>

</dd> <dt>

<span data-ttu-id="fa00c-119">*pfpVidMemVtx* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fa00c-119">*pfpVidMemVtx* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa00c-120">Nouveau pointeur vers la mémoire vidéo si le pilote a remplacé la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="fa00c-120">New pointer to video memory if the driver swapped the vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="fa00c-121">*pdwSizeVtx* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fa00c-121">*pdwSizeVtx* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa00c-122">Spécifie le nombre minimal d’octets que le pilote doit allouer pour la mémoire tampon de vertex swap.</span><span class="sxs-lookup"><span data-stu-id="fa00c-122">Specifies the minimum number of bytes that the driver must allocate for the swap vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa00c-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa00c-123">Return value</span></span>

<span data-ttu-id="fa00c-124">**NtGdiD3DDrawPrimitives2** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="fa00c-124">**NtGdiD3DDrawPrimitives2** returns one of the following callback codes.</span></span>



| <span data-ttu-id="fa00c-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fa00c-125">Return code</span></span>                                                                                              | <span data-ttu-id="fa00c-126">Description</span><span class="sxs-lookup"><span data-stu-id="fa00c-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fa00c-127"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="fa00c-127"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="fa00c-128">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="fa00c-128">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="fa00c-129">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="fa00c-129">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="fa00c-130">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="fa00c-130">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="fa00c-131"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="fa00c-131"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="fa00c-132">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="fa00c-132">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="fa00c-133">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="fa00c-133">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="fa00c-134">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fa00c-134">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fa00c-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa00c-135">Requirements</span></span>



| <span data-ttu-id="fa00c-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa00c-136">Requirement</span></span> | <span data-ttu-id="fa00c-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa00c-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fa00c-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa00c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fa00c-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa00c-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="fa00c-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa00c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fa00c-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa00c-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fa00c-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa00c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa00c-143"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa00c-143"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa00c-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa00c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa00c-145">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="fa00c-145">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
