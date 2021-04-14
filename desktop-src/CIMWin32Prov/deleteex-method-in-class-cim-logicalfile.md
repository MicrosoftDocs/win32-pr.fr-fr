---
description: La méthode DeleteEx supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode Delete.
ms.assetid: 53785f2e-8796-446c-8228-9abc2d9a0d68
ms.tgt_platform: multiple
title: Méthode DeleteEx de la classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4f9799513111ff53bb97c14feaf70c922dfb085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523399"
---
# <a name="deleteex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="0bf9c-104">Méthode DeleteEx de la \_ classe CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="0bf9c-104">DeleteEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="0bf9c-105">La méthode **DeleteEx** supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="0bf9c-106">Cette méthode est une version étendue de la méthode [**Delete**](delete-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="0bf9c-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0bf9c-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0bf9c-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0bf9c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0bf9c-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="0bf9c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0bf9c-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0bf9c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0bf9c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bf9c-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="0bf9c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0bf9c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bf9c-113">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0bf9c-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf9c-114">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="0bf9c-115">Ce paramètre a la valeur null si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0bf9c-116">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0bf9c-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf9c-117">Chaîne qui nomme le fichier enfant (ou le répertoire) à utiliser comme point de départ de la méthode.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-117">String that names the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="0bf9c-118">En général, ce paramètre est le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="0bf9c-119">Si ce paramètre a la valeur null, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="0bf9c-119">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bf9c-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0bf9c-120">Return value</span></span>

<span data-ttu-id="0bf9c-121">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0bf9c-122">**Success**</span><span class="sxs-lookup"><span data-stu-id="0bf9c-122">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="0bf9c-123">0</span><span class="sxs-lookup"><span data-stu-id="0bf9c-123">0</span></span>

<span data-ttu-id="0bf9c-124">Réussite.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-124">Success.</span></span>

</dd> <dt>

<span data-ttu-id="0bf9c-125">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="0bf9c-125">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="0bf9c-126">2</span><span class="sxs-lookup"><span data-stu-id="0bf9c-126">2</span></span>

<span data-ttu-id="0bf9c-127">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-127">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="0bf9c-128">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="0bf9c-128">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="0bf9c-129">8</span><span class="sxs-lookup"><span data-stu-id="0bf9c-129">8</span></span>

<span data-ttu-id="0bf9c-130">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-130">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="0bf9c-131">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="0bf9c-131">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="0bf9c-132">9</span><span class="sxs-lookup"><span data-stu-id="0bf9c-132">9</span></span>

<span data-ttu-id="0bf9c-133">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-133">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="0bf9c-134">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="0bf9c-134">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="0bf9c-135">10</span><span class="sxs-lookup"><span data-stu-id="0bf9c-135">10</span></span>

<span data-ttu-id="0bf9c-136">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-136">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0bf9c-137">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="0bf9c-137">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="0bf9c-138">11</span><span class="sxs-lookup"><span data-stu-id="0bf9c-138">11</span></span>

<span data-ttu-id="0bf9c-139">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-139">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0bf9c-140">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="0bf9c-140">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="0bf9c-141">12</span><span class="sxs-lookup"><span data-stu-id="0bf9c-141">12</span></span>

<span data-ttu-id="0bf9c-142">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0bf9c-143">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="0bf9c-143">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="0bf9c-144">13</span><span class="sxs-lookup"><span data-stu-id="0bf9c-144">13</span></span>

<span data-ttu-id="0bf9c-145">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-145">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0bf9c-146">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="0bf9c-146">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="0bf9c-147">14</span><span class="sxs-lookup"><span data-stu-id="0bf9c-147">14</span></span>

<span data-ttu-id="0bf9c-148">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-148">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0bf9c-149">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="0bf9c-149">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="0bf9c-150">15</span><span class="sxs-lookup"><span data-stu-id="0bf9c-150">15</span></span>

<span data-ttu-id="0bf9c-151">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-151">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0bf9c-152">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="0bf9c-152">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="0bf9c-153">16</span><span class="sxs-lookup"><span data-stu-id="0bf9c-153">16</span></span>

<span data-ttu-id="0bf9c-154">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-154">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="0bf9c-155">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="0bf9c-155">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="0bf9c-156">17</span><span class="sxs-lookup"><span data-stu-id="0bf9c-156">17</span></span>

<span data-ttu-id="0bf9c-157">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-157">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="0bf9c-158">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="0bf9c-158">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0bf9c-159">21</span><span class="sxs-lookup"><span data-stu-id="0bf9c-159">21</span></span>

<span data-ttu-id="0bf9c-160">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-160">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0bf9c-161">Notes</span><span class="sxs-lookup"><span data-stu-id="0bf9c-161">Remarks</span></span>

<span data-ttu-id="0bf9c-162">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-162">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0bf9c-163">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-163">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0bf9c-164">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-164">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0bf9c-165">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0bf9c-165">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bf9c-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bf9c-166">Requirements</span></span>



| <span data-ttu-id="0bf9c-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bf9c-167">Requirement</span></span> | <span data-ttu-id="0bf9c-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bf9c-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf9c-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bf9c-169">Minimum supported client</span></span><br/> | <span data-ttu-id="0bf9c-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0bf9c-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0bf9c-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bf9c-171">Minimum supported server</span></span><br/> | <span data-ttu-id="0bf9c-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0bf9c-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0bf9c-173">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0bf9c-173">Namespace</span></span><br/>                | <span data-ttu-id="0bf9c-174">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0bf9c-174">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0bf9c-175">MOF</span><span class="sxs-lookup"><span data-stu-id="0bf9c-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bf9c-176"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0bf9c-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0bf9c-177">DLL</span><span class="sxs-lookup"><span data-stu-id="0bf9c-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bf9c-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bf9c-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bf9c-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bf9c-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bf9c-180">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="0bf9c-180">CIM\_LogicalFile</span></span>](deleteex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="0bf9c-181">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="0bf9c-181">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

