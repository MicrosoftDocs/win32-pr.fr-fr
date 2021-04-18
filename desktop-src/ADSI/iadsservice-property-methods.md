---
title: Méthodes de propriété IADsService (IADs. h)
description: Lisez et écrivez les propriétés décrites dans cette rubrique.
ms.assetid: ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsService ADSI
topic_type:
- apiref
api_name:
- IADsService Property Methods
- IADsService.Dependencies
- IADsService.get_Dependencies
- IADsService.put_Dependencies
- IADsService.DisplayName
- IADsService.get_DisplayName
- IADsService.put_DisplayName
- IADsService.ErrorControl
- IADsService.get_ErrorControl
- IADsService.put_ErrorControl
- IADsService.HostComputer
- IADsService.get_HostComputer
- IADsService.put_HostComputer
- IADsService.LoadOrderGroup
- IADsService.get_LoadOrderGroup
- IADsService.put_LoadOrderGroup
- IADsService.Path
- IADsService.get_Path
- IADsService.put_Path
- IADsService.ServiceAccountName
- IADsService.get_ServiceAccountName
- IADsService.put_ServiceAccountName
- IADsService.ServiceAccountPath
- IADsService.get_ServiceAccountPath
- IADsService.put_ServiceAccountPath
- IADsService.ServiceType
- IADsService.get_ServiceType
- IADsService.put_ServiceType
- IADsService.StartType
- IADsService.get_StartType
- IADsService.put_StartType
- IADsService.StartupParameters
- IADsService.get_StartupParameters
- IADsService.put_StartupParameters
- IADsService.Version
- IADsService.get_Version
- IADsService.put_Version
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b0e0d8b09618c7346280697843281ca74536c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512801"
---
# <a name="iadsservice-property-methods"></a><span data-ttu-id="a3279-104">Méthodes de propriété IADsService</span><span class="sxs-lookup"><span data-stu-id="a3279-104">IADsService Property Methods</span></span>

