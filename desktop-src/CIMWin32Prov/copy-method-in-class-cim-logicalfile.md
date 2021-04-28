---
description: 'Méthode Copy de la classe CIM_LogicalFile : la méthode Copy copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.'
ms.assetid: 643946e4-5d32-4839-ae1f-80ec7cede429
ms.tgt_platform: multiple
title: Méthode Copy de la classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10ba9c28bde9d909d947e5a73241ce1aa8f1e956
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089727"
---
# <a name="copy-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="4c5ba-103">Méthode Copy de la \_ classe CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="4c5ba-103">Copy method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="4c5ba-104">La méthode **Copy** copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c5ba-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4c5ba-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4c5ba-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4c5ba-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="4c5ba-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4c5ba-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4c5ba-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4c5ba-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c5ba-109">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="4c5ba-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c5ba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c5ba-111">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c5ba-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c5ba-112">Nom complet du fichier de destination (ou répertoire).</span><span class="sxs-lookup"><span data-stu-id="4c5ba-112">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="4c5ba-113">Exemple : « c : \\ temp \\ newDirectory »</span><span class="sxs-lookup"><span data-stu-id="4c5ba-113">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c5ba-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4c5ba-114">Return value</span></span>

<span data-ttu-id="4c5ba-115">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="4c5ba-116">**Success**</span><span class="sxs-lookup"><span data-stu-id="4c5ba-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ba-117">0</span><span class="sxs-lookup"><span data-stu-id="4c5ba-117">0</span></span>

<span data-ttu-id="4c5ba-118">Réussite.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ba-119">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="4c5ba-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ba-120">2</span><span class="sxs-lookup"><span data-stu-id="4c5ba-120">2</span></span>

<span data-ttu-id="4c5ba-121">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ba-122">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="4c5ba-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ba-123">8</span><span class="sxs-lookup"><span data-stu-id="4c5ba-123">8</span></span>

<span data-ttu-id="4c5ba-124">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ba-125">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="4c5ba-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ba-126">9</span><span class="sxs-lookup"><span data-stu-id="4c5ba-126">9</span></span>

<span data-ttu-id="4c5ba-127">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ba-128">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="4c5ba-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ba-129">10</span><span class="sxs-lookup"><span data-stu-id="4c5ba-129">10</span></span>

<span data-ttu-id="4c5ba-130">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ba-131">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="4c5ba-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ba-132">11</span><span class="sxs-lookup"><span data-stu-id="4c5ba-132">11</span></span>

<span data-ttu-id="4c5ba-133">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ba-134">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="4c5ba-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ba-135">12</span><span class="sxs-lookup"><span data-stu-id="4c5ba-135">12</span></span>

<span data-ttu-id="4c5ba-136">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ba-137">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="4c5ba-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ba-138">13</span><span class="sxs-lookup"><span data-stu-id="4c5ba-138">13</span></span>

<span data-ttu-id="4c5ba-139">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ba-140">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="4c5ba-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ba-141">14</span><span class="sxs-lookup"><span data-stu-id="4c5ba-141">14</span></span>

<span data-ttu-id="4c5ba-142">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ba-143">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="4c5ba-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ba-144">15</span><span class="sxs-lookup"><span data-stu-id="4c5ba-144">15</span></span>

<span data-ttu-id="4c5ba-145">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ba-146">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="4c5ba-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ba-147">16</span><span class="sxs-lookup"><span data-stu-id="4c5ba-147">16</span></span>

<span data-ttu-id="4c5ba-148">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ba-149">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="4c5ba-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ba-150">17</span><span class="sxs-lookup"><span data-stu-id="4c5ba-150">17</span></span>

<span data-ttu-id="4c5ba-151">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ba-152">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="4c5ba-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ba-153">21</span><span class="sxs-lookup"><span data-stu-id="4c5ba-153">21</span></span>

<span data-ttu-id="4c5ba-154">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c5ba-155">Notes </span><span class="sxs-lookup"><span data-stu-id="4c5ba-155">Remarks</span></span>

<span data-ttu-id="4c5ba-156">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4c5ba-157">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4c5ba-158">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4c5ba-159">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4c5ba-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c5ba-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c5ba-160">Requirements</span></span>



| <span data-ttu-id="4c5ba-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c5ba-161">Requirement</span></span> | <span data-ttu-id="4c5ba-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c5ba-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c5ba-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c5ba-163">Minimum supported client</span></span><br/> | <span data-ttu-id="4c5ba-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c5ba-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4c5ba-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c5ba-165">Minimum supported server</span></span><br/> | <span data-ttu-id="4c5ba-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c5ba-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c5ba-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4c5ba-167">Namespace</span></span><br/>                | <span data-ttu-id="4c5ba-168">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4c5ba-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4c5ba-169">MOF</span><span class="sxs-lookup"><span data-stu-id="4c5ba-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c5ba-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c5ba-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c5ba-171">DLL</span><span class="sxs-lookup"><span data-stu-id="4c5ba-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c5ba-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c5ba-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c5ba-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c5ba-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c5ba-174">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="4c5ba-174">CIM\_LogicalFile</span></span>](copy-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="4c5ba-175">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="4c5ba-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

