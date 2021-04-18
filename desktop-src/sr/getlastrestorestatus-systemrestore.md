---
title: Méthode GetLastRestoreStatus de la classe SystemRestore
description: Récupère l’état de la dernière restauration du système.
ms.assetid: 03f9fd71-9f20-428e-bdca-4692e838581a
keywords:
- Restauration du système de méthode GetLastRestoreStatus
- Restauration du système de méthode GetLastRestoreStatus, classe SystemRestore
- Restauration du système de la classe SystemRestore, méthode GetLastRestoreStatus
topic_type:
- apiref
api_name:
- SystemRestore.GetLastRestoreStatus
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd1ef0e62f7874bb92f3c8e9ecec7b62a1b3ff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512777"
---
# <a name="getlastrestorestatus-method-of-the-systemrestore-class"></a><span data-ttu-id="d18d6-106">Méthode GetLastRestoreStatus de la classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="d18d6-106">GetLastRestoreStatus method of the SystemRestore class</span></span>

<span data-ttu-id="d18d6-107">Récupère l’état de la dernière restauration du système.</span><span class="sxs-lookup"><span data-stu-id="d18d6-107">Retrieves the status of the last system restore.</span></span>

## <a name="syntax"></a><span data-ttu-id="d18d6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d18d6-108">Syntax</span></span>


```mof
uint32 GetLastRestoreStatus();
```



## <a name="parameters"></a><span data-ttu-id="d18d6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d18d6-109">Parameters</span></span>

<span data-ttu-id="d18d6-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d18d6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d18d6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d18d6-111">Return value</span></span>

<span data-ttu-id="d18d6-112">La méthode retourne l’une des valeurs d’État suivantes.</span><span class="sxs-lookup"><span data-stu-id="d18d6-112">The method returns one of the following status values.</span></span>



| <span data-ttu-id="d18d6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d18d6-113">Return value</span></span>                                                                 | <span data-ttu-id="d18d6-114">Description</span><span class="sxs-lookup"><span data-stu-id="d18d6-114">Description</span></span>                                  |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d18d6-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d18d6-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="d18d6-116">La dernière restauration a échoué.</span><span class="sxs-lookup"><span data-stu-id="d18d6-116">The last restore failed.</span></span><br/>          |
| <dl> <span data-ttu-id="d18d6-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d18d6-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="d18d6-118">La dernière restauration a réussi.</span><span class="sxs-lookup"><span data-stu-id="d18d6-118">The last restore was successful.</span></span><br/>  |
| <dl> <span data-ttu-id="d18d6-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d18d6-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="d18d6-120">La dernière restauration a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="d18d6-120">The last restore was interrupted.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="d18d6-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="d18d6-121">Examples</span></span>


```VB
'GetLastRestoreStatus Method of the SystemRestore Class
'Retrieves the status of the last system restore.
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
stat = obj.GetLastRestoreStatus()
If stat = 0 Then
    wscript.Echo "Failed"
ElseIf stat = 1 Then 
    wscript.Echo "Success"
ElseIf stat = 2 Then
    wscript.Echo "Interrrupted"
End If
```



## <a name="requirements"></a><span data-ttu-id="d18d6-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d18d6-122">Requirements</span></span>



| <span data-ttu-id="d18d6-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d18d6-123">Requirement</span></span> | <span data-ttu-id="d18d6-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d18d6-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d18d6-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d18d6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d18d6-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d18d6-126">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d18d6-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d18d6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d18d6-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d18d6-128">None supported</span></span><br/>                                                         |
| <span data-ttu-id="d18d6-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d18d6-129">Namespace</span></span><br/>                | <span data-ttu-id="d18d6-130">Racine \\ par défaut</span><span class="sxs-lookup"><span data-stu-id="d18d6-130">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="d18d6-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d18d6-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d18d6-132"><dt>SR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d18d6-132"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d18d6-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d18d6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d18d6-134">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="d18d6-134">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





