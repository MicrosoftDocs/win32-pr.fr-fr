---
description: Représente les informations d’identification relatives à un moniteur vidéo, telles que le nom du fabricant, l’année de fabrication ou le numéro de série.
ms.assetid: 85c8c4b1-20e2-4c0b-9209-a3724509a2f0
title: WmiMonitorID, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorID
- WmiMonitorID.Active
- WmiMonitorID.InstanceName
- WmiMonitorID.ManufacturerName
- WmiMonitorID.ManufacturerNameLength
- WmiMonitorID.ProductCodeID
- WmiMonitorID.SerialNumberID
- WmiMonitorID.WeekOfManufacture
- WmiMonitorID.YearOfManufacture
- WmiMonitorID.UserFriendlyName
- WmiMonitorID.UserFriendlyNameLength
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.custom: project-verbatim
ms.openlocfilehash: 485b42a86ca67d15ec00be13992c17b31ed51608
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "106538565"
---
# <a name="wmimonitorid-class"></a><span data-ttu-id="d8344-103">WmiMonitorID, classe</span><span class="sxs-lookup"><span data-stu-id="d8344-103">WmiMonitorID class</span></span>

<span data-ttu-id="d8344-104">La classe WMI **WmiMonitorID** représente les informations d’identification d’un moniteur vidéo, telles que le nom du fabricant, l’année de fabrication ou le numéro de série.</span><span class="sxs-lookup"><span data-stu-id="d8344-104">The **WmiMonitorID** WMI class represents the identifying information about a video monitor, such as manufacturer name, year of manufacture, or serial number.</span></span> <span data-ttu-id="d8344-105">Les données de cette classe correspondent aux données dans le bloc d’identification du fournisseur ou du produit de la définition d’entrée vidéo de la norme VESA (Video Electronics standard Association) Enhanced Display Identification Data (E-EDID) améliorée.</span><span class="sxs-lookup"><span data-stu-id="d8344-105">The data in this class correspond to data in the Vendor/Product Identification block of Video Input Definition of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8344-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8344-106">Syntax</span></span>

``` syntax
class WmiMonitorID : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint16  ManufacturerName[];
  uint16  ManufacturerNameLength;
  uint16  ProductCodeID[];
  uint16  SerialNumberID[];
  uint8   WeekOfManufacture;
  uint16  YearOfManufacture;
  uint16  UserFriendlyName[];
  uint16  UserFriendlyNameLength;
};
```

## <a name="members"></a><span data-ttu-id="d8344-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d8344-107">Members</span></span>

<span data-ttu-id="d8344-108">La classe **WmiMonitorID** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d8344-108">The **WmiMonitorID** class has these types of members:</span></span>

