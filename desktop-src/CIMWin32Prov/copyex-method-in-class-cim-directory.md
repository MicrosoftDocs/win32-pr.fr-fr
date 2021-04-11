---
description: La méthode CopyEx copie le fichier logique (ou le répertoire) spécifié dans le chemin de l’objet vers l’emplacement spécifié par le paramètre FileName. Cette méthode est une version étendue de la méthode de copie et est héritée de la \_ LOGICALFILE CIM.
ms.assetid: e207cc80-055e-41bc-ab80-dc50131b544d
ms.tgt_platform: multiple
title: Méthode CopyEx de la classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d7502c46c616d9b8e1fffeebf5aefcd022dd4cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950484"
---
# <a name="copyex-method-of-the-cim_directory-class"></a><span data-ttu-id="ff07a-104">Méthode CopyEx de la \_ classe de répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="ff07a-104">CopyEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="ff07a-105">La méthode **CopyEx** copie le fichier logique (ou le répertoire) spécifié dans le chemin de l’objet vers l’emplacement spécifié par le paramètre *filename* .</span><span class="sxs-lookup"><span data-stu-id="ff07a-105">The **CopyEx** method copies the logical file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="ff07a-106">Cette méthode est une version étendue de la méthode de [**copie**](copy-method-in-class-cim-directory.md) et est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ff07a-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff07a-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="ff07a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ff07a-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ff07a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ff07a-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ff07a-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ff07a-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ff07a-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff07a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff07a-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string REF FileName,
  [out] string     StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="ff07a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff07a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff07a-113">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff07a-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff07a-114">Nom complet de la copie du fichier de destination (ou répertoire).</span><span class="sxs-lookup"><span data-stu-id="ff07a-114">Fully qualified name of the copy of the destination file (or directory).</span></span>

<span data-ttu-id="ff07a-115">Exemple : « c : \\ temp \\ newDirectory »</span><span class="sxs-lookup"><span data-stu-id="ff07a-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="ff07a-116">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ff07a-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff07a-117">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="ff07a-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="ff07a-118">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="ff07a-118">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="ff07a-119">*StartFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff07a-119">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff07a-120">Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="ff07a-120">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="ff07a-121">En général, ce paramètre est le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="ff07a-121">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="ff07a-122">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier (ou le répertoire) spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="ff07a-122">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="ff07a-123">*Récursif* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff07a-123">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff07a-124">Si la valeur est TRUE, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance de [**\_ répertoire CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="ff07a-124">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="ff07a-125">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ff07a-125">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff07a-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ff07a-126">Return value</span></span>

<span data-ttu-id="ff07a-127">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="ff07a-127">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="ff07a-128">0</span><span class="sxs-lookup"><span data-stu-id="ff07a-128">0</span></span>

<span data-ttu-id="ff07a-129">Réussite.</span><span class="sxs-lookup"><span data-stu-id="ff07a-129">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff07a-130">2</span><span class="sxs-lookup"><span data-stu-id="ff07a-130">2</span></span>

<span data-ttu-id="ff07a-131">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="ff07a-131">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff07a-132">8</span><span class="sxs-lookup"><span data-stu-id="ff07a-132">8</span></span>

<span data-ttu-id="ff07a-133">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="ff07a-133">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff07a-134">9</span><span class="sxs-lookup"><span data-stu-id="ff07a-134">9</span></span>

<span data-ttu-id="ff07a-135">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="ff07a-135">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff07a-136">10</span><span class="sxs-lookup"><span data-stu-id="ff07a-136">10</span></span>

<span data-ttu-id="ff07a-137">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="ff07a-137">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff07a-138">11</span><span class="sxs-lookup"><span data-stu-id="ff07a-138">11</span></span>

<span data-ttu-id="ff07a-139">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="ff07a-139">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff07a-140">12</span><span class="sxs-lookup"><span data-stu-id="ff07a-140">12</span></span>

<span data-ttu-id="ff07a-141">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="ff07a-141">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff07a-142">13</span><span class="sxs-lookup"><span data-stu-id="ff07a-142">13</span></span>

<span data-ttu-id="ff07a-143">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="ff07a-143">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff07a-144">14</span><span class="sxs-lookup"><span data-stu-id="ff07a-144">14</span></span>

<span data-ttu-id="ff07a-145">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="ff07a-145">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff07a-146">15</span><span class="sxs-lookup"><span data-stu-id="ff07a-146">15</span></span>

<span data-ttu-id="ff07a-147">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="ff07a-147">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff07a-148">16</span><span class="sxs-lookup"><span data-stu-id="ff07a-148">16</span></span>

<span data-ttu-id="ff07a-149">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="ff07a-149">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff07a-150">17</span><span class="sxs-lookup"><span data-stu-id="ff07a-150">17</span></span>

<span data-ttu-id="ff07a-151">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="ff07a-151">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff07a-152">21</span><span class="sxs-lookup"><span data-stu-id="ff07a-152">21</span></span>

<span data-ttu-id="ff07a-153">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="ff07a-153">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff07a-154">Notes</span><span class="sxs-lookup"><span data-stu-id="ff07a-154">Remarks</span></span>

<span data-ttu-id="ff07a-155">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="ff07a-155">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ff07a-156">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ff07a-156">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ff07a-157">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="ff07a-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ff07a-158">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ff07a-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff07a-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff07a-159">Requirements</span></span>



| <span data-ttu-id="ff07a-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff07a-160">Requirement</span></span> | <span data-ttu-id="ff07a-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff07a-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff07a-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff07a-162">Minimum supported client</span></span><br/> | <span data-ttu-id="ff07a-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff07a-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ff07a-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff07a-164">Minimum supported server</span></span><br/> | <span data-ttu-id="ff07a-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff07a-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ff07a-166">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ff07a-166">Namespace</span></span><br/>                | <span data-ttu-id="ff07a-167">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ff07a-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ff07a-168">MOF</span><span class="sxs-lookup"><span data-stu-id="ff07a-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff07a-169"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff07a-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff07a-170">DLL</span><span class="sxs-lookup"><span data-stu-id="ff07a-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff07a-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff07a-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff07a-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff07a-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff07a-173">\_Répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="ff07a-173">CIM\_Directory</span></span>](copyex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="ff07a-174">**\_Répertoire CIM**</span><span class="sxs-lookup"><span data-stu-id="ff07a-174">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

