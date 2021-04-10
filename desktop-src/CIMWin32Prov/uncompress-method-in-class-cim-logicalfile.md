---
description: Décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.
ms.assetid: 0de01859-4a4b-4d70-802d-c52b2f56d7a1
ms.tgt_platform: multiple
title: Méthode decompress de la classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a2cde35ade1b1e8cbb3705a4c2f1b08f943139c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950509"
---
# <a name="uncompress-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="9aa15-103">Méthode decompress de la \_ classe CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="9aa15-103">Uncompress method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="9aa15-104">La méthode **decompress** décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9aa15-104">The **Uncompress** method uncompresses the logical file (or directory) specified in the object path.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9aa15-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="9aa15-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9aa15-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9aa15-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9aa15-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="9aa15-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9aa15-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9aa15-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa15-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9aa15-109">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="9aa15-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9aa15-110">Parameters</span></span>

<span data-ttu-id="9aa15-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9aa15-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9aa15-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9aa15-112">Return value</span></span>

<span data-ttu-id="9aa15-113">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="9aa15-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="9aa15-114">**Success**</span><span class="sxs-lookup"><span data-stu-id="9aa15-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="9aa15-115">0</span><span class="sxs-lookup"><span data-stu-id="9aa15-115">0</span></span>

<span data-ttu-id="9aa15-116">Réussite.</span><span class="sxs-lookup"><span data-stu-id="9aa15-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="9aa15-117">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="9aa15-117">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="9aa15-118">2</span><span class="sxs-lookup"><span data-stu-id="9aa15-118">2</span></span>

<span data-ttu-id="9aa15-119">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="9aa15-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="9aa15-120">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="9aa15-120">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="9aa15-121">8</span><span class="sxs-lookup"><span data-stu-id="9aa15-121">8</span></span>

<span data-ttu-id="9aa15-122">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="9aa15-122">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="9aa15-123">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="9aa15-123">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="9aa15-124">9</span><span class="sxs-lookup"><span data-stu-id="9aa15-124">9</span></span>

<span data-ttu-id="9aa15-125">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="9aa15-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="9aa15-126">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="9aa15-126">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="9aa15-127">10</span><span class="sxs-lookup"><span data-stu-id="9aa15-127">10</span></span>

<span data-ttu-id="9aa15-128">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="9aa15-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="9aa15-129">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="9aa15-129">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="9aa15-130">11</span><span class="sxs-lookup"><span data-stu-id="9aa15-130">11</span></span>

<span data-ttu-id="9aa15-131">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="9aa15-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="9aa15-132">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="9aa15-132">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="9aa15-133">12</span><span class="sxs-lookup"><span data-stu-id="9aa15-133">12</span></span>

<span data-ttu-id="9aa15-134">Plateforme non basée sur Windows NT.</span><span class="sxs-lookup"><span data-stu-id="9aa15-134">Platform not Windows NT-based.</span></span>

</dd> <dt>

<span data-ttu-id="9aa15-135">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="9aa15-135">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="9aa15-136">13</span><span class="sxs-lookup"><span data-stu-id="9aa15-136">13</span></span>

<span data-ttu-id="9aa15-137">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="9aa15-137">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="9aa15-138">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="9aa15-138">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="9aa15-139">14</span><span class="sxs-lookup"><span data-stu-id="9aa15-139">14</span></span>

<span data-ttu-id="9aa15-140">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="9aa15-140">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="9aa15-141">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="9aa15-141">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="9aa15-142">15</span><span class="sxs-lookup"><span data-stu-id="9aa15-142">15</span></span>

<span data-ttu-id="9aa15-143">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="9aa15-143">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="9aa15-144">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="9aa15-144">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="9aa15-145">16</span><span class="sxs-lookup"><span data-stu-id="9aa15-145">16</span></span>

<span data-ttu-id="9aa15-146">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="9aa15-146">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="9aa15-147">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="9aa15-147">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="9aa15-148">17</span><span class="sxs-lookup"><span data-stu-id="9aa15-148">17</span></span>

<span data-ttu-id="9aa15-149">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="9aa15-149">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="9aa15-150">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="9aa15-150">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9aa15-151">21</span><span class="sxs-lookup"><span data-stu-id="9aa15-151">21</span></span>

<span data-ttu-id="9aa15-152">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="9aa15-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9aa15-153">Notes</span><span class="sxs-lookup"><span data-stu-id="9aa15-153">Remarks</span></span>

<span data-ttu-id="9aa15-154">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="9aa15-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9aa15-155">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9aa15-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9aa15-156">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="9aa15-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9aa15-157">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9aa15-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa15-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9aa15-158">Requirements</span></span>



| <span data-ttu-id="9aa15-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9aa15-159">Requirement</span></span> | <span data-ttu-id="9aa15-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="9aa15-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa15-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9aa15-161">Minimum supported client</span></span><br/> | <span data-ttu-id="9aa15-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9aa15-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9aa15-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9aa15-163">Minimum supported server</span></span><br/> | <span data-ttu-id="9aa15-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9aa15-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9aa15-165">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9aa15-165">Namespace</span></span><br/>                | <span data-ttu-id="9aa15-166">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9aa15-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9aa15-167">MOF</span><span class="sxs-lookup"><span data-stu-id="9aa15-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9aa15-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9aa15-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9aa15-169">DLL</span><span class="sxs-lookup"><span data-stu-id="9aa15-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aa15-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aa15-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aa15-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9aa15-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa15-172">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="9aa15-172">CIM\_LogicalFile</span></span>](uncompress-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="9aa15-173">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="9aa15-173">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

