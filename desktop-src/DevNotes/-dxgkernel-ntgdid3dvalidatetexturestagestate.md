---
description: Retourne le nombre de passes où le matériel peut effectuer les opérations de fusion spécifiées dans l’état actuel.
ms.assetid: 355dae78-cd65-4fc9-8f08-8e5ae123064b
title: NtGdiD3DValidateTextureStageState, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DValidateTextureStageState
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 37c852343c70c5d3325926c9108dcab2948fdc95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860814"
---
# <a name="ntgdid3dvalidatetexturestagestate-function"></a><span data-ttu-id="ed4e1-103">NtGdiD3DValidateTextureStageState fonction)</span><span class="sxs-lookup"><span data-stu-id="ed4e1-103">NtGdiD3DValidateTextureStageState function</span></span>

<span data-ttu-id="ed4e1-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="ed4e1-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="ed4e1-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="ed4e1-106">Retourne le nombre de passes où le matériel peut effectuer les opérations de fusion spécifiées dans l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-106">Returns the number of passes where the hardware can perform the blending operations specified in the current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed4e1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed4e1-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DValidateTextureStageState(
  _Inout_ LPD3DNTHAL_VALIDATETEXTURESTAGESTATEDATA pData
);
```



## <a name="parameters"></a><span data-ttu-id="ed4e1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed4e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed4e1-109">*pData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ed4e1-109">*pData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed4e1-110">Pointeur vers une structure [**D3DNTHAL \_ VALIDATETEXTURESTAGESTATEDATA**](/windows-hardware/drivers/ddi/) qui contient les informations requises pour que le pilote détermine et retourne le nombre de passes requis pour effectuer les opérations de fusion.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-110">Pointer to a [**D3DNTHAL\_VALIDATETEXTURESTAGESTATEDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to determine and return the number of passes required to perform the blending operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed4e1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed4e1-111">Return value</span></span>

<span data-ttu-id="ed4e1-112">**NtGdiD3DValidateTextureStageState** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-112">**NtGdiD3DValidateTextureStageState** returns one of the following callback codes.</span></span>



| <span data-ttu-id="ed4e1-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ed4e1-113">Return code</span></span>                                                                                              | <span data-ttu-id="ed4e1-114">Description</span><span class="sxs-lookup"><span data-stu-id="ed4e1-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ed4e1-115"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="ed4e1-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="ed4e1-116">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="ed4e1-117">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="ed4e1-118">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="ed4e1-119"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="ed4e1-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="ed4e1-120">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="ed4e1-121">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="ed4e1-122">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ed4e1-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ed4e1-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed4e1-123">Requirements</span></span>



| <span data-ttu-id="ed4e1-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed4e1-124">Requirement</span></span> | <span data-ttu-id="ed4e1-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed4e1-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed4e1-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed4e1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ed4e1-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed4e1-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ed4e1-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed4e1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ed4e1-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed4e1-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ed4e1-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="ed4e1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed4e1-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed4e1-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed4e1-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed4e1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed4e1-133">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="ed4e1-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
