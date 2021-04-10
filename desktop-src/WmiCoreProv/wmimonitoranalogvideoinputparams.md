---
description: Représente les paramètres d’entrée de vidéo analogique d’un moniteur d’ordinateur.
ms.assetid: 87d4260d-06c7-4a76-a3a1-8f6e51e23d92
title: WmiMonitorAnalogVideoInputParams, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorAnalogVideoInputParams
- WmiMonitorAnalogVideoInputParams.Active
- WmiMonitorAnalogVideoInputParams.CompositeSyncSupported
- WmiMonitorAnalogVideoInputParams.InstanceName
- WmiMonitorAnalogVideoInputParams.SeparateSyncsSupported
- WmiMonitorAnalogVideoInputParams.SerrationOfVsyncRequired
- WmiMonitorAnalogVideoInputParams.SetupExpected
- WmiMonitorAnalogVideoInputParams.SignalLevelStandard
- WmiMonitorAnalogVideoInputParams.SyncOnGreenVideoSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 900bf4353de0c81acb5aa2c69578256b0212a2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952348"
---
# <a name="wmimonitoranalogvideoinputparams-class"></a><span data-ttu-id="153e0-103">WmiMonitorAnalogVideoInputParams, classe</span><span class="sxs-lookup"><span data-stu-id="153e0-103">WmiMonitorAnalogVideoInputParams class</span></span>

<span data-ttu-id="153e0-104">La classe WMI **WmiMonitorAnalogVideoInputParams** représente les paramètres d’entrée de vidéo analogique d’un moniteur d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="153e0-104">The **WmiMonitorAnalogVideoInputParams** WMI class represents the analog video input parameters of a computer monitor.</span></span> <span data-ttu-id="153e0-105">Les données de cette classe correspondent aux données de la définition d’entrée vidéo de la norme E-EDID (Extended Display Identification Data) améliorée de l’Association Video Electronics standard Association (VESA).</span><span class="sxs-lookup"><span data-stu-id="153e0-105">The data in this class corresponds to data in the Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span> <span data-ttu-id="153e0-106">Une instance de cette classe est disponible uniquement lorsque la valeur de la propriété **VideoInputType** de la classe [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) est « Analog ».</span><span class="sxs-lookup"><span data-stu-id="153e0-106">An instance of this class is available only when the value of the **VideoInputType** property of the [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) class is "Analog".</span></span>

## <a name="syntax"></a><span data-ttu-id="153e0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="153e0-107">Syntax</span></span>

``` syntax
class WmiMonitorAnalogVideoInputParams : MSMonitorClass
{
  boolean Active;
  uint8   CompositeSyncSupported;
  string  InstanceName;
  uint8   SeparateSyncsSupported;
  uint8   SerrationOfVsyncRequired;
  uint8   SetupExpected;
  uint8   SignalLevelStandard;
  uint8   SyncOnGreenVideoSupported;
};
```

## <a name="members"></a><span data-ttu-id="153e0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="153e0-108">Members</span></span>

<span data-ttu-id="153e0-109">La classe **WmiMonitorAnalogVideoInputParams** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="153e0-109">The **WmiMonitorAnalogVideoInputParams** class has these types of members:</span></span>

