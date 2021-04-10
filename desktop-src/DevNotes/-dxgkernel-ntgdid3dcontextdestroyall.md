---
description: Interroge la quantité de mémoire disponible dans le segment de mémoire géré par le pilote.
ms.assetid: d7f8792b-a515-4e70-9474-6a3474b6612b
title: NtGdiD3DContextDestroyAll, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextDestroyAll
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 8bb42c902555568ebe7a26656cd188e9c8e40213
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860917"
---
# <a name="ntgdid3dcontextdestroyall-function"></a><span data-ttu-id="35de0-103">NtGdiD3DContextDestroyAll fonction)</span><span class="sxs-lookup"><span data-stu-id="35de0-103">NtGdiD3DContextDestroyAll function</span></span>

<span data-ttu-id="35de0-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="35de0-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="35de0-105">Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="35de0-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="35de0-106">Interroge la quantité de mémoire disponible dans le segment de mémoire géré par le pilote.</span><span class="sxs-lookup"><span data-stu-id="35de0-106">Queries the amount of free memory in the driver-managed memory heap.</span></span>

## <a name="syntax"></a><span data-ttu-id="35de0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35de0-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DContextDestroyAll(void);
```



## <a name="parameters"></a><span data-ttu-id="35de0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35de0-108">Parameters</span></span>

<span data-ttu-id="35de0-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="35de0-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35de0-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35de0-110">Return value</span></span>

<span data-ttu-id="35de0-111">**NtGdiD3DContextDestroyAll** retourne l’un des codes de rappel suivants.</span><span class="sxs-lookup"><span data-stu-id="35de0-111">**NtGdiD3DContextDestroyAll** returns one of the following callback codes.</span></span>



| <span data-ttu-id="35de0-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="35de0-112">Return code</span></span>                                                                                              | <span data-ttu-id="35de0-113">Description</span><span class="sxs-lookup"><span data-stu-id="35de0-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35de0-114"><dt>**\_pilote DDHAL \_ géré**</dt></span><span class="sxs-lookup"><span data-stu-id="35de0-114"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="35de0-115">Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="35de0-115">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="35de0-116">Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction.</span><span class="sxs-lookup"><span data-stu-id="35de0-116">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="35de0-117">Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.</span><span class="sxs-lookup"><span data-stu-id="35de0-117">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="35de0-118"><dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="35de0-118"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="35de0-119">Le pilote n’a pas de commentaire sur l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="35de0-119">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="35de0-120">Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="35de0-120">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="35de0-121">Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="35de0-121">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="35de0-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35de0-122">Requirements</span></span>



| <span data-ttu-id="35de0-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35de0-123">Requirement</span></span> | <span data-ttu-id="35de0-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="35de0-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35de0-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35de0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="35de0-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35de0-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="35de0-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35de0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="35de0-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35de0-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="35de0-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="35de0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="35de0-130"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="35de0-130"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35de0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35de0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35de0-132">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="35de0-132">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




