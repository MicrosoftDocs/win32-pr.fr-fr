---
description: Renomme le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Le changement de nom n’est pas pris en charge si la destination se trouve sur un autre lecteur ou si le remplacement d’un fichier logique existant est nécessaire.
ms.assetid: 728737a7-7cb8-4237-be03-16c4dac530b2
ms.tgt_platform: multiple
title: Renommer la méthode de la classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83429f3a5248b1d3be24832b26bf99213d442ce5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483729"
---
# <a name="rename-method-of-the-cim_directory-class"></a><span data-ttu-id="4247a-104">Renommer la méthode de la \_ classe de répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="4247a-104">Rename method of the CIM\_Directory class</span></span>

<span data-ttu-id="4247a-105">La méthode **Rename** renomme le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4247a-105">The **Rename** method renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="4247a-106">Le changement de nom n’est pas pris en charge si la destination se trouve sur un autre lecteur ou si le remplacement d’un fichier logique existant est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4247a-106">Renaming is not supported if the destination is on another drive or overwriting an existing logical file is required.</span></span>

<span data-ttu-id="4247a-107">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="4247a-107">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4247a-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="4247a-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4247a-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4247a-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4247a-110">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="4247a-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4247a-111">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4247a-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4247a-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4247a-112">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="4247a-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4247a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4247a-114">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4247a-114">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4247a-115">Nouveau nom complet du fichier (ou répertoire).</span><span class="sxs-lookup"><span data-stu-id="4247a-115">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="4247a-116">Exemple : « c : \\ temp \\newname.txt »</span><span class="sxs-lookup"><span data-stu-id="4247a-116">Example: "c:\\temp\\newname.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4247a-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4247a-117">Return value</span></span>

<span data-ttu-id="4247a-118">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="4247a-118">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="4247a-119">**0**</span><span class="sxs-lookup"><span data-stu-id="4247a-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4247a-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="4247a-120">Success.</span></span>

</dd> <dt>

<span data-ttu-id="4247a-121">**2**</span><span class="sxs-lookup"><span data-stu-id="4247a-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="4247a-122">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="4247a-122">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4247a-123">**8**</span><span class="sxs-lookup"><span data-stu-id="4247a-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="4247a-124">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="4247a-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="4247a-125">**9**</span><span class="sxs-lookup"><span data-stu-id="4247a-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="4247a-126">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="4247a-126">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="4247a-127">**10**</span><span class="sxs-lookup"><span data-stu-id="4247a-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="4247a-128">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="4247a-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4247a-129">**11**</span><span class="sxs-lookup"><span data-stu-id="4247a-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="4247a-130">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="4247a-130">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4247a-131">**12**</span><span class="sxs-lookup"><span data-stu-id="4247a-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="4247a-132">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="4247a-132">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="4247a-133">**13**</span><span class="sxs-lookup"><span data-stu-id="4247a-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="4247a-134">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="4247a-134">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="4247a-135">**14**</span><span class="sxs-lookup"><span data-stu-id="4247a-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="4247a-136">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="4247a-136">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="4247a-137">**15**</span><span class="sxs-lookup"><span data-stu-id="4247a-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="4247a-138">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="4247a-138">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="4247a-139">**16**</span><span class="sxs-lookup"><span data-stu-id="4247a-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="4247a-140">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="4247a-140">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="4247a-141">**17**</span><span class="sxs-lookup"><span data-stu-id="4247a-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="4247a-142">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="4247a-142">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="4247a-143">**21**</span><span class="sxs-lookup"><span data-stu-id="4247a-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="4247a-144">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="4247a-144">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4247a-145">Notes</span><span class="sxs-lookup"><span data-stu-id="4247a-145">Remarks</span></span>

<span data-ttu-id="4247a-146">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="4247a-146">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4247a-147">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4247a-147">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4247a-148">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="4247a-148">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4247a-149">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4247a-149">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4247a-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4247a-150">Requirements</span></span>



| <span data-ttu-id="4247a-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4247a-151">Requirement</span></span> | <span data-ttu-id="4247a-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="4247a-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4247a-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4247a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="4247a-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4247a-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4247a-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4247a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="4247a-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4247a-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4247a-157">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4247a-157">Namespace</span></span><br/>                | <span data-ttu-id="4247a-158">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4247a-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4247a-159">MOF</span><span class="sxs-lookup"><span data-stu-id="4247a-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4247a-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4247a-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4247a-161">DLL</span><span class="sxs-lookup"><span data-stu-id="4247a-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4247a-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4247a-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4247a-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4247a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4247a-164">\_Répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="4247a-164">CIM\_Directory</span></span>](rename-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="4247a-165">**\_Répertoire CIM**</span><span class="sxs-lookup"><span data-stu-id="4247a-165">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

