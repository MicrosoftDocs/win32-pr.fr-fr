---
description: La méthode Copy copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.
ms.assetid: 71481cc8-9052-4c62-9c26-6887ea646ee1
ms.tgt_platform: multiple
title: Méthode Copy de la classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 02bca61e559cea9ee56b9d36b28d13c33e423f9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110811"
---
# <a name="copy-method-of-the-cim_directory-class"></a><span data-ttu-id="1986c-103">Méthode Copy de la \_ classe Directory CIM</span><span class="sxs-lookup"><span data-stu-id="1986c-103">Copy method of the CIM\_Directory class</span></span>

<span data-ttu-id="1986c-104">La méthode **Copy** copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1986c-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="1986c-105">Une copie n’est pas prise en charge si le remplacement d’un fichier logique existant est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1986c-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="1986c-106">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="1986c-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1986c-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="1986c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1986c-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1986c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1986c-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1986c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1986c-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1986c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1986c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1986c-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="1986c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1986c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1986c-113">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1986c-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1986c-114">Nom complet de la copie du fichier de destination (ou répertoire).</span><span class="sxs-lookup"><span data-stu-id="1986c-114">Fully qualified name of the copy of the destination file (or directory).</span></span>

<span data-ttu-id="1986c-115">Exemple : « c : \\ temp \\ newDirectory »</span><span class="sxs-lookup"><span data-stu-id="1986c-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1986c-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1986c-116">Return value</span></span>

<span data-ttu-id="1986c-117">Retourne la valeur 0 en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="1986c-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1986c-118">**0**</span><span class="sxs-lookup"><span data-stu-id="1986c-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1986c-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="1986c-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="1986c-120">**2**</span><span class="sxs-lookup"><span data-stu-id="1986c-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1986c-121">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="1986c-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="1986c-122">**8**</span><span class="sxs-lookup"><span data-stu-id="1986c-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1986c-123">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="1986c-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="1986c-124">**9**</span><span class="sxs-lookup"><span data-stu-id="1986c-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1986c-125">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="1986c-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="1986c-126">**10**</span><span class="sxs-lookup"><span data-stu-id="1986c-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1986c-127">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="1986c-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1986c-128">**11**</span><span class="sxs-lookup"><span data-stu-id="1986c-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1986c-129">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="1986c-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="1986c-130">**12**</span><span class="sxs-lookup"><span data-stu-id="1986c-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1986c-131">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="1986c-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1986c-132">**13**</span><span class="sxs-lookup"><span data-stu-id="1986c-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1986c-133">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="1986c-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="1986c-134">**14**</span><span class="sxs-lookup"><span data-stu-id="1986c-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1986c-135">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="1986c-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="1986c-136">**15**</span><span class="sxs-lookup"><span data-stu-id="1986c-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1986c-137">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="1986c-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="1986c-138">**16**</span><span class="sxs-lookup"><span data-stu-id="1986c-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1986c-139">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="1986c-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="1986c-140">**17**</span><span class="sxs-lookup"><span data-stu-id="1986c-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1986c-141">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="1986c-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="1986c-142">**21**</span><span class="sxs-lookup"><span data-stu-id="1986c-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1986c-143">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="1986c-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1986c-144">Notes</span><span class="sxs-lookup"><span data-stu-id="1986c-144">Remarks</span></span>

<span data-ttu-id="1986c-145">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="1986c-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1986c-146">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1986c-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1986c-147">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="1986c-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1986c-148">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="1986c-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1986c-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1986c-149">Requirements</span></span>



| <span data-ttu-id="1986c-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1986c-150">Requirement</span></span> | <span data-ttu-id="1986c-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="1986c-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1986c-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1986c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="1986c-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1986c-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1986c-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1986c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="1986c-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1986c-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1986c-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1986c-156">Namespace</span></span><br/>                | <span data-ttu-id="1986c-157">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1986c-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1986c-158">MOF</span><span class="sxs-lookup"><span data-stu-id="1986c-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1986c-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1986c-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1986c-160">DLL</span><span class="sxs-lookup"><span data-stu-id="1986c-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1986c-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1986c-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1986c-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1986c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1986c-163">\_Répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="1986c-163">CIM\_Directory</span></span>](copy-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="1986c-164">**\_Répertoire CIM**</span><span class="sxs-lookup"><span data-stu-id="1986c-164">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

