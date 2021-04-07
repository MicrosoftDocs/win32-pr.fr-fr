---
description: Décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode decompress.
ms.assetid: 383475ba-77d4-4bfb-a241-9c37aa594a1e
ms.tgt_platform: multiple
title: Méthode UncompressEx de la classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c514939425625c15f3b683e4dc10bd5e05cb511
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748933"
---
# <a name="uncompressex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="11922-104">Méthode UncompressEx de la \_ classe CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="11922-104">UncompressEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="11922-105">La méthode **UncompressEx** décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="11922-105">The **UncompressEx** method uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="11922-106">Cette méthode est une version étendue de la méthode [**decompress**](uncompress-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="11922-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11922-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="11922-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="11922-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="11922-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="11922-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="11922-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="11922-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="11922-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="11922-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11922-111">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="11922-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11922-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11922-113">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="11922-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11922-114">Nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="11922-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="11922-115">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="11922-115">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="11922-116">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="11922-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="11922-117">Nom du fichier enfant (ou répertoire) à utiliser comme point de départ de la méthode.</span><span class="sxs-lookup"><span data-stu-id="11922-117">Name of the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="11922-118">En général, ce paramètre est le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="11922-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="11922-119">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="11922-119">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="11922-120">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="11922-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="11922-121">Si la **valeur est true**, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="11922-121">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="11922-122">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="11922-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11922-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="11922-123">Return value</span></span>

<span data-ttu-id="11922-124">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="11922-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="11922-125">**Success**</span><span class="sxs-lookup"><span data-stu-id="11922-125">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="11922-126">0</span><span class="sxs-lookup"><span data-stu-id="11922-126">0</span></span>

<span data-ttu-id="11922-127">Réussite.</span><span class="sxs-lookup"><span data-stu-id="11922-127">Success.</span></span>

</dd> <dt>

<span data-ttu-id="11922-128">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="11922-128">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="11922-129">2</span><span class="sxs-lookup"><span data-stu-id="11922-129">2</span></span>

<span data-ttu-id="11922-130">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="11922-130">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="11922-131">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="11922-131">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="11922-132">8</span><span class="sxs-lookup"><span data-stu-id="11922-132">8</span></span>

<span data-ttu-id="11922-133">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="11922-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="11922-134">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="11922-134">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="11922-135">9</span><span class="sxs-lookup"><span data-stu-id="11922-135">9</span></span>

<span data-ttu-id="11922-136">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="11922-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="11922-137">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="11922-137">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="11922-138">10</span><span class="sxs-lookup"><span data-stu-id="11922-138">10</span></span>

<span data-ttu-id="11922-139">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="11922-139">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="11922-140">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="11922-140">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="11922-141">11</span><span class="sxs-lookup"><span data-stu-id="11922-141">11</span></span>

<span data-ttu-id="11922-142">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="11922-142">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="11922-143">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="11922-143">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="11922-144">12</span><span class="sxs-lookup"><span data-stu-id="11922-144">12</span></span>

<span data-ttu-id="11922-145">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="11922-145">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="11922-146">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="11922-146">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="11922-147">13</span><span class="sxs-lookup"><span data-stu-id="11922-147">13</span></span>

<span data-ttu-id="11922-148">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="11922-148">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="11922-149">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="11922-149">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="11922-150">14</span><span class="sxs-lookup"><span data-stu-id="11922-150">14</span></span>

<span data-ttu-id="11922-151">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="11922-151">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="11922-152">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="11922-152">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="11922-153">15</span><span class="sxs-lookup"><span data-stu-id="11922-153">15</span></span>

<span data-ttu-id="11922-154">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="11922-154">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="11922-155">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="11922-155">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="11922-156">16</span><span class="sxs-lookup"><span data-stu-id="11922-156">16</span></span>

<span data-ttu-id="11922-157">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="11922-157">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="11922-158">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="11922-158">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="11922-159">17</span><span class="sxs-lookup"><span data-stu-id="11922-159">17</span></span>

<span data-ttu-id="11922-160">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="11922-160">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="11922-161">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="11922-161">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="11922-162">21</span><span class="sxs-lookup"><span data-stu-id="11922-162">21</span></span>

<span data-ttu-id="11922-163">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="11922-163">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11922-164">Notes</span><span class="sxs-lookup"><span data-stu-id="11922-164">Remarks</span></span>

<span data-ttu-id="11922-165">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="11922-165">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="11922-166">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="11922-166">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="11922-167">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="11922-167">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="11922-168">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="11922-168">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="11922-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11922-169">Requirements</span></span>



| <span data-ttu-id="11922-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11922-170">Requirement</span></span> | <span data-ttu-id="11922-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="11922-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11922-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11922-172">Minimum supported client</span></span><br/> | <span data-ttu-id="11922-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11922-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="11922-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11922-174">Minimum supported server</span></span><br/> | <span data-ttu-id="11922-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11922-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="11922-176">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="11922-176">Namespace</span></span><br/>                | <span data-ttu-id="11922-177">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="11922-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="11922-178">MOF</span><span class="sxs-lookup"><span data-stu-id="11922-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11922-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11922-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="11922-180">DLL</span><span class="sxs-lookup"><span data-stu-id="11922-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11922-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11922-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11922-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11922-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11922-183">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="11922-183">CIM\_LogicalFile</span></span>](uncompressex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="11922-184">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="11922-184">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

