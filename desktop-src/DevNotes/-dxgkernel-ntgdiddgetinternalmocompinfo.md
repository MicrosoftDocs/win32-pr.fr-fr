---
description: Permet au pilote de signaler qu’il alloue en interne de la mémoire d’affichage pour effectuer la compensation de mouvement.
ms.assetid: cf2878ae-7eff-4214-bb9e-e8b608831108
title: NtGdiDdGetInternalMoCompInfo, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetInternalMoCompInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a9ddbb7843c7a1142ac6cd9906ef1ed3265e5d11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861086"
---
# <a name="ntgdiddgetinternalmocompinfo-function"></a><span data-ttu-id="0d38a-103">NtGdiDdGetInternalMoCompInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="0d38a-103">NtGdiDdGetInternalMoCompInfo function</span></span>

<span data-ttu-id="0d38a-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0d38a-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="0d38a-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="0d38a-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="0d38a-106">Permet au pilote de signaler qu’il alloue en interne de la mémoire d’affichage pour effectuer la compensation de mouvement.</span><span class="sxs-lookup"><span data-stu-id="0d38a-106">Allows the driver to report that it internally allocates display memory to perform motion compensation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d38a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d38a-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetInternalMoCompInfo(
  _In_    HANDLE                    hDirectDraw,
  _Inout_ PDD_GETINTERNALMOCOMPDATA puGetInternalData
);
```



## <a name="parameters"></a><span data-ttu-id="0d38a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d38a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d38a-109">*hDirectDraw* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d38a-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d38a-110">Handle vers l’objet DirectDraw en mode noyau précédemment créé.</span><span class="sxs-lookup"><span data-stu-id="0d38a-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="0d38a-111">*puGetInternalData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0d38a-111">*puGetInternalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d38a-112">Pointeur vers une [**structure \_ GETINTERNALMOCOMPDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getinternalmocompdata) qui contient les exigences en matière de mémoire interne.</span><span class="sxs-lookup"><span data-stu-id="0d38a-112">Pointer to a [**DD\_GETINTERNALMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getinternalmocompdata) structure that contains the internal memory requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d38a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d38a-113">Return value</span></span>

<span data-ttu-id="0d38a-114">**NtGdiDdGetInternalMoCompInfo** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="0d38a-114">**NtGdiDdGetInternalMoCompInfo** returns one of the following callback codes.</span></span>



| <span data-ttu-id="0d38a-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0d38a-115">Return code</span></span>                                                                                              | <span data-ttu-id="0d38a-116">Description</span><span class="sxs-lookup"><span data-stu-id="0d38a-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d38a-117"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="0d38a-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="0d38a-118">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="0d38a-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="0d38a-119">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="0d38a-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="0d38a-120">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="0d38a-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="0d38a-121"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="0d38a-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="0d38a-122">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="0d38a-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="0d38a-123">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0d38a-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="0d38a-124">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0d38a-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d38a-125">Notes</span><span class="sxs-lookup"><span data-stu-id="0d38a-125">Remarks</span></span>

<span data-ttu-id="0d38a-126">Pour plus d’informations, consultez Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="0d38a-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d38a-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d38a-127">Requirements</span></span>



| <span data-ttu-id="0d38a-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d38a-128">Requirement</span></span> | <span data-ttu-id="0d38a-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d38a-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d38a-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d38a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0d38a-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d38a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="0d38a-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d38a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0d38a-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d38a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0d38a-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d38a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d38a-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d38a-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d38a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d38a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d38a-137">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="0d38a-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