-   [<span data-ttu-id="153e0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="153e0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="153e0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="153e0-111">Properties</span></span>

<span data-ttu-id="153e0-112">La classe **WmiMonitorAnalogVideoInputParams** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="153e0-112">The **WmiMonitorAnalogVideoInputParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="153e0-113">**Actif**</span><span class="sxs-lookup"><span data-stu-id="153e0-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="153e0-114">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="153e0-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="153e0-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="153e0-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="153e0-116">Indique le moniteur actif.</span><span class="sxs-lookup"><span data-stu-id="153e0-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="153e0-117">**CompositeSyncSupported**</span><span class="sxs-lookup"><span data-stu-id="153e0-117">**CompositeSyncSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="153e0-118">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="153e0-118">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="153e0-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="153e0-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="153e0-120">Indique si la synchronisation composite est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="153e0-120">Indicates whether composite sync is supported.</span></span>



| <span data-ttu-id="153e0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="153e0-121">Value</span></span>                                                                              | <span data-ttu-id="153e0-122">Signification</span><span class="sxs-lookup"><span data-stu-id="153e0-122">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="153e0-123"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-123"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="153e0-124">La synchronisation composite sur la ligne de synchronisation horizontale est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="153e0-124">Composite sync on horizontal sync line is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="153e0-125"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-125"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="153e0-126">La synchronisation composite sur la ligne de synchronisation horizontale n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="153e0-126">Composite sync on horizontal sync line is not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="153e0-127">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="153e0-127">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="153e0-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="153e0-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="153e0-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="153e0-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="153e0-130">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="153e0-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="153e0-131">Nom de l’instance d’analyse spécifique.</span><span class="sxs-lookup"><span data-stu-id="153e0-131">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="153e0-132">**SeparateSyncsSupported**</span><span class="sxs-lookup"><span data-stu-id="153e0-132">**SeparateSyncsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="153e0-133">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="153e0-133">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="153e0-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="153e0-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="153e0-135">Indique si les synchronisations distinctes sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="153e0-135">Indicates whether separate syncs are supported.</span></span>



| <span data-ttu-id="153e0-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="153e0-136">Value</span></span>                                                                              | <span data-ttu-id="153e0-137">Signification</span><span class="sxs-lookup"><span data-stu-id="153e0-137">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="153e0-138"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-138"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="153e0-139">Les synchronisations distinctes sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="153e0-139">Separate syncs are supported.</span></span><br/>     |
| <dl> <span data-ttu-id="153e0-140"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-140"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="153e0-141">Les synchronisations distinctes ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="153e0-141">Separate syncs are not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="153e0-142">**SerrationOfVsyncRequired**</span><span class="sxs-lookup"><span data-stu-id="153e0-142">**SerrationOfVsyncRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="153e0-143">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="153e0-143">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="153e0-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="153e0-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="153e0-145">Indique si l’impulsion de synchronisation verticale serration est requise.</span><span class="sxs-lookup"><span data-stu-id="153e0-145">Indicates whether vertical sync pulse serration is required.</span></span>



| <span data-ttu-id="153e0-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="153e0-146">Value</span></span>                                                                              | <span data-ttu-id="153e0-147">Signification</span><span class="sxs-lookup"><span data-stu-id="153e0-147">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="153e0-148"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-148"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="153e0-149">Serration de l’impulsion de synchronisation verticale est nécessaire lors de l’utilisation d’une synchronisation composite ou d’une vidéo en vert.</span><span class="sxs-lookup"><span data-stu-id="153e0-149">Serration of the vertical sync pulse is required when composite sync or sync-on-green video is used.</span></span><br/>     |
| <dl> <span data-ttu-id="153e0-150"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-150"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="153e0-151">Le serration de l’impulsion de synchronisation verticale n’est pas requis lorsque la synchronisation composite ou la vidéo de synchronisation en vert est utilisée.</span><span class="sxs-lookup"><span data-stu-id="153e0-151">Serration of the vertical sync pulse is not required when composite sync or sync-on-green video is used.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="153e0-152">**SetupExpected**</span><span class="sxs-lookup"><span data-stu-id="153e0-152">**SetupExpected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="153e0-153">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="153e0-153">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="153e0-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="153e0-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="153e0-155">Indique si l’installation est attendue.</span><span class="sxs-lookup"><span data-stu-id="153e0-155">Indicates whether setup is expected.</span></span>



| <span data-ttu-id="153e0-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="153e0-156">Value</span></span>                                                                              | <span data-ttu-id="153e0-157">Signification</span><span class="sxs-lookup"><span data-stu-id="153e0-157">Meaning</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="153e0-158"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-158"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="153e0-159">Le moniteur attend une installation vide ou un socle pour chaque niveau de signal approprié.</span><span class="sxs-lookup"><span data-stu-id="153e0-159">Monitor expects a blank-to-blank setup or pedestal per appropriate Signal Level Standard.</span></span><br/>                      |
| <dl> <span data-ttu-id="153e0-160"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-160"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="153e0-161">Le moniteur ne s’attend pas à une installation vide ou à un socle en fonction de la norme de niveau de signal appropriée.</span><span class="sxs-lookup"><span data-stu-id="153e0-161">Monitor does not expect a blank-to-blank setup or pedestal according to the appropriate signal level standard.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="153e0-162">**SignalLevelStandard**</span><span class="sxs-lookup"><span data-stu-id="153e0-162">**SignalLevelStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="153e0-163">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="153e0-163">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="153e0-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="153e0-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="153e0-165">Norme de niveau de signal pour les connexions EVC (Enhanced Video Connector).</span><span class="sxs-lookup"><span data-stu-id="153e0-165">Signal level standard for Enhanced video connector (EVC) connections.</span></span>



| <span data-ttu-id="153e0-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="153e0-166">Value</span></span>                                                                              | <span data-ttu-id="153e0-167">Signification</span><span class="sxs-lookup"><span data-stu-id="153e0-167">Meaning</span></span>                     |
|------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="153e0-168"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-168"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="153e0-169">0,7, 0.3 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="153e0-169">0.7,0.3\[V\]</span></span><br/>     |
| <dl> <span data-ttu-id="153e0-170"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-170"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="153e0-171">0.714, 0.286 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="153e0-171">0.714,0.286\[V\]</span></span><br/> |
| <dl> <span data-ttu-id="153e0-172"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-172"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="153e0-173">1,0, 0,4 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="153e0-173">1.0,0.4\[V\]</span></span><br/>     |
| <dl> <span data-ttu-id="153e0-174"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-174"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="153e0-175">0,7, 0.0 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="153e0-175">0.7,0.0\[V\]</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="153e0-176">**SyncOnGreenVideoSupported**</span><span class="sxs-lookup"><span data-stu-id="153e0-176">**SyncOnGreenVideoSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="153e0-177">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="153e0-177">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="153e0-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="153e0-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="153e0-179">Indique si la synchronisation sur le vert est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="153e0-179">Indicates whether sync on green is supported.</span></span>



| <span data-ttu-id="153e0-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="153e0-180">Value</span></span>                                                                              | <span data-ttu-id="153e0-181">Signification</span><span class="sxs-lookup"><span data-stu-id="153e0-181">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="153e0-182"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-182"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="153e0-183">La synchronisation sur Green Video est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="153e0-183">Sync on green video is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="153e0-184"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-184"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="153e0-185">La synchronisation sur une vidéo verte n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="153e0-185">Sync on green video is not supported.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="153e0-186">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="153e0-186">Requirements</span></span>



| <span data-ttu-id="153e0-187">Condition requise</span><span class="sxs-lookup"><span data-stu-id="153e0-187">Requirement</span></span> | <span data-ttu-id="153e0-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="153e0-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="153e0-189">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="153e0-189">Minimum supported client</span></span><br/> | <span data-ttu-id="153e0-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="153e0-190">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="153e0-191">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="153e0-191">Minimum supported server</span></span><br/> | <span data-ttu-id="153e0-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="153e0-192">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="153e0-193">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="153e0-193">Namespace</span></span><br/>                | <span data-ttu-id="153e0-194">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="153e0-194">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="153e0-195">MOF</span><span class="sxs-lookup"><span data-stu-id="153e0-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="153e0-196"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-196"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="153e0-197">DLL</span><span class="sxs-lookup"><span data-stu-id="153e0-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="153e0-198"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="153e0-198"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="153e0-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="153e0-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="153e0-200">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="153e0-200">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