<span data-ttu-id="a3279-105">Les méthodes de propriété de l’interface [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice) lisent et écrivent les propriétés décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="a3279-105">The property methods of the [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="a3279-106">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="a3279-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="a3279-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a3279-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="a3279-108">**Dépendances**</span><span class="sxs-lookup"><span data-stu-id="a3279-108">**Dependencies**</span></span>
<span data-ttu-id="a3279-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a3279-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="a3279-110">Tableau de noms **BSTR** de services ou de groupes de charge qui doivent être chargés pour que ce service soit chargé.</span><span class="sxs-lookup"><span data-stu-id="a3279-110">Array of **BSTR** names of services or load groups that must be loaded for this service to load.</span></span> <span data-ttu-id="a3279-111">La syntaxe de l’entrée est « service : », suivie du nom du service ou « Group : », suivi du nom du groupe de charge.</span><span class="sxs-lookup"><span data-stu-id="a3279-111">The syntax for the entry is "Service:" followed by the service name or "Group:" followed by the load group name.</span></span>

<dt>

<span data-ttu-id="a3279-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a3279-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a3279-113">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="a3279-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Dependencies(
  [out] VARIANT* pvServiceDepend
);
HRESULT put_Dependencies(
  [in] VARIANT vServiceDepend
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3279-114">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="a3279-114">**DisplayName**</span></span>
<span data-ttu-id="a3279-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a3279-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="a3279-116">Nom convivial du service.</span><span class="sxs-lookup"><span data-stu-id="a3279-116">The friendly name of the service.</span></span>

<dt>

<span data-ttu-id="a3279-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a3279-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a3279-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a3279-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DisplayName(
  [out] BSTR* pbstrDisplayName
);
HRESULT put_DisplayName(
  [in] BSTR bstrDisplayName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3279-119">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="a3279-119">**ErrorControl**</span></span>
<span data-ttu-id="a3279-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a3279-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="a3279-121">Action à effectuer en cas d’échec de ce service au démarrage.</span><span class="sxs-lookup"><span data-stu-id="a3279-121">The action to be performed if this service fails on startup.</span></span> <span data-ttu-id="a3279-122">Les valeurs valides pour cette propriété sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="a3279-122">The following are valid values for this property.</span></span>

<dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span data-ttu-id="a3279-123"><span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>\_erreur de service ADS \_ \_ ignorée \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="a3279-123"><span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_IGNORE\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="a3279-124">Le programme de démarrage consigne l’erreur, mais poursuit l’opération de démarrage.</span><span class="sxs-lookup"><span data-stu-id="a3279-124">The startup program logs the error, but continues the startup operation.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span data-ttu-id="a3279-125"><span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>\_erreur de service ADS \_ \_ normale \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="a3279-125"><span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_NORMAL\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="a3279-126">Le programme de démarrage consigne l’erreur et affiche une boîte de message, mais poursuit l’opération de démarrage.</span><span class="sxs-lookup"><span data-stu-id="a3279-126">The startup program logs the error and presents a message box, but continues the startup operation.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span data-ttu-id="a3279-127"><span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\_erreur de service ADS \_ \_ critique \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="a3279-127"><span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_SEVERE\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="a3279-128">Le programme de démarrage consigne l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a3279-128">The startup program logs the error.</span></span> <span data-ttu-id="a3279-129">Si la dernière bonne configuration connue est démarrée, l’opération de démarrage continue.</span><span class="sxs-lookup"><span data-stu-id="a3279-129">If the last-known-good configuration is started, the startup operation continues.</span></span> <span data-ttu-id="a3279-130">Dans le cas contraire, le système est redémarré avec la dernière bonne configuration connue.</span><span class="sxs-lookup"><span data-stu-id="a3279-130">Otherwise, the system is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span data-ttu-id="a3279-131"><span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\_erreur de service ADS \_ \_ critique \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="a3279-131"><span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_CRITICAL\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="a3279-132">Le programme de démarrage consigne l’erreur, si possible.</span><span class="sxs-lookup"><span data-stu-id="a3279-132">The startup program logs the error, if possible.</span></span> <span data-ttu-id="a3279-133">Si la dernière bonne configuration connue est en cours de démarrage, l’opération de démarrage échoue.</span><span class="sxs-lookup"><span data-stu-id="a3279-133">If the last-known-good configuration is being started, the startup operation fails.</span></span> <span data-ttu-id="a3279-134">Dans le cas contraire, le système est redémarré avec la dernière bonne configuration connue.</span><span class="sxs-lookup"><span data-stu-id="a3279-134">Otherwise, the system is restarted with the last-known good configuration.</span></span>

</dd> </dl> <dt>

<span data-ttu-id="a3279-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a3279-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a3279-136">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="a3279-136">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ErrorControl(
  [out] LONG* plErrorControl
);
HRESULT put_ErrorControl(
  [in] LONG lErrorControl
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3279-137">**HostComputer**</span><span class="sxs-lookup"><span data-stu-id="a3279-137">**HostComputer**</span></span>
<span data-ttu-id="a3279-138"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a3279-138"></dt> <dd> <dl></span></span>

<span data-ttu-id="a3279-139">Chaîne ADsPath de l’hôte de ce service.</span><span class="sxs-lookup"><span data-stu-id="a3279-139">The ADsPath string of the host of this service.</span></span>

<dt>

<span data-ttu-id="a3279-140">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a3279-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a3279-141">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a3279-141">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3279-142">**LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="a3279-142">**LoadOrderGroup**</span></span>
<span data-ttu-id="a3279-143"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a3279-143"></dt> <dd> <dl></span></span>

<span data-ttu-id="a3279-144">Nom du groupe d’ordre de chargement dont ce service est membre.</span><span class="sxs-lookup"><span data-stu-id="a3279-144">Name of the load order group that this service is a member.</span></span>

<dt>

<span data-ttu-id="a3279-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a3279-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a3279-146">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a3279-146">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoadOrderGroup(
  [out] BSTR* pbstrLoadOrderGroup
);
HRESULT put_LoadOrderGroup(
  [in] BSTR bstrLoadOrderGroup
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3279-147">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="a3279-147">**Path**</span></span>
<span data-ttu-id="a3279-148"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a3279-148"></dt> <dd> <dl></span></span>

<span data-ttu-id="a3279-149">Chemin d’accès et nom de fichier du fichier exécutable de ce service.</span><span class="sxs-lookup"><span data-stu-id="a3279-149">Path and filename to the executable of this service.</span></span>

<dt>

<span data-ttu-id="a3279-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a3279-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a3279-151">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a3279-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3279-152">**ServiceAccountName**</span><span class="sxs-lookup"><span data-stu-id="a3279-152">**ServiceAccountName**</span></span>
<span data-ttu-id="a3279-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a3279-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="a3279-154">Nom du compte utilisé par ce service pour s’authentifier au démarrage.</span><span class="sxs-lookup"><span data-stu-id="a3279-154">Name of the account that this service uses to authenticate itself on startup.</span></span>

<dt>

<span data-ttu-id="a3279-155">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a3279-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a3279-156">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a3279-156">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountName(
  [out] BSTR* pbstrServiceAccountName
);
HRESULT put_ServiceAccountName(
  [in] BSTR bstrServiceAccountName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3279-157">**ServiceAccountPath**</span><span class="sxs-lookup"><span data-stu-id="a3279-157">**ServiceAccountPath**</span></span>
<span data-ttu-id="a3279-158"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a3279-158"></dt> <dd> <dl></span></span>

<span data-ttu-id="a3279-159">Chemin d’accès du compte spécifié par la propriété **ServiceAccountPath** .</span><span class="sxs-lookup"><span data-stu-id="a3279-159">Path of the account specified by the **ServiceAccountPath** property.</span></span>

<dt>

<span data-ttu-id="a3279-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a3279-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a3279-161">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a3279-161">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountPath(
  [out] BSTR* pbstrServiceAccountPath
);
HRESULT put_ServiceAccountPath(
  [in] BSTR bstrServiceAccountPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3279-162">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="a3279-162">**ServiceType**</span></span>
<span data-ttu-id="a3279-163"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a3279-163"></dt> <dd> <dl></span></span>

<span data-ttu-id="a3279-164">Description de la façon dont un service s’affiche sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="a3279-164">The description of how a service presents itself on the host computer.</span></span> <span data-ttu-id="a3279-165">Cette propriété peut avoir la valeur zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a3279-165">This property can be zero or a combination of one or more of the following values.</span></span>

<dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

<span data-ttu-id="a3279-166">\_ \_ Pilote du noyau du service ADS \_ \* \* \* (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="a3279-166">\*\*\*\*ADS\_SERVICE\_KERNEL\_DRIVER\*\*\*\* (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

<span data-ttu-id="a3279-167">\_Pilote du \_ système de fichiers du service ADS \* \* \* \* \_ \_ (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="a3279-167">\*\*\*\*ADS\_SERVICE\_FILE\_SYSTEM\_DRIVER\*\*\*\* (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

<span data-ttu-id="a3279-168">\_Processus propre au service ADS \_ \_ \* \* \* \* (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="a3279-168">\*\*\*\*ADS\_SERVICE\_OWN\_PROCESS\*\*\*\* (0x00000010)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

<span data-ttu-id="a3279-169">\_ \_ \_ Processus de partage de service ADS \* \* \* \* (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="a3279-169">\*\*\*\*ADS\_SERVICE\_SHARE\_PROCESS\*\*\*\* (0x00000020)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="a3279-170">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a3279-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a3279-171">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="a3279-171">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceType(
  [out] LONG* plServiceType
);
HRESULT put_ServiceType(
  [in] LONG lServiceType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3279-172">**Type de démarrage**</span><span class="sxs-lookup"><span data-stu-id="a3279-172">**StartType**</span></span>
<span data-ttu-id="a3279-173"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a3279-173"></dt> <dd> <dl></span></span>

<span data-ttu-id="a3279-174">Détermine comment démarrer le service.</span><span class="sxs-lookup"><span data-stu-id="a3279-174">Determines how to start the service.</span></span> <span data-ttu-id="a3279-175">Les valeurs valides pour cette propriété sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="a3279-175">The following are valid values for this property.</span></span>

<dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span data-ttu-id="a3279-176"><span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>démarrage du \_ démarrage du service ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="a3279-176"><span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>\*\*\*\*ADS\_SERVICE\_BOOT\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="a3279-177">Le service est un pilote de périphérique Démarré par le chargeur du système.</span><span class="sxs-lookup"><span data-stu-id="a3279-177">The service is a device driver started by the system loader.</span></span> <span data-ttu-id="a3279-178">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="a3279-178">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span data-ttu-id="a3279-179"><span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\_démarrage du système de service ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="a3279-179"><span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\*\*\*\*ADS\_SERVICE\_SYSTEM\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="a3279-180">Le service est un pilote de périphérique Démarré par la fonction **IoInitSystem** .</span><span class="sxs-lookup"><span data-stu-id="a3279-180">The service is a device driver started by the **IoInitSystem** function.</span></span> <span data-ttu-id="a3279-181">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="a3279-181">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span data-ttu-id="a3279-182"><span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\_démarrage automatique du service ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="a3279-182"><span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\*\*\*\*ADS\_SERVICE\_AUTO\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="a3279-183">Le service est démarré automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="a3279-183">The service will be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span data-ttu-id="a3279-184"><span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>\_démarrage de \_ la demande de service ADS \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="a3279-184"><span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>\*\*\*\*ADS\_SERVICE\_DEMAND\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="a3279-185">Le service est démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la fonction [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) .</span><span class="sxs-lookup"><span data-stu-id="a3279-185">The service will be started by the service control manager when a process calls the [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) function.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span data-ttu-id="a3279-186"><span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\_service ADS \_ désactivé \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="a3279-186"><span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\*\*\*\*ADS\_SERVICE\_DISABLED\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="a3279-187">Le service ne peut pas être démarré.</span><span class="sxs-lookup"><span data-stu-id="a3279-187">The service cannot be started.</span></span> <span data-ttu-id="a3279-188">Les tentatives de démarrage du service entraînent la **\_ \_ désactivation du service d’erreur** de code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="a3279-188">Attempts to start the service result in the error code **ERROR\_SERVICE\_DISABLED**.</span></span>

</dd> </dl> <dt>

<span data-ttu-id="a3279-189">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a3279-189">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a3279-190">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="a3279-190">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartType(
  [out] LONG* plStartType
);
HRESULT put_StartType(
  [in] LONG lStartType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3279-191">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="a3279-191">**StartupParameters**</span></span>
<span data-ttu-id="a3279-192"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a3279-192"></dt> <dd> <dl></span></span>

<span data-ttu-id="a3279-193">Paramètres passés au service au démarrage.</span><span class="sxs-lookup"><span data-stu-id="a3279-193">Parameters passed to the service at startup.</span></span>

<dt>

<span data-ttu-id="a3279-194">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a3279-194">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a3279-195">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a3279-195">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartupParameters(
  [out] BSTR* pbstrStartupParameters
);
HRESULT put_StartupParameters(
  [in] BSTR bstrStartupParameters
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3279-196">**Version**</span><span class="sxs-lookup"><span data-stu-id="a3279-196">**Version**</span></span>
<span data-ttu-id="a3279-197"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a3279-197"></dt> <dd> <dl></span></span>

<span data-ttu-id="a3279-198">Version du service.</span><span class="sxs-lookup"><span data-stu-id="a3279-198">Version of the service.</span></span>

<dt>

<span data-ttu-id="a3279-199">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a3279-199">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a3279-200">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a3279-200">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Version(
  [out] BSTR* pbstrVersion
);
HRESULT put_Version(
  [in] BSTR bstrVersion
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="a3279-201">Exemples</span><span class="sxs-lookup"><span data-stu-id="a3279-201">Examples</span></span>

<span data-ttu-id="a3279-202">L’exemple de code suivant montre comment répertorier tous les services système disponibles qui s’exécutent sur l’ordinateur hôte, « monordinateur », ainsi que l’emplacement où trouver les exécutables des services.</span><span class="sxs-lookup"><span data-stu-id="a3279-202">The following code example shows how to list all the available system services running on the host computer, "myMachine", together with the location to find the executables of the services.</span></span>


```VB
Dim cp As IADsComputer
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
If (IsEmpty(cp) = False) Then
    cp.Filter = Array("Service")
    For Each service In cp
        MsgBox service.Name & " @" & service.path
    Next
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
```



## <a name="requirements"></a><span data-ttu-id="a3279-203">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3279-203">Requirements</span></span>



| <span data-ttu-id="a3279-204">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3279-204">Requirement</span></span> | <span data-ttu-id="a3279-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3279-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3279-206">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3279-206">Minimum supported client</span></span><br/> | <span data-ttu-id="a3279-207">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3279-207">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3279-208">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3279-208">Minimum supported server</span></span><br/> | <span data-ttu-id="a3279-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3279-209">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3279-210">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3279-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3279-211"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3279-211"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="a3279-212">DLL</span><span class="sxs-lookup"><span data-stu-id="a3279-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3279-213"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3279-213"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="a3279-214">IID</span><span class="sxs-lookup"><span data-stu-id="a3279-214">IID</span></span><br/>                      | <span data-ttu-id="a3279-215">IID \_ IADsService est défini en tant que 68AF66E0-31CA-11CF-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="a3279-215">IID\_IADsService is defined as 68AF66E0-31CA-11CF-A98A-00AA006BC149</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a3279-216">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3279-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3279-217">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="a3279-217">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="a3279-218">Méthodes de propriété d’interface</span><span class="sxs-lookup"><span data-stu-id="a3279-218">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

