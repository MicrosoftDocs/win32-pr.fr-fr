---
description: Modifie le mode de démarrage d’un \_ service SystemDriver Win32.
ms.assetid: 34f4e0ac-d8a0-4be7-8c84-0252e50db441
ms.tgt_platform: multiple
title: Méthode ChangeStartMode de la classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: edb6dfc9d745f5e408871246b581e6fab7eb72d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523495"
---
# <a name="changestartmode-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="ca2e4-103">Méthode ChangeStartMode de la \_ classe Win32 SystemDriver</span><span class="sxs-lookup"><span data-stu-id="ca2e4-103">ChangeStartMode method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="ca2e4-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifie le mode de démarrage d’un service [**\_ SystemDriver Win32**](win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="ca2e4-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_SystemDriver**](win32-systemdriver.md) service.</span></span>

<span data-ttu-id="ca2e4-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ca2e4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ca2e4-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ca2e4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca2e4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca2e4-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="ca2e4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca2e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca2e4-109">*StartMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca2e4-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca2e4-110">Mode de démarrage du service de base Windows.</span><span class="sxs-lookup"><span data-stu-id="ca2e4-110">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="ca2e4-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>Démarrage du **démarrage** (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="ca2e4-112">Pilote de périphérique Démarré par le chargeur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ca2e4-112">Device driver started by the operating system loader.</span></span> <span data-ttu-id="ca2e4-113">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="ca2e4-113">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="ca2e4-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Système** (« système »)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="ca2e4-115">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ca2e4-115">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="ca2e4-116">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="ca2e4-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="ca2e4-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Démarrage automatique** (« automatique »)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="ca2e4-118">Le service doit être démarré automatiquement par le Gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="ca2e4-118">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="ca2e4-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Début de la demande** (« manuel »)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="ca2e4-120">Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="ca2e4-120">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ca2e4-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** ("désactivé")</span><span class="sxs-lookup"><span data-stu-id="ca2e4-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="ca2e4-122">Service qui ne peut plus être démarré.</span><span class="sxs-lookup"><span data-stu-id="ca2e4-122">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca2e4-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ca2e4-123">Return value</span></span>

<span data-ttu-id="ca2e4-124">Retourne la valeur 0 (zéro) si le service a été correctement modifié, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="ca2e4-124">Returns a value of 0 (zero) if the service was successfully modified, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ca2e4-125">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-125">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-126">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-126">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-127">**Accès refusé** (2)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-127">**Access Denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-128">**Services dépendants en cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-128">**Dependent Services Running** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-129">**Contrôle de service non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-129">**Invalid Service Control** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-130">**Le service ne peut pas accepter le contrôle** (5)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-130">**Service Cannot Accept Control** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-131">**Service non actif** (6)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-131">**Service Not Active** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-132">**Délai d’expiration** de la demande de service (7)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-132">**Service Request Timeout** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-133">**Échec inconnu** (8)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-133">**Unknown Failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-134">**Chemin introuvable** (9)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-134">**Path Not Found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-135">**Service déjà en cours d’exécution** (10)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-135">**Service Already Running** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-136">**Base de données de service verrouillée** (11)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-136">**Service Database Locked** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-137">**Dépendance de service supprimée** (12)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-137">**Service Dependency Deleted** (12)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-138">**Échec** de la dépendance du service (13)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-138">**Service Dependency Failure** (13)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-139">**Service désactivé** (14)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-139">**Service Disabled** (14)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-140">**Échec** de l’ouverture de session du service (15)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-140">**Service Logon Failed** (15)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-141">**Service marqué pour suppression** (16)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-141">**Service Marked For Deletion** (16)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-142">**Service sans thread** (17)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-142">**Service No Thread** (17)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-143">**Dépendance circulaire d’État** (18)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-143">**Status Circular Dependency** (18)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-144">**Nom de l’État en double** (19)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-144">**Status Duplicate Name** (19)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-145">**Nom de l’état non valide** (20)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-145">**Status Invalid Name** (20)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-146">**Paramètre d’État non valide** (21)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-146">**Status Invalid Parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-147">**Compte de service de l’état non valide** (22)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-147">**Status Invalid Service Account** (22)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-148">Le **service d’État existe** (23)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-148">**Status Service Exists** (23)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-149">**Service déjà suspendu** (24)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-149">**Service Already Paused** (24)</span></span>
</dt> <dt>

<span data-ttu-id="ca2e4-150">**Autre** (25 4294967295)</span><span class="sxs-lookup"><span data-stu-id="ca2e4-150">**Other** (25 4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ca2e4-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca2e4-151">Requirements</span></span>



| <span data-ttu-id="ca2e4-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca2e4-152">Requirement</span></span> | <span data-ttu-id="ca2e4-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca2e4-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca2e4-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca2e4-154">Minimum supported client</span></span><br/> | <span data-ttu-id="ca2e4-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca2e4-155">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca2e4-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca2e4-156">Minimum supported server</span></span><br/> | <span data-ttu-id="ca2e4-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca2e4-157">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca2e4-158">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ca2e4-158">Namespace</span></span><br/>                | <span data-ttu-id="ca2e4-159">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ca2e4-159">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ca2e4-160">MOF</span><span class="sxs-lookup"><span data-stu-id="ca2e4-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca2e4-161"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca2e4-161"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca2e4-162">DLL</span><span class="sxs-lookup"><span data-stu-id="ca2e4-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca2e4-163"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca2e4-163"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca2e4-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca2e4-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="ca2e4-165">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca2e4-165">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ca2e4-166">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="ca2e4-166">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

