---
description: La méthode Rename renomme le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Le changement de nom n’est pas pris en charge si la destination se trouve sur un autre lecteur ou si le remplacement d’un fichier logique existant est nécessaire.
ms.assetid: 5a62ff64-d1d2-43a2-997c-0ad46896b31f
ms.tgt_platform: multiple
title: Renommer la méthode de la classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0da38020d7b22dceb6f1d061f8feaf858eeb5f04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111250"
---
# <a name="rename-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="61901-104">Renommer la méthode de la \_ classe CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="61901-104">Rename method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="61901-105">La méthode **Rename** renomme le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="61901-105">The **Rename** method renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="61901-106">Le changement de nom n’est pas pris en charge si la destination se trouve sur un autre lecteur ou si le remplacement d’un fichier logique existant est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="61901-106">Renaming is not supported if the destination is on another drive, or overwriting an existing logical file is required.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61901-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="61901-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="61901-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="61901-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="61901-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="61901-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="61901-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="61901-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="61901-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61901-111">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="61901-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61901-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61901-113">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61901-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61901-114">Nom complet du nouveau fichier (ou du répertoire).</span><span class="sxs-lookup"><span data-stu-id="61901-114">Fully qualified new file (or directory) name.</span></span>

<span data-ttu-id="61901-115">Exemple : « c : \\ temp \\newfile.txt »</span><span class="sxs-lookup"><span data-stu-id="61901-115">Example: "c:\\temp\\newfile.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61901-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61901-116">Return value</span></span>

<span data-ttu-id="61901-117">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="61901-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="61901-118">**Success**</span><span class="sxs-lookup"><span data-stu-id="61901-118">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="61901-119">0</span><span class="sxs-lookup"><span data-stu-id="61901-119">0</span></span>

<span data-ttu-id="61901-120">Réussite.</span><span class="sxs-lookup"><span data-stu-id="61901-120">Success.</span></span>

</dd> <dt>

<span data-ttu-id="61901-121">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="61901-121">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="61901-122">2</span><span class="sxs-lookup"><span data-stu-id="61901-122">2</span></span>

<span data-ttu-id="61901-123">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="61901-123">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="61901-124">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="61901-124">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="61901-125">8</span><span class="sxs-lookup"><span data-stu-id="61901-125">8</span></span>

<span data-ttu-id="61901-126">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="61901-126">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="61901-127">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="61901-127">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="61901-128">9</span><span class="sxs-lookup"><span data-stu-id="61901-128">9</span></span>

<span data-ttu-id="61901-129">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="61901-129">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="61901-130">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="61901-130">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="61901-131">10</span><span class="sxs-lookup"><span data-stu-id="61901-131">10</span></span>

<span data-ttu-id="61901-132">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="61901-132">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="61901-133">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="61901-133">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="61901-134">11</span><span class="sxs-lookup"><span data-stu-id="61901-134">11</span></span>

<span data-ttu-id="61901-135">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="61901-135">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="61901-136">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="61901-136">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="61901-137">12</span><span class="sxs-lookup"><span data-stu-id="61901-137">12</span></span>

<span data-ttu-id="61901-138">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="61901-138">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="61901-139">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="61901-139">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="61901-140">13</span><span class="sxs-lookup"><span data-stu-id="61901-140">13</span></span>

<span data-ttu-id="61901-141">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="61901-141">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="61901-142">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="61901-142">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="61901-143">14</span><span class="sxs-lookup"><span data-stu-id="61901-143">14</span></span>

<span data-ttu-id="61901-144">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="61901-144">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="61901-145">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="61901-145">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="61901-146">15</span><span class="sxs-lookup"><span data-stu-id="61901-146">15</span></span>

<span data-ttu-id="61901-147">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="61901-147">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="61901-148">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="61901-148">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="61901-149">16</span><span class="sxs-lookup"><span data-stu-id="61901-149">16</span></span>

<span data-ttu-id="61901-150">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="61901-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="61901-151">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="61901-151">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="61901-152">17</span><span class="sxs-lookup"><span data-stu-id="61901-152">17</span></span>

<span data-ttu-id="61901-153">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="61901-153">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="61901-154">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="61901-154">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="61901-155">21</span><span class="sxs-lookup"><span data-stu-id="61901-155">21</span></span>

<span data-ttu-id="61901-156">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="61901-156">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61901-157">Notes</span><span class="sxs-lookup"><span data-stu-id="61901-157">Remarks</span></span>

<span data-ttu-id="61901-158">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="61901-158">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="61901-159">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="61901-159">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="61901-160">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="61901-160">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="61901-161">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="61901-161">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="61901-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61901-162">Requirements</span></span>



| <span data-ttu-id="61901-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61901-163">Requirement</span></span> | <span data-ttu-id="61901-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="61901-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61901-165">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61901-165">Minimum supported client</span></span><br/> | <span data-ttu-id="61901-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61901-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="61901-167">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61901-167">Minimum supported server</span></span><br/> | <span data-ttu-id="61901-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61901-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="61901-169">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="61901-169">Namespace</span></span><br/>                | <span data-ttu-id="61901-170">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="61901-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="61901-171">MOF</span><span class="sxs-lookup"><span data-stu-id="61901-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61901-172"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61901-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="61901-173">DLL</span><span class="sxs-lookup"><span data-stu-id="61901-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61901-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61901-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61901-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61901-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61901-176">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="61901-176">CIM\_LogicalFile</span></span>](rename-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="61901-177">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="61901-177">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

