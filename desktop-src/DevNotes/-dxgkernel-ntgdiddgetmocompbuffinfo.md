---
description: Permet au pilote de spécifier le nombre de surfaces intermédiaires requises pour prendre en charge le GUID spécifié, ainsi que la taille, l’emplacement et le format de chacune de ces surfaces.
ms.assetid: 1f3207a8-aa6a-47a3-a1d0-19166592eeca
title: NtGdiDdGetMoCompBuffInfo, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetMoCompBuffInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 03d471e62edd061ce167e0baf2051836e9634fae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033675"
---
# <a name="ntgdiddgetmocompbuffinfo-function"></a><span data-ttu-id="3808f-103">NtGdiDdGetMoCompBuffInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="3808f-103">NtGdiDdGetMoCompBuffInfo function</span></span>

<span data-ttu-id="3808f-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3808f-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="3808f-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="3808f-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="3808f-106">Permet au pilote de spécifier le nombre de surfaces intermédiaires requises pour prendre en charge le GUID spécifié, ainsi que la taille, l’emplacement et le format de chacune de ces surfaces.</span><span class="sxs-lookup"><span data-stu-id="3808f-106">Allows the driver to specify how many interim surfaces are required to support the specified GUID, and the size, location, and format of each of these surfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="3808f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3808f-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetMoCompBuffInfo(
  _In_    HANDLE                    hDirectDraw,
  _Inout_ PDD_GETMOCOMPCOMPBUFFDATA puGetBuffData
);
```



## <a name="parameters"></a><span data-ttu-id="3808f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3808f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3808f-109">*hDirectDraw* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3808f-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3808f-110">Handle vers l’objet DirectDraw en mode noyau précédemment créé.</span><span class="sxs-lookup"><span data-stu-id="3808f-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="3808f-111">*puGetBuffData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3808f-111">*puGetBuffData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3808f-112">Pointeur vers une [**structure \_ GETMOCOMPCOMPBUFFDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getmocompcompbuffdata) qui contient les informations de mémoire tampon compressées.</span><span class="sxs-lookup"><span data-stu-id="3808f-112">Pointer to a [**DD\_GETMOCOMPCOMPBUFFDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getmocompcompbuffdata) structure that contains the compressed buffer information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3808f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3808f-113">Return value</span></span>

<span data-ttu-id="3808f-114">**NtGdiDdGetMoCompBuffInfo** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="3808f-114">**NtGdiDdGetMoCompBuffInfo** returns one of the following callback codes.</span></span>



| <span data-ttu-id="3808f-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3808f-115">Return code</span></span>                                                                                              | <span data-ttu-id="3808f-116">Description</span><span class="sxs-lookup"><span data-stu-id="3808f-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3808f-117"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="3808f-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="3808f-118">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="3808f-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="3808f-119">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="3808f-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="3808f-120">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="3808f-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="3808f-121"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="3808f-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="3808f-122">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="3808f-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="3808f-123">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3808f-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="3808f-124">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3808f-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3808f-125">Notes</span><span class="sxs-lookup"><span data-stu-id="3808f-125">Remarks</span></span>

<span data-ttu-id="3808f-126">Pour plus d’informations, consultez Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="3808f-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="3808f-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3808f-127">Requirements</span></span>



| <span data-ttu-id="3808f-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3808f-128">Requirement</span></span> | <span data-ttu-id="3808f-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3808f-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3808f-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3808f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3808f-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3808f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3808f-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3808f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3808f-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3808f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3808f-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="3808f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3808f-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3808f-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3808f-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3808f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3808f-137">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="3808f-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
