---
description: Détruit un objet surface Microsoft DirectDraw précédemment alloué en mode noyau qui a été créé avec le membre dwCaps de la structure DDSCAPS défini sur DDSCAPS \_ EXECUTEBUFFER.
ms.assetid: c737b706-25be-49b8-8d8c-35f48aea2889
title: NtGdiDdDestroyD3DBuffer, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: e88394e8cc3d13e1d117a1e53eab1190b1290ca4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747717"
---
# <a name="ntgdidddestroyd3dbuffer-function"></a><span data-ttu-id="26237-103">NtGdiDdDestroyD3DBuffer fonction)</span><span class="sxs-lookup"><span data-stu-id="26237-103">NtGdiDdDestroyD3DBuffer function</span></span>

<span data-ttu-id="26237-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="26237-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="26237-105">Utilisez à la place DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="26237-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="26237-106">Détruit un objet surface Microsoft DirectDraw précédemment alloué en mode noyau qui a été créé avec le membre **dwCaps** de la structure [**DDSCAPS**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)) défini sur DDSCAPS \_ EXECUTEBUFFER.</span><span class="sxs-lookup"><span data-stu-id="26237-106">Destroys a previously allocated kernel-mode Microsoft DirectDraw surface object that was created with the **dwCaps** member of the [**DDSCAPS**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)) structure set to DDSCAPS\_EXECUTEBUFFER.</span></span>

## <a name="syntax"></a><span data-ttu-id="26237-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26237-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroyD3DBuffer(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="26237-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26237-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26237-109">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26237-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26237-110">Handle vers une [**structure \_ DESTROYSURFACEDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata) qui contient les informations nécessaires pour détruire une commande Direct3D ou une mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="26237-110">Handle to a [**DD\_DESTROYSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata) structure that contains the information needed to destroy a Direct3D command or vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26237-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26237-111">Return value</span></span>

<span data-ttu-id="26237-112">**NtGdiDdDestroyD3DBuffer** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="26237-112">**NtGdiDdDestroyD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="26237-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="26237-113">Return code</span></span>                                                                                              | <span data-ttu-id="26237-114">Description</span><span class="sxs-lookup"><span data-stu-id="26237-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="26237-115"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="26237-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="26237-116">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="26237-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="26237-117">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="26237-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="26237-118">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="26237-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="26237-119"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="26237-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="26237-120">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="26237-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="26237-121">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="26237-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="26237-122">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="26237-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="26237-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26237-123">Requirements</span></span>



| <span data-ttu-id="26237-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26237-124">Requirement</span></span> | <span data-ttu-id="26237-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="26237-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26237-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26237-126">Minimum supported client</span></span><br/> | <span data-ttu-id="26237-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26237-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="26237-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26237-128">Minimum supported server</span></span><br/> | <span data-ttu-id="26237-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26237-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="26237-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="26237-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="26237-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="26237-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26237-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26237-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26237-133">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="26237-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
