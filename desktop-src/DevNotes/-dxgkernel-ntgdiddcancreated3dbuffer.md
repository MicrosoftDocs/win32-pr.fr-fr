---
description: Détermine si le pilote peut créer une mémoire tampon de commande ou de vertex au niveau du pilote de la description spécifiée.
ms.assetid: c67492d9-c4ba-4206-8beb-3d67235192f9
title: NtGdiDdCanCreateD3DBuffer, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCanCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 849eb2ba9c1349c54c20703217989b0b92ee78e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513303"
---
# <a name="ntgdiddcancreated3dbuffer-function"></a><span data-ttu-id="57aa0-103">NtGdiDdCanCreateD3DBuffer fonction)</span><span class="sxs-lookup"><span data-stu-id="57aa0-103">NtGdiDdCanCreateD3DBuffer function</span></span>

<span data-ttu-id="57aa0-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="57aa0-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="57aa0-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="57aa0-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="57aa0-106">Détermine si le pilote peut créer une mémoire tampon de commande ou de vertex au niveau du pilote de la description spécifiée.</span><span class="sxs-lookup"><span data-stu-id="57aa0-106">Determines whether the driver can create a driver-level command or vertex buffer of the specified description.</span></span>

## <a name="syntax"></a><span data-ttu-id="57aa0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57aa0-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCanCreateD3DBuffer(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_CANCREATESURFACEDATA puCanCreateSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="57aa0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57aa0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57aa0-109">*hDirectDraw* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="57aa0-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57aa0-110">Handle de la [**structure \_ \_ globale DD DirectDraw**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) représentant l’objet DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="57aa0-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="57aa0-111">*puCanCreateSurfaceData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="57aa0-111">*puCanCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="57aa0-112">Pointeur vers une structure [**DD \_ CANCREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) .</span><span class="sxs-lookup"><span data-stu-id="57aa0-112">Pointer to a [**DD\_CANCREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) structure.</span></span> <span data-ttu-id="57aa0-113">Cette structure contient les informations nécessaires au pilote pour déterminer si une mémoire tampon de la commande ou du vertex peut être créée.</span><span class="sxs-lookup"><span data-stu-id="57aa0-113">This structure contains the information required for the driver to determine whether a command or vertex buffer can be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57aa0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57aa0-114">Return value</span></span>

<span data-ttu-id="57aa0-115">**NtGdiDdCanCreateD3DBuffer** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="57aa0-115">**NtGdiDdCanCreateD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="57aa0-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="57aa0-116">Return code</span></span>                                                                                              | <span data-ttu-id="57aa0-117">Description</span><span class="sxs-lookup"><span data-stu-id="57aa0-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="57aa0-118"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="57aa0-118"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="57aa0-119">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="57aa0-119">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="57aa0-120">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="57aa0-120">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="57aa0-121">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="57aa0-121">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="57aa0-122"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="57aa0-122"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="57aa0-123">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="57aa0-123">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="57aa0-124">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="57aa0-124">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="57aa0-125">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="57aa0-125">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="57aa0-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57aa0-126">Requirements</span></span>



| <span data-ttu-id="57aa0-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57aa0-127">Requirement</span></span> | <span data-ttu-id="57aa0-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="57aa0-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="57aa0-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57aa0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="57aa0-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57aa0-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="57aa0-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57aa0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="57aa0-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57aa0-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="57aa0-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="57aa0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="57aa0-134"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="57aa0-134"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57aa0-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57aa0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57aa0-136">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="57aa0-136">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
