---
description: La méthode Copy copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.
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
ms.openlocfilehash: 4a69107bd173be0aa853c1541a1e1365148c2e59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033700"
---
# <a name="copy-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="13d05-103">Méthode Copy de la \_ classe CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="13d05-103">Copy method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="13d05-104">La méthode **Copy** copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="13d05-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="13d05-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="13d05-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="13d05-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="13d05-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="13d05-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="13d05-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="13d05-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="13d05-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="13d05-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13d05-109">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="13d05-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13d05-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13d05-111">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="13d05-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13d05-112">Nom complet du fichier de destination (ou répertoire).</span><span class="sxs-lookup"><span data-stu-id="13d05-112">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="13d05-113">Exemple : « c : \\ temp \\ newDirectory »</span><span class="sxs-lookup"><span data-stu-id="13d05-113">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13d05-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13d05-114">Return value</span></span>

<span data-ttu-id="13d05-115">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="13d05-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="13d05-116">**Success**</span><span class="sxs-lookup"><span data-stu-id="13d05-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="13d05-117">0</span><span class="sxs-lookup"><span data-stu-id="13d05-117">0</span></span>

<span data-ttu-id="13d05-118">Réussite.</span><span class="sxs-lookup"><span data-stu-id="13d05-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="13d05-119">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="13d05-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="13d05-120">2</span><span class="sxs-lookup"><span data-stu-id="13d05-120">2</span></span>

<span data-ttu-id="13d05-121">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="13d05-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="13d05-122">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="13d05-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="13d05-123">8</span><span class="sxs-lookup"><span data-stu-id="13d05-123">8</span></span>

<span data-ttu-id="13d05-124">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="13d05-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="13d05-125">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="13d05-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="13d05-126">9</span><span class="sxs-lookup"><span data-stu-id="13d05-126">9</span></span>

<span data-ttu-id="13d05-127">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="13d05-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="13d05-128">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="13d05-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="13d05-129">10</span><span class="sxs-lookup"><span data-stu-id="13d05-129">10</span></span>

<span data-ttu-id="13d05-130">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="13d05-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="13d05-131">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="13d05-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="13d05-132">11</span><span class="sxs-lookup"><span data-stu-id="13d05-132">11</span></span>

<span data-ttu-id="13d05-133">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="13d05-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="13d05-134">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="13d05-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="13d05-135">12</span><span class="sxs-lookup"><span data-stu-id="13d05-135">12</span></span>

<span data-ttu-id="13d05-136">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="13d05-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="13d05-137">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="13d05-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="13d05-138">13</span><span class="sxs-lookup"><span data-stu-id="13d05-138">13</span></span>

<span data-ttu-id="13d05-139">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="13d05-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="13d05-140">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="13d05-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="13d05-141">14</span><span class="sxs-lookup"><span data-stu-id="13d05-141">14</span></span>

<span data-ttu-id="13d05-142">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="13d05-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="13d05-143">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="13d05-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="13d05-144">15</span><span class="sxs-lookup"><span data-stu-id="13d05-144">15</span></span>

<span data-ttu-id="13d05-145">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="13d05-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="13d05-146">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="13d05-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="13d05-147">16</span><span class="sxs-lookup"><span data-stu-id="13d05-147">16</span></span>

<span data-ttu-id="13d05-148">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="13d05-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="13d05-149">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="13d05-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="13d05-150">17</span><span class="sxs-lookup"><span data-stu-id="13d05-150">17</span></span>

<span data-ttu-id="13d05-151">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="13d05-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="13d05-152">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="13d05-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="13d05-153">21</span><span class="sxs-lookup"><span data-stu-id="13d05-153">21</span></span>

<span data-ttu-id="13d05-154">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="13d05-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13d05-155">Notes</span><span class="sxs-lookup"><span data-stu-id="13d05-155">Remarks</span></span>

<span data-ttu-id="13d05-156">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="13d05-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="13d05-157">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="13d05-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="13d05-158">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="13d05-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="13d05-159">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="13d05-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="13d05-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13d05-160">Requirements</span></span>



| <span data-ttu-id="13d05-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13d05-161">Requirement</span></span> | <span data-ttu-id="13d05-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="13d05-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13d05-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13d05-163">Minimum supported client</span></span><br/> | <span data-ttu-id="13d05-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13d05-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13d05-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13d05-165">Minimum supported server</span></span><br/> | <span data-ttu-id="13d05-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13d05-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13d05-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="13d05-167">Namespace</span></span><br/>                | <span data-ttu-id="13d05-168">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="13d05-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="13d05-169">MOF</span><span class="sxs-lookup"><span data-stu-id="13d05-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13d05-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13d05-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="13d05-171">DLL</span><span class="sxs-lookup"><span data-stu-id="13d05-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13d05-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13d05-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d05-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13d05-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d05-174">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="13d05-174">CIM\_LogicalFile</span></span>](copy-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="13d05-175">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="13d05-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

