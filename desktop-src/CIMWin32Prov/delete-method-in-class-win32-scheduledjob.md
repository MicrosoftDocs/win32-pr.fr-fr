---
description: La suppression&\# 8194 ; La méthode de classe WMI supprime une tâche planifiée.
ms.assetid: 064ff3f8-6d41-4f8d-a511-6c051bb48a5b
ms.tgt_platform: multiple
title: Méthode Delete de la classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd375c3da85bd72bddfc97ed3f57e52103578441
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111643"
---
# <a name="delete-method-of-the-win32_scheduledjob-class"></a><span data-ttu-id="d5f1e-103">Méthode Delete de la \_ classe ScheduledJob Win32</span><span class="sxs-lookup"><span data-stu-id="d5f1e-103">Delete method of the Win32\_ScheduledJob class</span></span>

<span data-ttu-id="d5f1e-104">La méthode **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) supprime une tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes a scheduled job.</span></span>

<span data-ttu-id="d5f1e-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d5f1e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d5f1e-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d5f1e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f1e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5f1e-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="d5f1e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5f1e-108">Parameters</span></span>

<span data-ttu-id="d5f1e-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5f1e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5f1e-110">Return value</span></span>

<span data-ttu-id="d5f1e-111">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-111">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="d5f1e-112">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d5f1e-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d5f1e-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d5f1e-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d5f1e-114">**Opération réussie**</span><span class="sxs-lookup"><span data-stu-id="d5f1e-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="d5f1e-115">0</span><span class="sxs-lookup"><span data-stu-id="d5f1e-115">0</span></span>

<span data-ttu-id="d5f1e-116">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="d5f1e-117">**Non pris en charge**</span><span class="sxs-lookup"><span data-stu-id="d5f1e-117">**Not supported**</span></span>
</dt> <dd>

<span data-ttu-id="d5f1e-118">1</span><span class="sxs-lookup"><span data-stu-id="d5f1e-118">1</span></span>

<span data-ttu-id="d5f1e-119">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-119">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d5f1e-120">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="d5f1e-120">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d5f1e-121">2</span><span class="sxs-lookup"><span data-stu-id="d5f1e-121">2</span></span>

<span data-ttu-id="d5f1e-122">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="d5f1e-123">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="d5f1e-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d5f1e-124">8</span><span class="sxs-lookup"><span data-stu-id="d5f1e-124">8</span></span>

<span data-ttu-id="d5f1e-125">Processus interactif.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-125">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="d5f1e-126">**Chemin d'accès introuvable**</span><span class="sxs-lookup"><span data-stu-id="d5f1e-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="d5f1e-127">9</span><span class="sxs-lookup"><span data-stu-id="d5f1e-127">9</span></span>

<span data-ttu-id="d5f1e-128">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-128">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="d5f1e-129">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="d5f1e-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d5f1e-130">21</span><span class="sxs-lookup"><span data-stu-id="d5f1e-130">21</span></span>

<span data-ttu-id="d5f1e-131">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-131">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d5f1e-132">**Service non démarré**</span><span class="sxs-lookup"><span data-stu-id="d5f1e-132">**Service not started**</span></span>
</dt> <dd>

<span data-ttu-id="d5f1e-133">22</span><span class="sxs-lookup"><span data-stu-id="d5f1e-133">22</span></span>

<span data-ttu-id="d5f1e-134">Le compte sous lequel ce service doit s’exécuter n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="d5f1e-134">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="d5f1e-135">**Autres**</span><span class="sxs-lookup"><span data-stu-id="d5f1e-135">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d5f1e-136">23 4294967295</span><span class="sxs-lookup"><span data-stu-id="d5f1e-136">23 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5f1e-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5f1e-137">Requirements</span></span>



| <span data-ttu-id="d5f1e-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5f1e-138">Requirement</span></span> | <span data-ttu-id="d5f1e-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5f1e-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f1e-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5f1e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f1e-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5f1e-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5f1e-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5f1e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f1e-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5f1e-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5f1e-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d5f1e-144">Namespace</span></span><br/>                | <span data-ttu-id="d5f1e-145">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d5f1e-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d5f1e-146">MOF</span><span class="sxs-lookup"><span data-stu-id="d5f1e-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5f1e-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5f1e-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5f1e-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d5f1e-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5f1e-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5f1e-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5f1e-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5f1e-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5f1e-151">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d5f1e-151">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d5f1e-152">**\_ScheduledJob Win32**</span><span class="sxs-lookup"><span data-stu-id="d5f1e-152">**Win32\_ScheduledJob**</span></span>](win32-scheduledjob.md)
</dt> </dl>

 

