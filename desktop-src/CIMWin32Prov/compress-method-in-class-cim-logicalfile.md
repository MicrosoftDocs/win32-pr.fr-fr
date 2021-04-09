---
description: La méthode Compress compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.
ms.assetid: 4a26beaf-388b-4f37-b4ee-ef3a7d15d2b6
ms.tgt_platform: multiple
title: Méthode Compress de la classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12938001d62920916e75d70ad632170c3e92bd51
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860729"
---
# <a name="compress-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="d5648-103">Méthode Compress de la \_ classe CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="d5648-103">Compress method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="d5648-104">La méthode **Compress** compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d5648-104">The **Compress** method compresses the logical file (or directory) specified in the object path.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5648-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d5648-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d5648-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d5648-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d5648-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d5648-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d5648-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d5648-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5648-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5648-109">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="d5648-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5648-110">Parameters</span></span>

<span data-ttu-id="d5648-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d5648-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5648-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5648-112">Return value</span></span>

<span data-ttu-id="d5648-113">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="d5648-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d5648-114">**Success**</span><span class="sxs-lookup"><span data-stu-id="d5648-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="d5648-115">0</span><span class="sxs-lookup"><span data-stu-id="d5648-115">0</span></span>

<span data-ttu-id="d5648-116">Réussite.</span><span class="sxs-lookup"><span data-stu-id="d5648-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="d5648-117">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="d5648-117">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="d5648-118">2</span><span class="sxs-lookup"><span data-stu-id="d5648-118">2</span></span>

<span data-ttu-id="d5648-119">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="d5648-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d5648-120">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="d5648-120">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="d5648-121">8</span><span class="sxs-lookup"><span data-stu-id="d5648-121">8</span></span>

<span data-ttu-id="d5648-122">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="d5648-122">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="d5648-123">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="d5648-123">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="d5648-124">9</span><span class="sxs-lookup"><span data-stu-id="d5648-124">9</span></span>

<span data-ttu-id="d5648-125">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="d5648-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="d5648-126">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="d5648-126">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d5648-127">10</span><span class="sxs-lookup"><span data-stu-id="d5648-127">10</span></span>

<span data-ttu-id="d5648-128">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="d5648-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d5648-129">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="d5648-129">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="d5648-130">11</span><span class="sxs-lookup"><span data-stu-id="d5648-130">11</span></span>

<span data-ttu-id="d5648-131">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="d5648-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d5648-132">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="d5648-132">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="d5648-133">12</span><span class="sxs-lookup"><span data-stu-id="d5648-133">12</span></span>

<span data-ttu-id="d5648-134">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="d5648-134">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d5648-135">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="d5648-135">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="d5648-136">13</span><span class="sxs-lookup"><span data-stu-id="d5648-136">13</span></span>

<span data-ttu-id="d5648-137">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="d5648-137">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d5648-138">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="d5648-138">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="d5648-139">14</span><span class="sxs-lookup"><span data-stu-id="d5648-139">14</span></span>

<span data-ttu-id="d5648-140">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="d5648-140">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d5648-141">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="d5648-141">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="d5648-142">15</span><span class="sxs-lookup"><span data-stu-id="d5648-142">15</span></span>

<span data-ttu-id="d5648-143">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="d5648-143">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d5648-144">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="d5648-144">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="d5648-145">16</span><span class="sxs-lookup"><span data-stu-id="d5648-145">16</span></span>

<span data-ttu-id="d5648-146">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="d5648-146">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="d5648-147">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="d5648-147">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="d5648-148">17</span><span class="sxs-lookup"><span data-stu-id="d5648-148">17</span></span>

<span data-ttu-id="d5648-149">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="d5648-149">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="d5648-150">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="d5648-150">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d5648-151">21</span><span class="sxs-lookup"><span data-stu-id="d5648-151">21</span></span>

<span data-ttu-id="d5648-152">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="d5648-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5648-153">Notes</span><span class="sxs-lookup"><span data-stu-id="d5648-153">Remarks</span></span>

<span data-ttu-id="d5648-154">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="d5648-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d5648-155">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d5648-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d5648-156">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d5648-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d5648-157">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d5648-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5648-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5648-158">Requirements</span></span>



| <span data-ttu-id="d5648-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5648-159">Requirement</span></span> | <span data-ttu-id="d5648-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5648-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5648-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5648-161">Minimum supported client</span></span><br/> | <span data-ttu-id="d5648-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5648-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5648-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5648-163">Minimum supported server</span></span><br/> | <span data-ttu-id="d5648-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5648-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5648-165">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d5648-165">Namespace</span></span><br/>                | <span data-ttu-id="d5648-166">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d5648-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d5648-167">MOF</span><span class="sxs-lookup"><span data-stu-id="d5648-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5648-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5648-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5648-169">DLL</span><span class="sxs-lookup"><span data-stu-id="d5648-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5648-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5648-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5648-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5648-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5648-172">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="d5648-172">CIM\_LogicalFile</span></span>](compress-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="d5648-173">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="d5648-173">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

