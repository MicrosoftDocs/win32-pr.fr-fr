---
title: Classe Win32_TSDeploymentLicensing
description: Paramètres de licence pour le déploiement de la virtualisation de Bureau à distance (RDV).
ms.assetid: 78e95629-6580-4aa1-bcbd-a79af44ddb54
ms.tgt_platform: multiple
keywords:
- Win32_TSDeploymentLicensing de la classe Services Bureau à distance
- Win32_TSDeploymentLicensing de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSDeploymentLicensing
- Win32_TSDeploymentLicensing.Caption
- Win32_TSDeploymentLicensing.Description
- Win32_TSDeploymentLicensing.InstallDate
- Win32_TSDeploymentLicensing.Name
- Win32_TSDeploymentLicensing.Status
- Win32_TSDeploymentLicensing.UseCentralLicensingSettings
- Win32_TSDeploymentLicensing.LicenseServers
- Win32_TSDeploymentLicensing.LicensingType
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 952f58daa8a809e158265aac71b0094c0cd46fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510172"
---
# <a name="win32_tsdeploymentlicensing-class"></a><span data-ttu-id="57097-105">\_Classe TSDeploymentLicensing Win32</span><span class="sxs-lookup"><span data-stu-id="57097-105">Win32\_TSDeploymentLicensing class</span></span>

<span data-ttu-id="57097-106">Paramètres de licence pour le déploiement de la virtualisation de Bureau à distance (RDV).</span><span class="sxs-lookup"><span data-stu-id="57097-106">Licensing Settings for the Remote Desktop Virtualization (RDV) deployment.</span></span>

<span data-ttu-id="57097-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="57097-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="57097-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57097-108">Syntax</span></span>

``` syntax
class Win32_TSDeploymentLicensing : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  UseCentralLicensingSettings;
  String   LicenseServers[];
  uint32   LicensingType;
};
```

## <a name="members"></a><span data-ttu-id="57097-109">Membres</span><span class="sxs-lookup"><span data-stu-id="57097-109">Members</span></span>

<span data-ttu-id="57097-110">La classe **Win32 \_ TSDeploymentLicensing** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="57097-110">The **Win32\_TSDeploymentLicensing** class has these types of members:</span></span>

-   [<span data-ttu-id="57097-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="57097-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57097-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="57097-112">Properties</span></span>

<span data-ttu-id="57097-113">La classe **Win32 \_ TSDeploymentLicensing** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="57097-113">The **Win32\_TSDeploymentLicensing** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="57097-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="57097-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57097-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="57097-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57097-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="57097-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57097-117">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="57097-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="57097-118">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="57097-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="57097-119">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="57097-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="57097-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="57097-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57097-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="57097-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57097-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="57097-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57097-123">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="57097-123">Description of the object.</span></span>

<span data-ttu-id="57097-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="57097-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="57097-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="57097-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57097-126">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="57097-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="57097-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="57097-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57097-128">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="57097-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="57097-129">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="57097-129">The date the object was installed.</span></span> <span data-ttu-id="57097-130">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="57097-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="57097-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="57097-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="57097-132">**LicenseServers**</span><span class="sxs-lookup"><span data-stu-id="57097-132">**LicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57097-133">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="57097-133">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="57097-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="57097-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="57097-135">Spécifie les serveurs de licences à utiliser.</span><span class="sxs-lookup"><span data-stu-id="57097-135">Specifies the license servers to use.</span></span>

</dd> <dt>

<span data-ttu-id="57097-136">**LicensingType**</span><span class="sxs-lookup"><span data-stu-id="57097-136">**LicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57097-137">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57097-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57097-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="57097-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="57097-139">Mode de licence</span><span class="sxs-lookup"><span data-stu-id="57097-139">Licensing Mode</span></span>

<dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span data-ttu-id="57097-140">**Par appareil** (2)</span><span class="sxs-lookup"><span data-stu-id="57097-140">**Per Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="57097-141">**Par utilisateur** (4)</span><span class="sxs-lookup"><span data-stu-id="57097-141">**Per User** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Yet_Configured"></span><span id="not_yet_configured"></span><span id="NOT_YET_CONFIGURED"></span>

<span data-ttu-id="57097-142">**Pas encore configuré** (5)</span><span class="sxs-lookup"><span data-stu-id="57097-142">**Not Yet Configured** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="57097-143">**Nom**</span><span class="sxs-lookup"><span data-stu-id="57097-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57097-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="57097-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57097-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="57097-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57097-146">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="57097-146">The name of the object.</span></span>

<span data-ttu-id="57097-147">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="57097-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="57097-148">**État**</span><span class="sxs-lookup"><span data-stu-id="57097-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57097-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="57097-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57097-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="57097-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57097-151">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="57097-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="57097-152">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="57097-152">Current status of the object.</span></span> <span data-ttu-id="57097-153">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="57097-153">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="57097-154">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="57097-154">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="57097-155">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="57097-155">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="57097-156">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="57097-156">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="57097-157">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="57097-157">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="57097-158">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="57097-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="57097-159">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="57097-159">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="57097-160">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="57097-160">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="57097-161">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="57097-161">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="57097-162">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="57097-162">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="57097-163">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="57097-163">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="57097-164">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="57097-164">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="57097-165">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="57097-165">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="57097-166">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="57097-166">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="57097-167">**UseCentralLicensingSettings**</span><span class="sxs-lookup"><span data-stu-id="57097-167">**UseCentralLicensingSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57097-168">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="57097-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="57097-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="57097-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="57097-170">Spécifie s’il faut utiliser les paramètres de gestion de licences à l’ensemble du déploiement.</span><span class="sxs-lookup"><span data-stu-id="57097-170">Specifies whether to use deployment-wide licensing settings.</span></span> <span data-ttu-id="57097-171">**True** pour utiliser ces paramètres pour tous les serveurs de ce déploiement.</span><span class="sxs-lookup"><span data-stu-id="57097-171">**True** to use these settings for all servers in this deployment.</span></span> <span data-ttu-id="57097-172">**false** pour les définir par serveur.</span><span class="sxs-lookup"><span data-stu-id="57097-172">**false** to set them per-server.</span></span> <span data-ttu-id="57097-173">Si la valeur est **false**, tous les autres paramètres de licence sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="57097-173">If this is set to **false**, all other licensing settings are ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57097-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57097-174">Requirements</span></span>



| <span data-ttu-id="57097-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57097-175">Requirement</span></span> | <span data-ttu-id="57097-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="57097-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57097-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57097-177">Minimum supported client</span></span><br/> | <span data-ttu-id="57097-178">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="57097-178">None supported</span></span><br/>                                                               |
| <span data-ttu-id="57097-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57097-179">Minimum supported server</span></span><br/> | <span data-ttu-id="57097-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="57097-180">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="57097-181">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="57097-181">Namespace</span></span><br/>                | <span data-ttu-id="57097-182">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="57097-182">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="57097-183">MOF</span><span class="sxs-lookup"><span data-stu-id="57097-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57097-184"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57097-184"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="57097-185">DLL</span><span class="sxs-lookup"><span data-stu-id="57097-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57097-186"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57097-186"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

