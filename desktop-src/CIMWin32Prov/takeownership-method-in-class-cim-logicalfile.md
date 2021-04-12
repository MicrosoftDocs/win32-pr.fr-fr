---
description: La méthode TakeOwnerShip obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet. Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en prenant possession de tous les fichiers et sous-répertoires contenus dans le répertoire.
ms.assetid: 5db62da0-ac93-4a8c-af17-306e02bfa756
ms.tgt_platform: multiple
title: Méthode TakeOwnerShip de la classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7cdd9515a5e947a3e707464dcbd524c875f7785f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523015"
---
# <a name="takeownership-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="91c7e-104">Méthode TakeOwnerShip de la \_ classe CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="91c7e-104">TakeOwnerShip method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="91c7e-105">La méthode **TakeOwnership** obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="91c7e-105">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="91c7e-106">Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en prenant possession de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="91c7e-106">If the logical file is a directory, then this method acts recursively, taking ownership of all files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91c7e-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="91c7e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="91c7e-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="91c7e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="91c7e-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="91c7e-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="91c7e-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="91c7e-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="91c7e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91c7e-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="91c7e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91c7e-112">Parameters</span></span>

<span data-ttu-id="91c7e-113">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="91c7e-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91c7e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91c7e-114">Return value</span></span>

<span data-ttu-id="91c7e-115">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="91c7e-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="91c7e-116">**Success**</span><span class="sxs-lookup"><span data-stu-id="91c7e-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="91c7e-117">0</span><span class="sxs-lookup"><span data-stu-id="91c7e-117">0</span></span>

<span data-ttu-id="91c7e-118">Réussite.</span><span class="sxs-lookup"><span data-stu-id="91c7e-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="91c7e-119">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="91c7e-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="91c7e-120">2</span><span class="sxs-lookup"><span data-stu-id="91c7e-120">2</span></span>

<span data-ttu-id="91c7e-121">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="91c7e-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="91c7e-122">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="91c7e-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="91c7e-123">8</span><span class="sxs-lookup"><span data-stu-id="91c7e-123">8</span></span>

<span data-ttu-id="91c7e-124">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="91c7e-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="91c7e-125">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="91c7e-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="91c7e-126">9</span><span class="sxs-lookup"><span data-stu-id="91c7e-126">9</span></span>

<span data-ttu-id="91c7e-127">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="91c7e-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="91c7e-128">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="91c7e-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="91c7e-129">10</span><span class="sxs-lookup"><span data-stu-id="91c7e-129">10</span></span>

<span data-ttu-id="91c7e-130">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="91c7e-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="91c7e-131">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="91c7e-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="91c7e-132">11</span><span class="sxs-lookup"><span data-stu-id="91c7e-132">11</span></span>

<span data-ttu-id="91c7e-133">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="91c7e-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="91c7e-134">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="91c7e-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="91c7e-135">12</span><span class="sxs-lookup"><span data-stu-id="91c7e-135">12</span></span>

<span data-ttu-id="91c7e-136">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="91c7e-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="91c7e-137">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="91c7e-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="91c7e-138">13</span><span class="sxs-lookup"><span data-stu-id="91c7e-138">13</span></span>

<span data-ttu-id="91c7e-139">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="91c7e-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="91c7e-140">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="91c7e-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="91c7e-141">14</span><span class="sxs-lookup"><span data-stu-id="91c7e-141">14</span></span>

<span data-ttu-id="91c7e-142">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="91c7e-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="91c7e-143">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="91c7e-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="91c7e-144">15</span><span class="sxs-lookup"><span data-stu-id="91c7e-144">15</span></span>

<span data-ttu-id="91c7e-145">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="91c7e-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="91c7e-146">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="91c7e-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="91c7e-147">16</span><span class="sxs-lookup"><span data-stu-id="91c7e-147">16</span></span>

<span data-ttu-id="91c7e-148">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="91c7e-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="91c7e-149">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="91c7e-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="91c7e-150">17</span><span class="sxs-lookup"><span data-stu-id="91c7e-150">17</span></span>

<span data-ttu-id="91c7e-151">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="91c7e-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="91c7e-152">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="91c7e-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="91c7e-153">21</span><span class="sxs-lookup"><span data-stu-id="91c7e-153">21</span></span>

<span data-ttu-id="91c7e-154">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="91c7e-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91c7e-155">Notes</span><span class="sxs-lookup"><span data-stu-id="91c7e-155">Remarks</span></span>

<span data-ttu-id="91c7e-156">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="91c7e-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="91c7e-157">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="91c7e-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="91c7e-158">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="91c7e-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="91c7e-159">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="91c7e-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="91c7e-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91c7e-160">Requirements</span></span>



| <span data-ttu-id="91c7e-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91c7e-161">Requirement</span></span> | <span data-ttu-id="91c7e-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="91c7e-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91c7e-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91c7e-163">Minimum supported client</span></span><br/> | <span data-ttu-id="91c7e-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91c7e-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91c7e-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91c7e-165">Minimum supported server</span></span><br/> | <span data-ttu-id="91c7e-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91c7e-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91c7e-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="91c7e-167">Namespace</span></span><br/>                | <span data-ttu-id="91c7e-168">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="91c7e-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="91c7e-169">MOF</span><span class="sxs-lookup"><span data-stu-id="91c7e-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91c7e-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91c7e-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="91c7e-171">DLL</span><span class="sxs-lookup"><span data-stu-id="91c7e-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91c7e-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91c7e-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91c7e-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91c7e-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c7e-174">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="91c7e-174">CIM\_LogicalFile</span></span>](takeownership-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="91c7e-175">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="91c7e-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

