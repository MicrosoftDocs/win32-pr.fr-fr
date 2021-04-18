---
description: Compresse le fichier d’entrée de répertoire logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est héritée de la \_ LOGICALFILE CIM.
ms.assetid: 40aac2f8-4ff6-4e21-9395-5d3d40b39b00
ms.tgt_platform: multiple
title: Méthode Compress de la classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f1717e77fdedb0c6b2e218e66f61d67bcef7c1a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513122"
---
# <a name="compress-method-of-the-cim_directory-class"></a><span data-ttu-id="45015-104">Méthode Compress de la \_ classe de répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="45015-104">Compress method of the CIM\_Directory class</span></span>

<span data-ttu-id="45015-105">La méthode **Compress** compresse le fichier d’entrée de répertoire logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45015-105">The **Compress** method compresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="45015-106">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="45015-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45015-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="45015-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="45015-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="45015-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="45015-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="45015-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="45015-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="45015-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="45015-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45015-111">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="45015-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45015-112">Parameters</span></span>

<span data-ttu-id="45015-113">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="45015-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="45015-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="45015-114">Return value</span></span>

<span data-ttu-id="45015-115">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="45015-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="45015-116">**0**</span><span class="sxs-lookup"><span data-stu-id="45015-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="45015-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="45015-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="45015-118">**2**</span><span class="sxs-lookup"><span data-stu-id="45015-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="45015-119">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="45015-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="45015-120">**8**</span><span class="sxs-lookup"><span data-stu-id="45015-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="45015-121">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="45015-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="45015-122">**9**</span><span class="sxs-lookup"><span data-stu-id="45015-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="45015-123">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="45015-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="45015-124">**10**</span><span class="sxs-lookup"><span data-stu-id="45015-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="45015-125">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="45015-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="45015-126">**11**</span><span class="sxs-lookup"><span data-stu-id="45015-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="45015-127">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="45015-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="45015-128">**12**</span><span class="sxs-lookup"><span data-stu-id="45015-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="45015-129">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="45015-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="45015-130">**13**</span><span class="sxs-lookup"><span data-stu-id="45015-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="45015-131">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="45015-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="45015-132">**14**</span><span class="sxs-lookup"><span data-stu-id="45015-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="45015-133">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="45015-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="45015-134">**15**</span><span class="sxs-lookup"><span data-stu-id="45015-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="45015-135">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="45015-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="45015-136">**16**</span><span class="sxs-lookup"><span data-stu-id="45015-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="45015-137">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="45015-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="45015-138">**17**</span><span class="sxs-lookup"><span data-stu-id="45015-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="45015-139">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="45015-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="45015-140">**21**</span><span class="sxs-lookup"><span data-stu-id="45015-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="45015-141">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="45015-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45015-142">Notes</span><span class="sxs-lookup"><span data-stu-id="45015-142">Remarks</span></span>

<span data-ttu-id="45015-143">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="45015-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="45015-144">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="45015-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="45015-145">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="45015-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="45015-146">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="45015-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="45015-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45015-147">Requirements</span></span>



| <span data-ttu-id="45015-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45015-148">Requirement</span></span> | <span data-ttu-id="45015-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="45015-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45015-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45015-150">Minimum supported client</span></span><br/> | <span data-ttu-id="45015-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45015-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45015-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45015-152">Minimum supported server</span></span><br/> | <span data-ttu-id="45015-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45015-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45015-154">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="45015-154">Namespace</span></span><br/>                | <span data-ttu-id="45015-155">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="45015-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="45015-156">MOF</span><span class="sxs-lookup"><span data-stu-id="45015-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45015-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45015-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="45015-158">DLL</span><span class="sxs-lookup"><span data-stu-id="45015-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45015-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45015-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45015-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45015-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45015-161">\_Répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="45015-161">CIM\_Directory</span></span>](compress-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="45015-162">**\_Répertoire CIM**</span><span class="sxs-lookup"><span data-stu-id="45015-162">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

