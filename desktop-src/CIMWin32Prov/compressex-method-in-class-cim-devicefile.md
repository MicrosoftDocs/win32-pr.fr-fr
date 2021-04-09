---
description: La méthode CompressEx compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode Compress. Cette méthode est héritée de la \_ LOGICALFILE CIM.
ms.assetid: a5f7b35b-5d52-4129-bf7e-6db5e0ff6852
ms.tgt_platform: multiple
title: Méthode CompressEx de la classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e607497a8bb49d0a5926e5b50eb3310c671d9f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860714"
---
# <a name="compressex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="79a11-105">Méthode CompressEx de la \_ classe CIM DeviceFile</span><span class="sxs-lookup"><span data-stu-id="79a11-105">CompressEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="79a11-106">La méthode **CompressEx** compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="79a11-106">The **CompressEx** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="79a11-107">Cette méthode est une version étendue de la méthode [**Compress**](compress-method-in-class-cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="79a11-107">This method is an extended version of the [**Compress**](compress-method-in-class-cim-devicefile.md) method.</span></span> <span data-ttu-id="79a11-108">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="79a11-108">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="79a11-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="79a11-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="79a11-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="79a11-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="79a11-111">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="79a11-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="79a11-112">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="79a11-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="79a11-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79a11-113">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="79a11-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79a11-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79a11-115">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="79a11-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79a11-116">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="79a11-116">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="79a11-117">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="79a11-117">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="79a11-118">*StartFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79a11-118">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79a11-119">Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="79a11-119">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="79a11-120">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier (ou le répertoire) auquel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="79a11-120">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="79a11-121">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier (ou le répertoire) spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="79a11-121">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="79a11-122">*Récursif* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79a11-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79a11-123">Si la **valeur est true**, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ DeviceFile**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="79a11-123">If **TRUE**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="79a11-124">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="79a11-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79a11-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79a11-125">Return value</span></span>

<span data-ttu-id="79a11-126">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="79a11-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="79a11-127">0</span><span class="sxs-lookup"><span data-stu-id="79a11-127">0</span></span>

<span data-ttu-id="79a11-128">Réussite.</span><span class="sxs-lookup"><span data-stu-id="79a11-128">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="79a11-129">2</span><span class="sxs-lookup"><span data-stu-id="79a11-129">2</span></span>

<span data-ttu-id="79a11-130">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="79a11-130">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="79a11-131">8</span><span class="sxs-lookup"><span data-stu-id="79a11-131">8</span></span>

<span data-ttu-id="79a11-132">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="79a11-132">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="79a11-133">9</span><span class="sxs-lookup"><span data-stu-id="79a11-133">9</span></span>

<span data-ttu-id="79a11-134">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="79a11-134">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="79a11-135">10</span><span class="sxs-lookup"><span data-stu-id="79a11-135">10</span></span>

<span data-ttu-id="79a11-136">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="79a11-136">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="79a11-137">11</span><span class="sxs-lookup"><span data-stu-id="79a11-137">11</span></span>

<span data-ttu-id="79a11-138">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="79a11-138">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="79a11-139">12</span><span class="sxs-lookup"><span data-stu-id="79a11-139">12</span></span>

<span data-ttu-id="79a11-140">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="79a11-140">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="79a11-141">13</span><span class="sxs-lookup"><span data-stu-id="79a11-141">13</span></span>

<span data-ttu-id="79a11-142">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="79a11-142">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="79a11-143">14</span><span class="sxs-lookup"><span data-stu-id="79a11-143">14</span></span>

<span data-ttu-id="79a11-144">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="79a11-144">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="79a11-145">15</span><span class="sxs-lookup"><span data-stu-id="79a11-145">15</span></span>

<span data-ttu-id="79a11-146">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="79a11-146">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="79a11-147">16</span><span class="sxs-lookup"><span data-stu-id="79a11-147">16</span></span>

<span data-ttu-id="79a11-148">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="79a11-148">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="79a11-149">17</span><span class="sxs-lookup"><span data-stu-id="79a11-149">17</span></span>

<span data-ttu-id="79a11-150">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="79a11-150">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="79a11-151">21</span><span class="sxs-lookup"><span data-stu-id="79a11-151">21</span></span>

<span data-ttu-id="79a11-152">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="79a11-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79a11-153">Notes</span><span class="sxs-lookup"><span data-stu-id="79a11-153">Remarks</span></span>

<span data-ttu-id="79a11-154">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="79a11-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="79a11-155">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="79a11-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="79a11-156">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="79a11-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="79a11-157">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="79a11-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="79a11-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79a11-158">Requirements</span></span>



| <span data-ttu-id="79a11-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79a11-159">Requirement</span></span> | <span data-ttu-id="79a11-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="79a11-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79a11-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79a11-161">Minimum supported client</span></span><br/> | <span data-ttu-id="79a11-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79a11-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79a11-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79a11-163">Minimum supported server</span></span><br/> | <span data-ttu-id="79a11-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79a11-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79a11-165">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="79a11-165">Namespace</span></span><br/>                | <span data-ttu-id="79a11-166">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="79a11-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="79a11-167">MOF</span><span class="sxs-lookup"><span data-stu-id="79a11-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79a11-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79a11-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="79a11-169">DLL</span><span class="sxs-lookup"><span data-stu-id="79a11-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79a11-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79a11-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79a11-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79a11-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79a11-172">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="79a11-172">CIM\_DeviceFile</span></span>](compressex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="79a11-173">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="79a11-173">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

