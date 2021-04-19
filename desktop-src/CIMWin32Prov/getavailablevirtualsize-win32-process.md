---
description: Récupère la taille actuelle, en octets, de l’espace d’adressage virtuel libre disponible pour le processus.
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Méthode GetAvailableVirtualSize de la classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetAvailableVirtualSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ee6e798b8df32822de481f3af1dc6b21a81d1024
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536946"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a><span data-ttu-id="27b01-103">Méthode GetAvailableVirtualSize de la \_ classe de processus Win32</span><span class="sxs-lookup"><span data-stu-id="27b01-103">GetAvailableVirtualSize method of the Win32\_Process class</span></span>

<span data-ttu-id="27b01-104">Récupère la taille actuelle, en octets, de l’espace d’adressage virtuel libre disponible pour le processus.</span><span class="sxs-lookup"><span data-stu-id="27b01-104">Retrieves the current size, in bytes, of the free virtual address space available to the process.</span></span>

## <a name="syntax"></a><span data-ttu-id="27b01-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27b01-105">Syntax</span></span>


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a><span data-ttu-id="27b01-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27b01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27b01-107">*AvailableVirtualSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="27b01-107">*AvailableVirtualSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27b01-108">Le paramètre *AvailableVirtualSize* retourne l’espace d’adressage virtuel gratuit disponible pour ce processus.</span><span class="sxs-lookup"><span data-stu-id="27b01-108">The *AvailableVirtualSize* parameter returns the free virtual address space available to this process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27b01-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="27b01-109">Return value</span></span>

<span data-ttu-id="27b01-110">Retourne zéro (0) pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="27b01-110">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="27b01-111">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="27b01-111">Any other number indicates an error.</span></span> <span data-ttu-id="27b01-112">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="27b01-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="27b01-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="27b01-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="27b01-114">**Opération réussie**</span><span class="sxs-lookup"><span data-stu-id="27b01-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="27b01-115">0</span><span class="sxs-lookup"><span data-stu-id="27b01-115">0</span></span>

<span data-ttu-id="27b01-116">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="27b01-116">The operation completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="27b01-117">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="27b01-117">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="27b01-118">2</span><span class="sxs-lookup"><span data-stu-id="27b01-118">2</span></span>

<span data-ttu-id="27b01-119">L’utilisateur n’a pas accès aux informations demandées</span><span class="sxs-lookup"><span data-stu-id="27b01-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="27b01-120">**Privilèges insuffisants**</span><span class="sxs-lookup"><span data-stu-id="27b01-120">**Insufficient privilege**</span></span>
</dt> <dd>

<span data-ttu-id="27b01-121">3</span><span class="sxs-lookup"><span data-stu-id="27b01-121">3</span></span>

<span data-ttu-id="27b01-122">L’utilisateur ne dispose pas de privilèges suffisants.</span><span class="sxs-lookup"><span data-stu-id="27b01-122">The user does not have sufficient privilege.</span></span>

</dd> <dt>

<span data-ttu-id="27b01-123">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="27b01-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="27b01-124">8</span><span class="sxs-lookup"><span data-stu-id="27b01-124">8</span></span>

<span data-ttu-id="27b01-125">Échec inconnu.</span><span class="sxs-lookup"><span data-stu-id="27b01-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="27b01-126">**Chemin d'accès introuvable**</span><span class="sxs-lookup"><span data-stu-id="27b01-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="27b01-127">9</span><span class="sxs-lookup"><span data-stu-id="27b01-127">9</span></span>

<span data-ttu-id="27b01-128">Le chemin d'accès spécifié n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="27b01-128">The path specified does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="27b01-129">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="27b01-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="27b01-130">21</span><span class="sxs-lookup"><span data-stu-id="27b01-130">21</span></span>

<span data-ttu-id="27b01-131">Le paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="27b01-131">The specified parameter is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="27b01-132">**Autres**</span><span class="sxs-lookup"><span data-stu-id="27b01-132">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="27b01-133">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="27b01-133">22 4294967295</span></span>

<span data-ttu-id="27b01-134">Pour les valeurs autres que celles listées, reportez-vous à la documentation sur les [codes d’erreur système](/windows/desktop/Debug/system-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="27b01-134">For values other than those listed, refer to the [System Error Codes](/windows/desktop/Debug/system-error-codes) documentation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27b01-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27b01-135">Requirements</span></span>



| <span data-ttu-id="27b01-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27b01-136">Requirement</span></span> | <span data-ttu-id="27b01-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="27b01-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27b01-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27b01-138">Minimum supported client</span></span><br/> | <span data-ttu-id="27b01-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="27b01-139">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="27b01-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27b01-140">Minimum supported server</span></span><br/> | <span data-ttu-id="27b01-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="27b01-141">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="27b01-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="27b01-142">Namespace</span></span><br/>                | <span data-ttu-id="27b01-143">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="27b01-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="27b01-144">MOF</span><span class="sxs-lookup"><span data-stu-id="27b01-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27b01-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27b01-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="27b01-146">DLL</span><span class="sxs-lookup"><span data-stu-id="27b01-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27b01-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27b01-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27b01-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27b01-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27b01-149">**\_Processus Win32**</span><span class="sxs-lookup"><span data-stu-id="27b01-149">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

