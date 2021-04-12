---
description: Décompresse le fichier de données logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet. Cette méthode est héritée de la \_ LOGICALFILE CIM.
ms.assetid: 0966ba13-8bbc-4283-919a-7675444409be
ms.tgt_platform: multiple
title: Méthode decompress de la classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 24495c94cca0eb6b99bc209cad8f25fac8f66896
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482984"
---
# <a name="uncompress-method-of-the-cim_datafile-class"></a><span data-ttu-id="43835-104">Méthode decompress de la \_ classe de fichier de fichier CIM</span><span class="sxs-lookup"><span data-stu-id="43835-104">Uncompress method of the CIM\_DataFile class</span></span>

<span data-ttu-id="43835-105">La méthode **decompress** décompresse le fichier de données logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="43835-105">The **Uncompress** method uncompresses the logical data file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="43835-106">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="43835-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="43835-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="43835-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="43835-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="43835-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="43835-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="43835-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="43835-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="43835-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="43835-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43835-111">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="43835-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43835-112">Parameters</span></span>

<span data-ttu-id="43835-113">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="43835-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43835-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43835-114">Return value</span></span>

<span data-ttu-id="43835-115">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="43835-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="43835-116">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="43835-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="43835-117">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="43835-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="43835-118">**0**</span><span class="sxs-lookup"><span data-stu-id="43835-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="43835-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="43835-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="43835-120">**2**</span><span class="sxs-lookup"><span data-stu-id="43835-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="43835-121">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="43835-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="43835-122">**8**</span><span class="sxs-lookup"><span data-stu-id="43835-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="43835-123">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="43835-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="43835-124">**9**</span><span class="sxs-lookup"><span data-stu-id="43835-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="43835-125">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="43835-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="43835-126">**10**</span><span class="sxs-lookup"><span data-stu-id="43835-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="43835-127">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="43835-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="43835-128">**11**</span><span class="sxs-lookup"><span data-stu-id="43835-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="43835-129">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="43835-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="43835-130">**12**</span><span class="sxs-lookup"><span data-stu-id="43835-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="43835-131">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="43835-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="43835-132">**13**</span><span class="sxs-lookup"><span data-stu-id="43835-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="43835-133">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="43835-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="43835-134">**14**</span><span class="sxs-lookup"><span data-stu-id="43835-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="43835-135">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="43835-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="43835-136">**15**</span><span class="sxs-lookup"><span data-stu-id="43835-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="43835-137">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="43835-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="43835-138">**16**</span><span class="sxs-lookup"><span data-stu-id="43835-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="43835-139">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="43835-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="43835-140">**17**</span><span class="sxs-lookup"><span data-stu-id="43835-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="43835-141">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="43835-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="43835-142">**21**</span><span class="sxs-lookup"><span data-stu-id="43835-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="43835-143">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="43835-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43835-144">Notes</span><span class="sxs-lookup"><span data-stu-id="43835-144">Remarks</span></span>

<span data-ttu-id="43835-145">La méthode de **décompression** du [**fichier de \_ fichier CIM**](cim-datafile.md) est implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="43835-145">The **Uncompress** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="43835-146">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="43835-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="43835-147">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="43835-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="43835-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43835-148">Requirements</span></span>



| <span data-ttu-id="43835-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43835-149">Requirement</span></span> | <span data-ttu-id="43835-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="43835-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43835-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43835-151">Minimum supported client</span></span><br/> | <span data-ttu-id="43835-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43835-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43835-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43835-153">Minimum supported server</span></span><br/> | <span data-ttu-id="43835-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43835-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43835-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="43835-155">Namespace</span></span><br/>                | <span data-ttu-id="43835-156">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="43835-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="43835-157">MOF</span><span class="sxs-lookup"><span data-stu-id="43835-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43835-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43835-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="43835-159">DLL</span><span class="sxs-lookup"><span data-stu-id="43835-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43835-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43835-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43835-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43835-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43835-162">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="43835-162">**CIM\_DataFile**</span></span>](uncompress-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="43835-163">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="43835-163">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="43835-164">Tâches WMI : fichiers et dossiers</span><span class="sxs-lookup"><span data-stu-id="43835-164">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="43835-165">**Constantes de droits d’accès aux fichiers et aux répertoires**</span><span class="sxs-lookup"><span data-stu-id="43835-165">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

