---
description: Avertit le pilote qu’un décodeur logiciel va commencer à utiliser la compensation de mouvement avec le GUID spécifié.
ms.assetid: c9a55428-7fe6-45dd-987a-d9ab8ae8a1cb
title: NtGdiDdCreateMoComp, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1705b5bf7ac5eddd1ac39e14f3b91b7fd3728cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110590"
---
# <a name="ntgdiddcreatemocomp-function"></a><span data-ttu-id="f4ead-103">NtGdiDdCreateMoComp fonction)</span><span class="sxs-lookup"><span data-stu-id="f4ead-103">NtGdiDdCreateMoComp function</span></span>

<span data-ttu-id="f4ead-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f4ead-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="f4ead-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="f4ead-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="f4ead-106">Avertit le pilote qu’un décodeur logiciel va commencer à utiliser la compensation de mouvement avec le GUID spécifié.</span><span class="sxs-lookup"><span data-stu-id="f4ead-106">Notifies the driver that a software decoder will start using motion compensation with the specified GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ead-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4ead-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateMoComp(
  _In_    HANDLE               hDirectDraw,
  _Inout_ PDD_CREATEMOCOMPDATA puCreateMoCompData
);
```



## <a name="parameters"></a><span data-ttu-id="f4ead-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4ead-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4ead-109">*hDirectDraw* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f4ead-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ead-110">Handle vers un objet en mode noyau DirectDraw précédemment créé pour l’appareil sur lequel la compensation de mouvement doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f4ead-110">Handle to a previously created DirectDraw kernel-mode object for the device on which motion compensation is to be used.</span></span>

</dd> <dt>

<span data-ttu-id="f4ead-111">*puCreateMoCompData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f4ead-111">*puCreateMoCompData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ead-112">Pointeur vers une [**structure \_ CREATEMOCOMPDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createmocompdata) qui contient les informations requises pour commencer à utiliser la compensation de mouvement.</span><span class="sxs-lookup"><span data-stu-id="f4ead-112">Pointer to a [**DD\_CREATEMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createmocompdata) structure that contains the information required to begin using motion compensation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4ead-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f4ead-113">Return value</span></span>

<span data-ttu-id="f4ead-114">**NtGdiDdCreateMoComp** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="f4ead-114">**NtGdiDdCreateMoComp** returns one of the following callback codes.</span></span>



| <span data-ttu-id="f4ead-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f4ead-115">Return code</span></span>                                                                                              | <span data-ttu-id="f4ead-116">Description</span><span class="sxs-lookup"><span data-stu-id="f4ead-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f4ead-117"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ead-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="f4ead-118">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="f4ead-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="f4ead-119">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="f4ead-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="f4ead-120">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="f4ead-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="f4ead-121"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ead-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="f4ead-122">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="f4ead-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="f4ead-123">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f4ead-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="f4ead-124">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f4ead-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f4ead-125">Notes</span><span class="sxs-lookup"><span data-stu-id="f4ead-125">Remarks</span></span>

<span data-ttu-id="f4ead-126">Pour plus d’informations, consultez Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="f4ead-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4ead-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4ead-127">Requirements</span></span>



| <span data-ttu-id="f4ead-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4ead-128">Requirement</span></span> | <span data-ttu-id="f4ead-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4ead-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ead-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4ead-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f4ead-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4ead-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f4ead-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4ead-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f4ead-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4ead-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f4ead-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4ead-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4ead-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4ead-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4ead-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4ead-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ead-137">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="f4ead-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
