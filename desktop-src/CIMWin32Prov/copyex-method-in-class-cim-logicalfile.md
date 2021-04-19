---
description: Copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre FileName.
ms.assetid: 534d8b73-fc22-4a42-b8e6-24a54353bb14
ms.tgt_platform: multiple
title: Méthode CopyEx de la classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ec7c44ec3fc01074a0f4af70249236aa366d64bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516799"
---
# <a name="copyex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="2249e-103">Méthode CopyEx de la \_ classe CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="2249e-103">CopyEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="2249e-104">La méthode **CopyEx** copie le fichier logique (ou le répertoire) spécifié dans le chemin de l’objet vers l’emplacement spécifié par le paramètre *filename* .</span><span class="sxs-lookup"><span data-stu-id="2249e-104">The **CopyEx** method copies the logical file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="2249e-105">Une copie n’est pas prise en charge si le remplacement d’un fichier logique existant est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2249e-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="2249e-106">Cette méthode est une version étendue de la méthode de [**copie**](copy-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="2249e-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2249e-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="2249e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2249e-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2249e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2249e-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="2249e-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2249e-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2249e-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2249e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2249e-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="2249e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2249e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2249e-113">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2249e-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2249e-114">Nom complet du fichier de destination (ou répertoire).</span><span class="sxs-lookup"><span data-stu-id="2249e-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="2249e-115">Exemple : « c : \\ temp \\ newDirectory »</span><span class="sxs-lookup"><span data-stu-id="2249e-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="2249e-116">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2249e-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2249e-117">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="2249e-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="2249e-118">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="2249e-118">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="2249e-119">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="2249e-119">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2249e-120">Chaîne qui nomme le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2249e-120">String that names the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="2249e-121">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier (ou le répertoire) auquel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="2249e-121">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="2249e-122">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="2249e-122">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="2249e-123">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="2249e-123">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2249e-124">Si la valeur est TRUE, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="2249e-124">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="2249e-125">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="2249e-125">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2249e-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2249e-126">Return value</span></span>

<span data-ttu-id="2249e-127">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="2249e-127">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="2249e-128">**Success**</span><span class="sxs-lookup"><span data-stu-id="2249e-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="2249e-129">0</span><span class="sxs-lookup"><span data-stu-id="2249e-129">0</span></span>

<span data-ttu-id="2249e-130">Réussite.</span><span class="sxs-lookup"><span data-stu-id="2249e-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="2249e-131">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="2249e-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="2249e-132">2</span><span class="sxs-lookup"><span data-stu-id="2249e-132">2</span></span>

<span data-ttu-id="2249e-133">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="2249e-133">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2249e-134">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="2249e-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="2249e-135">8</span><span class="sxs-lookup"><span data-stu-id="2249e-135">8</span></span>

<span data-ttu-id="2249e-136">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="2249e-136">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="2249e-137">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="2249e-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="2249e-138">9</span><span class="sxs-lookup"><span data-stu-id="2249e-138">9</span></span>

<span data-ttu-id="2249e-139">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="2249e-139">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="2249e-140">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="2249e-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="2249e-141">10</span><span class="sxs-lookup"><span data-stu-id="2249e-141">10</span></span>

<span data-ttu-id="2249e-142">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="2249e-142">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2249e-143">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="2249e-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="2249e-144">11</span><span class="sxs-lookup"><span data-stu-id="2249e-144">11</span></span>

<span data-ttu-id="2249e-145">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="2249e-145">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="2249e-146">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="2249e-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="2249e-147">12</span><span class="sxs-lookup"><span data-stu-id="2249e-147">12</span></span>

<span data-ttu-id="2249e-148">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="2249e-148">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="2249e-149">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="2249e-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="2249e-150">13</span><span class="sxs-lookup"><span data-stu-id="2249e-150">13</span></span>

<span data-ttu-id="2249e-151">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="2249e-151">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2249e-152">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="2249e-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="2249e-153">14</span><span class="sxs-lookup"><span data-stu-id="2249e-153">14</span></span>

<span data-ttu-id="2249e-154">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="2249e-154">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2249e-155">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="2249e-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="2249e-156">15</span><span class="sxs-lookup"><span data-stu-id="2249e-156">15</span></span>

<span data-ttu-id="2249e-157">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="2249e-157">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2249e-158">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="2249e-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="2249e-159">16</span><span class="sxs-lookup"><span data-stu-id="2249e-159">16</span></span>

<span data-ttu-id="2249e-160">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="2249e-160">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="2249e-161">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="2249e-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="2249e-162">17</span><span class="sxs-lookup"><span data-stu-id="2249e-162">17</span></span>

<span data-ttu-id="2249e-163">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="2249e-163">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="2249e-164">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="2249e-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2249e-165">21</span><span class="sxs-lookup"><span data-stu-id="2249e-165">21</span></span>

<span data-ttu-id="2249e-166">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="2249e-166">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2249e-167">Notes</span><span class="sxs-lookup"><span data-stu-id="2249e-167">Remarks</span></span>

<span data-ttu-id="2249e-168">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="2249e-168">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="2249e-169">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2249e-169">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="2249e-170">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="2249e-170">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2249e-171">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2249e-171">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2249e-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2249e-172">Requirements</span></span>



| <span data-ttu-id="2249e-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2249e-173">Requirement</span></span> | <span data-ttu-id="2249e-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="2249e-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2249e-175">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2249e-175">Minimum supported client</span></span><br/> | <span data-ttu-id="2249e-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2249e-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2249e-177">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2249e-177">Minimum supported server</span></span><br/> | <span data-ttu-id="2249e-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2249e-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2249e-179">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2249e-179">Namespace</span></span><br/>                | <span data-ttu-id="2249e-180">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2249e-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2249e-181">MOF</span><span class="sxs-lookup"><span data-stu-id="2249e-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2249e-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2249e-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2249e-183">DLL</span><span class="sxs-lookup"><span data-stu-id="2249e-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2249e-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2249e-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2249e-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2249e-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2249e-186">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="2249e-186">CIM\_LogicalFile</span></span>](copyex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="2249e-187">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="2249e-187">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

