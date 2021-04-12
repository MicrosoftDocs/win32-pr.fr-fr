---
description: Définit la valeur de clé de couleur pour la surface spécifiée.
ms.assetid: 052dba97-c047-4ef7-a908-2a66ade3af10
title: NtGdiDdSetColorKey, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetColorKey
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7d6186df13ee88ca3de4f123381c012548b1cd85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523004"
---
# <a name="ntgdiddsetcolorkey-function"></a><span data-ttu-id="141d3-103">NtGdiDdSetColorKey fonction)</span><span class="sxs-lookup"><span data-stu-id="141d3-103">NtGdiDdSetColorKey function</span></span>

<span data-ttu-id="141d3-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="141d3-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="141d3-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="141d3-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="141d3-106">Définit la valeur de clé de couleur pour la surface spécifiée.</span><span class="sxs-lookup"><span data-stu-id="141d3-106">Sets the color key value for the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="141d3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="141d3-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetColorKey(
  _In_    HANDLE              hSurface,
  _Inout_ PDD_SETCOLORKEYDATA puSetColorKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="141d3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="141d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="141d3-109">*hSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="141d3-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="141d3-110">Pointeur vers la structure de [**\_ surface \_ locale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui décrit la surface à laquelle la clé de couleur doit être associée.</span><span class="sxs-lookup"><span data-stu-id="141d3-110">Pointer to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface with which the color key is to be associated.</span></span>

</dd> <dt>

<span data-ttu-id="141d3-111">*puSetColorKeyData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="141d3-111">*puSetColorKeyData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="141d3-112">Pointeur vers une [**structure \_ SETCOLORKEYDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setcolorkeydata) qui contient les informations requises pour définir la clé de couleur pour la surface spécifiée.</span><span class="sxs-lookup"><span data-stu-id="141d3-112">Pointer to a [**DD\_SETCOLORKEYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setcolorkeydata) structure that contains the information required to set the color key for the specified surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="141d3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="141d3-113">Return value</span></span>

<span data-ttu-id="141d3-114">**NtGdiDdSetColorKey** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="141d3-114">**NtGdiDdSetColorKey** returns one of the following callback codes.</span></span>



| <span data-ttu-id="141d3-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="141d3-115">Return code</span></span>                                                                                              | <span data-ttu-id="141d3-116">Description</span><span class="sxs-lookup"><span data-stu-id="141d3-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="141d3-117"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="141d3-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="141d3-118">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="141d3-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="141d3-119">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="141d3-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="141d3-120">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="141d3-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="141d3-121"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="141d3-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="141d3-122">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="141d3-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="141d3-123">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="141d3-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="141d3-124">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="141d3-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="141d3-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="141d3-125">Requirements</span></span>



| <span data-ttu-id="141d3-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="141d3-126">Requirement</span></span> | <span data-ttu-id="141d3-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="141d3-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="141d3-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="141d3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="141d3-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="141d3-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="141d3-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="141d3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="141d3-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="141d3-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="141d3-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="141d3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="141d3-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="141d3-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="141d3-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="141d3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="141d3-135">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="141d3-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