-   [<span data-ttu-id="d8344-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8344-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8344-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8344-110">Properties</span></span>

<span data-ttu-id="d8344-111">La classe **WmiMonitorID** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d8344-111">The **WmiMonitorID** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8344-112">**Actif**</span><span class="sxs-lookup"><span data-stu-id="d8344-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8344-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d8344-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8344-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8344-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8344-115">Indique le moniteur actif.</span><span class="sxs-lookup"><span data-stu-id="d8344-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="d8344-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="d8344-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8344-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8344-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8344-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8344-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8344-119">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="d8344-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d8344-120">Nom de l’instance d’analyse spécifique.</span><span class="sxs-lookup"><span data-stu-id="d8344-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="d8344-121">**ManufacturerName**</span><span class="sxs-lookup"><span data-stu-id="d8344-121">**ManufacturerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8344-122">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8344-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d8344-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8344-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8344-124">Nom du fabricant.</span><span class="sxs-lookup"><span data-stu-id="d8344-124">Name of manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="d8344-125">**ManufacturerNameLength**</span><span class="sxs-lookup"><span data-stu-id="d8344-125">**ManufacturerNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8344-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8344-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8344-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8344-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8344-128">Longueur du nom de fabricant située dans la propriété **ManufacturerName** .</span><span class="sxs-lookup"><span data-stu-id="d8344-128">Length of manufacturer name located in the **ManufacturerName** property.</span></span>

</dd> <dt>

<span data-ttu-id="d8344-129">**ProductCodeID**</span><span class="sxs-lookup"><span data-stu-id="d8344-129">**ProductCodeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8344-130">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8344-130">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d8344-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8344-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8344-132">ID de code de produit attribué par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d8344-132">Vendor assigned product code ID.</span></span>

</dd> <dt>

<span data-ttu-id="d8344-133">**SerialNumberID**</span><span class="sxs-lookup"><span data-stu-id="d8344-133">**SerialNumberID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8344-134">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8344-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d8344-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8344-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8344-136">Numéro de série.</span><span class="sxs-lookup"><span data-stu-id="d8344-136">Serial number.</span></span>

</dd> <dt>

<span data-ttu-id="d8344-137">UserFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d8344-137">UserFriendlyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8344-138">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8344-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d8344-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8344-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8344-140">Nom convivial de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="d8344-140">The friendly name of the monitor.</span></span> <span data-ttu-id="d8344-141">La taille du nom est la longueur spécifiée par la propriété UserFriendlyNameLength.</span><span class="sxs-lookup"><span data-stu-id="d8344-141">The size of the name is the length specified by the UserFriendlyNameLength property.</span></span>

</dd> <dt>

<span data-ttu-id="d8344-142">UserFriendlyNameLength</span><span class="sxs-lookup"><span data-stu-id="d8344-142">UserFriendlyNameLength</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8344-143">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8344-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8344-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8344-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8344-145">Nombre de caractères dans le nom situé dans la propriété UserFriendlyName.</span><span class="sxs-lookup"><span data-stu-id="d8344-145">Number of characters in the name located in the UserFriendlyName property.</span></span>

</dd> <dt>

<span data-ttu-id="d8344-146">**WeekOfManufacture**</span><span class="sxs-lookup"><span data-stu-id="d8344-146">**WeekOfManufacture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8344-147">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d8344-147">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d8344-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8344-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8344-149">Semaine de fabrication par numéro de semaine.</span><span class="sxs-lookup"><span data-stu-id="d8344-149">Week of manufacture by week number.</span></span> <span data-ttu-id="d8344-150">La plage est comprise entre 1 et 53.</span><span class="sxs-lookup"><span data-stu-id="d8344-150">The range is from 1 through 53.</span></span> <span data-ttu-id="d8344-151">Zéro (0) n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="d8344-151">Zero (0) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="d8344-152">**YearOfManufacture**</span><span class="sxs-lookup"><span data-stu-id="d8344-152">**YearOfManufacture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8344-153">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8344-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8344-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8344-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8344-155">Année de fabrication.</span><span class="sxs-lookup"><span data-stu-id="d8344-155">Year of manufacture.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8344-156">Notes</span><span class="sxs-lookup"><span data-stu-id="d8344-156">Remarks</span></span>

<span data-ttu-id="d8344-157">Pour plus d’informations sur la façon de traduire les tableaux qui stockent des ID de numéro de série, consultez l’article [informations sur le moniteur de rapports avec Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) .</span><span class="sxs-lookup"><span data-stu-id="d8344-157">For a discussion on how to translate the arrays that store serial number ID's, see the [Reporting Monitor information with Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) blog article.</span></span>

## <a name="examples"></a><span data-ttu-id="d8344-158">Exemples</span><span class="sxs-lookup"><span data-stu-id="d8344-158">Examples</span></span>

<span data-ttu-id="d8344-159">L’exemple PowerShell suivant récupère le numéro de série de plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="d8344-159">The following PowerShell example retrieves the serial number of multiple monitors.</span></span>


```PowerShell
gwmi WmiMonitorID -Namespace root\wmi | ForEach-Object {($_.UserFriendlyName -ne 0 | foreach {[char]$_}) -join ""; ($_.SerialNumberID -ne 0 | foreach {[char]$_}) -join ""}
```



<span data-ttu-id="d8344-160">Le code VBScript suivant récupère également les informations d’ID d’analyse à partir d’un système.</span><span class="sxs-lookup"><span data-stu-id="d8344-160">The following VBScript code also retrieves monitor ID information from a system.</span></span>


```VB
Option Explicit

Dim strComputer, objWMIService, colItems, objItem

strComputer = "MyComputer"

Set objWMIService = GetObject("winmgmts:" _ 
  & "{impersonationLevel=impersonate,authenticationLevel=Pkt}!\\" _ 
  & strComputer & "\root\wmi") 

Set colItems = objWMIService.ExecQuery _
  ("SELECT * FROM WMIMonitorID")

For Each objItem In colItems
  Wscript.Echo objItem.InstanceName
Next
```



## <a name="requirements"></a><span data-ttu-id="d8344-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8344-161">Requirements</span></span>



| <span data-ttu-id="d8344-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8344-162">Requirement</span></span> | <span data-ttu-id="d8344-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8344-163">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8344-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8344-164">Minimum supported client</span></span><br/> | <span data-ttu-id="d8344-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8344-165">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d8344-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8344-166">Minimum supported server</span></span><br/> | <span data-ttu-id="d8344-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8344-167">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d8344-168">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d8344-168">Namespace</span></span><br/>                | <span data-ttu-id="d8344-169">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="d8344-169">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="d8344-170">MOF</span><span class="sxs-lookup"><span data-stu-id="d8344-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8344-171"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8344-171"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8344-172">DLL</span><span class="sxs-lookup"><span data-stu-id="d8344-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8344-173"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8344-173"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8344-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8344-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8344-175">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="d8344-175">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

