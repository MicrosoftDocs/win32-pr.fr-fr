---
description: Utilisé pour verrouiller une zone de mémoire tampon spécifiée et fournir un pointeur valide vers un bloc de mémoire associé à la mémoire tampon.
ms.assetid: 6f2ecefa-376c-4f6c-a031-666dd992f96a
title: NtGdiDdLockD3D, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdLockD3D
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c049d37e3507f5bf4429b6ffd5d8ec03327640e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514540"
---
# <a name="ntgdiddlockd3d-function"></a><span data-ttu-id="7c933-103">NtGdiDdLockD3D fonction)</span><span class="sxs-lookup"><span data-stu-id="7c933-103">NtGdiDdLockD3D function</span></span>

<span data-ttu-id="7c933-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7c933-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="7c933-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="7c933-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="7c933-106">Utilisé pour verrouiller une zone de mémoire tampon spécifiée et fournir un pointeur valide vers un bloc de mémoire associé à la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7c933-106">Used to lock a specified area of buffer memory and to provide a valid pointer to a block of memory associated with the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c933-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c933-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdLockD3D(
  _In_    HANDLE       hSurface,
  _Inout_ PDD_LOCKDATA puLockData
);
```



## <a name="parameters"></a><span data-ttu-id="7c933-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c933-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c933-109">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7c933-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c933-110">Pointeur vers une structure de [**\_ surface \_ locale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui décrit la surface associée à la région de mémoire à verrouiller.</span><span class="sxs-lookup"><span data-stu-id="7c933-110">Pointer to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface associated with the memory region to be locked down.</span></span>

</dd> <dt>

<span data-ttu-id="7c933-111">*puLockData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7c933-111">*puLockData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c933-112">Pointeur vers une [**structure \_ LOCKDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) qui contient les informations requises pour effectuer le verrouillage.</span><span class="sxs-lookup"><span data-stu-id="7c933-112">Pointer to a [**DD\_LOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) structure that contains the information required to perform the lock down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c933-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c933-113">Return value</span></span>

<span data-ttu-id="7c933-114">**NtGdiDdLockD3D** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="7c933-114">**NtGdiDdLockD3D** returns one of the following callback codes.</span></span>



| <span data-ttu-id="7c933-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7c933-115">Return code</span></span>                                                                                              | <span data-ttu-id="7c933-116">Description</span><span class="sxs-lookup"><span data-stu-id="7c933-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c933-117"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="7c933-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="7c933-118">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="7c933-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="7c933-119">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="7c933-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="7c933-120">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="7c933-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="7c933-121"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="7c933-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="7c933-122">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="7c933-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="7c933-123">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7c933-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="7c933-124">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7c933-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7c933-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c933-125">Requirements</span></span>



| <span data-ttu-id="7c933-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c933-126">Requirement</span></span> | <span data-ttu-id="7c933-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c933-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7c933-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c933-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7c933-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c933-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7c933-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c933-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7c933-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c933-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7c933-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c933-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c933-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c933-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c933-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c933-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c933-135">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="7c933-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
