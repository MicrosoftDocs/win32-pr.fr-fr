---
description: Obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode TakeOwnerShip.
ms.assetid: c01ab071-86e4-484d-aaed-4783b6c3bebf
ms.tgt_platform: multiple
title: Méthode TakeOwnerShipEx de la classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e7f08413440ec32037554476ced386c56827239
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519205"
---
# <a name="takeownershipex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="53b5e-104">Méthode TakeOwnerShipEx de la \_ classe CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="53b5e-104">TakeOwnerShipEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="53b5e-105">La méthode **TakeOwnerShipEx** obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="53b5e-105">The **TakeOwnerShipEx** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="53b5e-106">Cette méthode est une version étendue de la méthode [**TakeOwnership**](takeownership-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="53b5e-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-logicalfile.md) method.</span></span> <span data-ttu-id="53b5e-107">Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en prenant possession de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="53b5e-107">If the logical file is a directory, then this method acts recursively, taking ownership of all files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="53b5e-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="53b5e-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="53b5e-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="53b5e-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="53b5e-110">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="53b5e-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="53b5e-111">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="53b5e-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="53b5e-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53b5e-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="53b5e-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53b5e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53b5e-114">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="53b5e-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-115">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="53b5e-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="53b5e-116">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="53b5e-116">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="53b5e-117">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="53b5e-117">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-118">Chaîne qui nomme le fichier enfant (ou le répertoire) à utiliser comme point de départ de la méthode.</span><span class="sxs-lookup"><span data-stu-id="53b5e-118">String that names the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="53b5e-119">En général, ce paramètre est le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="53b5e-119">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="53b5e-120">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier (ou le répertoire) spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="53b5e-120">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="53b5e-121">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="53b5e-121">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-122">Si la **valeur est true**, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="53b5e-122">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="53b5e-123">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="53b5e-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53b5e-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53b5e-124">Return value</span></span>

<span data-ttu-id="53b5e-125">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="53b5e-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="53b5e-126">**Success**</span><span class="sxs-lookup"><span data-stu-id="53b5e-126">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-127">0</span><span class="sxs-lookup"><span data-stu-id="53b5e-127">0</span></span>

<span data-ttu-id="53b5e-128">Réussite.</span><span class="sxs-lookup"><span data-stu-id="53b5e-128">Success.</span></span>

</dd> <dt>

<span data-ttu-id="53b5e-129">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="53b5e-129">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-130">2</span><span class="sxs-lookup"><span data-stu-id="53b5e-130">2</span></span>

<span data-ttu-id="53b5e-131">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="53b5e-131">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="53b5e-132">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="53b5e-132">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-133">8</span><span class="sxs-lookup"><span data-stu-id="53b5e-133">8</span></span>

<span data-ttu-id="53b5e-134">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="53b5e-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="53b5e-135">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="53b5e-135">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-136">9</span><span class="sxs-lookup"><span data-stu-id="53b5e-136">9</span></span>

<span data-ttu-id="53b5e-137">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="53b5e-137">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="53b5e-138">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="53b5e-138">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-139">10</span><span class="sxs-lookup"><span data-stu-id="53b5e-139">10</span></span>

<span data-ttu-id="53b5e-140">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="53b5e-140">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="53b5e-141">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="53b5e-141">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-142">11</span><span class="sxs-lookup"><span data-stu-id="53b5e-142">11</span></span>

<span data-ttu-id="53b5e-143">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="53b5e-143">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="53b5e-144">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="53b5e-144">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-145">12</span><span class="sxs-lookup"><span data-stu-id="53b5e-145">12</span></span>

<span data-ttu-id="53b5e-146">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="53b5e-146">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="53b5e-147">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="53b5e-147">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-148">13</span><span class="sxs-lookup"><span data-stu-id="53b5e-148">13</span></span>

<span data-ttu-id="53b5e-149">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="53b5e-149">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="53b5e-150">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="53b5e-150">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-151">14</span><span class="sxs-lookup"><span data-stu-id="53b5e-151">14</span></span>

<span data-ttu-id="53b5e-152">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="53b5e-152">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="53b5e-153">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="53b5e-153">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-154">15</span><span class="sxs-lookup"><span data-stu-id="53b5e-154">15</span></span>

<span data-ttu-id="53b5e-155">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="53b5e-155">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="53b5e-156">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="53b5e-156">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-157">16</span><span class="sxs-lookup"><span data-stu-id="53b5e-157">16</span></span>

<span data-ttu-id="53b5e-158">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="53b5e-158">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="53b5e-159">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="53b5e-159">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-160">17</span><span class="sxs-lookup"><span data-stu-id="53b5e-160">17</span></span>

<span data-ttu-id="53b5e-161">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="53b5e-161">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="53b5e-162">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="53b5e-162">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="53b5e-163">21</span><span class="sxs-lookup"><span data-stu-id="53b5e-163">21</span></span>

<span data-ttu-id="53b5e-164">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="53b5e-164">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53b5e-165">Notes</span><span class="sxs-lookup"><span data-stu-id="53b5e-165">Remarks</span></span>

<span data-ttu-id="53b5e-166">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="53b5e-166">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="53b5e-167">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="53b5e-167">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="53b5e-168">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="53b5e-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="53b5e-169">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="53b5e-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="53b5e-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53b5e-170">Requirements</span></span>



| <span data-ttu-id="53b5e-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53b5e-171">Requirement</span></span> | <span data-ttu-id="53b5e-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="53b5e-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53b5e-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53b5e-173">Minimum supported client</span></span><br/> | <span data-ttu-id="53b5e-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53b5e-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="53b5e-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53b5e-175">Minimum supported server</span></span><br/> | <span data-ttu-id="53b5e-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53b5e-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="53b5e-177">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="53b5e-177">Namespace</span></span><br/>                | <span data-ttu-id="53b5e-178">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="53b5e-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="53b5e-179">MOF</span><span class="sxs-lookup"><span data-stu-id="53b5e-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53b5e-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53b5e-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="53b5e-181">DLL</span><span class="sxs-lookup"><span data-stu-id="53b5e-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53b5e-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53b5e-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53b5e-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53b5e-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b5e-184">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="53b5e-184">CIM\_LogicalFile</span></span>](takeownershipex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="53b5e-185">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="53b5e-185">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

