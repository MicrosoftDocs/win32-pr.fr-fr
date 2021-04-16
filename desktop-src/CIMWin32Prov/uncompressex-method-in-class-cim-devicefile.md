---
description: Décompresse le fichier d’unité logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode decompress. Cette méthode est héritée de la \_ LOGICALFILE CIM.
ms.assetid: dfa53b75-56ef-4119-83b9-08b4371762c6
ms.tgt_platform: multiple
title: Méthode UncompressEx de la classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a760c31a2067c294ffb43064402ac179c5fba7c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524127"
---
# <a name="uncompressex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="75dc8-105">Méthode UncompressEx de la \_ classe CIM DeviceFile</span><span class="sxs-lookup"><span data-stu-id="75dc8-105">UncompressEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="75dc8-106">La méthode **UncompressEx** décompresse le fichier d’unité logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="75dc8-106">The **UncompressEx** method uncompresses the logical device file (or directory) specified in the object path.</span></span> <span data-ttu-id="75dc8-107">Cette méthode est une version étendue de la méthode [**decompress**](uncompress-method-in-class-cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="75dc8-107">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-devicefile.md) method.</span></span> <span data-ttu-id="75dc8-108">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="75dc8-108">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75dc8-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="75dc8-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="75dc8-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="75dc8-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="75dc8-111">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="75dc8-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="75dc8-112">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="75dc8-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="75dc8-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75dc8-113">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="75dc8-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75dc8-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75dc8-115">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="75dc8-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75dc8-116">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="75dc8-116">String that represent the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="75dc8-117">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="75dc8-117">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="75dc8-118">*StartFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75dc8-118">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75dc8-119">Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ de la méthode.</span><span class="sxs-lookup"><span data-stu-id="75dc8-119">String that represents the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="75dc8-120">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="75dc8-120">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="75dc8-121">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="75dc8-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="75dc8-122">*Récursif* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75dc8-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75dc8-123">Si la **valeur est true**, cette méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ DeviceFile**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="75dc8-123">If **TRUE**, this method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="75dc8-124">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="75dc8-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75dc8-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75dc8-125">Return value</span></span>

<span data-ttu-id="75dc8-126">Retourne la valeur 0 en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="75dc8-126">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="75dc8-127">0</span><span class="sxs-lookup"><span data-stu-id="75dc8-127">0</span></span>

<span data-ttu-id="75dc8-128">Réussite.</span><span class="sxs-lookup"><span data-stu-id="75dc8-128">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="75dc8-129">2</span><span class="sxs-lookup"><span data-stu-id="75dc8-129">2</span></span>

<span data-ttu-id="75dc8-130">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="75dc8-130">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="75dc8-131">8</span><span class="sxs-lookup"><span data-stu-id="75dc8-131">8</span></span>

<span data-ttu-id="75dc8-132">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="75dc8-132">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="75dc8-133">9</span><span class="sxs-lookup"><span data-stu-id="75dc8-133">9</span></span>

<span data-ttu-id="75dc8-134">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="75dc8-134">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="75dc8-135">10</span><span class="sxs-lookup"><span data-stu-id="75dc8-135">10</span></span>

<span data-ttu-id="75dc8-136">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="75dc8-136">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="75dc8-137">11</span><span class="sxs-lookup"><span data-stu-id="75dc8-137">11</span></span>

<span data-ttu-id="75dc8-138">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="75dc8-138">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="75dc8-139">12</span><span class="sxs-lookup"><span data-stu-id="75dc8-139">12</span></span>

<span data-ttu-id="75dc8-140">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="75dc8-140">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="75dc8-141">13</span><span class="sxs-lookup"><span data-stu-id="75dc8-141">13</span></span>

<span data-ttu-id="75dc8-142">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="75dc8-142">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="75dc8-143">14</span><span class="sxs-lookup"><span data-stu-id="75dc8-143">14</span></span>

<span data-ttu-id="75dc8-144">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="75dc8-144">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="75dc8-145">15</span><span class="sxs-lookup"><span data-stu-id="75dc8-145">15</span></span>

<span data-ttu-id="75dc8-146">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="75dc8-146">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="75dc8-147">16</span><span class="sxs-lookup"><span data-stu-id="75dc8-147">16</span></span>

<span data-ttu-id="75dc8-148">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="75dc8-148">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="75dc8-149">17</span><span class="sxs-lookup"><span data-stu-id="75dc8-149">17</span></span>

<span data-ttu-id="75dc8-150">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="75dc8-150">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="75dc8-151">21</span><span class="sxs-lookup"><span data-stu-id="75dc8-151">21</span></span>

<span data-ttu-id="75dc8-152">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="75dc8-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75dc8-153">Notes</span><span class="sxs-lookup"><span data-stu-id="75dc8-153">Remarks</span></span>

<span data-ttu-id="75dc8-154">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="75dc8-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="75dc8-155">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="75dc8-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="75dc8-156">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="75dc8-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="75dc8-157">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="75dc8-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="75dc8-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75dc8-158">Requirements</span></span>



| <span data-ttu-id="75dc8-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75dc8-159">Requirement</span></span> | <span data-ttu-id="75dc8-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="75dc8-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75dc8-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75dc8-161">Minimum supported client</span></span><br/> | <span data-ttu-id="75dc8-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75dc8-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75dc8-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75dc8-163">Minimum supported server</span></span><br/> | <span data-ttu-id="75dc8-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75dc8-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75dc8-165">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="75dc8-165">Namespace</span></span><br/>                | <span data-ttu-id="75dc8-166">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="75dc8-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="75dc8-167">MOF</span><span class="sxs-lookup"><span data-stu-id="75dc8-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75dc8-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75dc8-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="75dc8-169">DLL</span><span class="sxs-lookup"><span data-stu-id="75dc8-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75dc8-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75dc8-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75dc8-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75dc8-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75dc8-172">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="75dc8-172">CIM\_DeviceFile</span></span>](uncompressex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="75dc8-173">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="75dc8-173">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

