---
description: Copie le fichier d’unité logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre FileName.
ms.assetid: 42cdb880-2431-4dcc-abdb-f271e2cd81a4
ms.tgt_platform: multiple
title: Méthode CopyEx de la classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0e9519155accadc1a41a1c91492755db90eec696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393096"
---
# <a name="copyex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="c61e8-103">Méthode CopyEx de la \_ classe CIM DeviceFile</span><span class="sxs-lookup"><span data-stu-id="c61e8-103">CopyEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="c61e8-104">La méthode **CopyEx** copie le fichier d’unité logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre *filename* .</span><span class="sxs-lookup"><span data-stu-id="c61e8-104">The **CopyEx** method copies the logical device file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="c61e8-105">Une copie n’est pas prise en charge si le remplacement d’un fichier logique existant est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c61e8-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="c61e8-106">Cette méthode est une version étendue de la méthode de [**copie**](copy-method-in-class-cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="c61e8-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-devicefile.md) method.</span></span> <span data-ttu-id="c61e8-107">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c61e8-107">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c61e8-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="c61e8-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c61e8-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c61e8-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c61e8-110">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c61e8-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c61e8-111">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c61e8-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c61e8-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c61e8-112">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="c61e8-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c61e8-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c61e8-114">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c61e8-114">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c61e8-115">Nom complet du fichier de destination (ou répertoire).</span><span class="sxs-lookup"><span data-stu-id="c61e8-115">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="c61e8-116">Exemple : « c : \\ temp \\ newDirectory »</span><span class="sxs-lookup"><span data-stu-id="c61e8-116">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="c61e8-117">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c61e8-117">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c61e8-118">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="c61e8-118">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="c61e8-119">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="c61e8-119">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="c61e8-120">*StartFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c61e8-120">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c61e8-121">Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c61e8-121">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="c61e8-122">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="c61e8-122">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="c61e8-123">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier (ou le répertoire) spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="c61e8-123">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="c61e8-124">*Récursif* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c61e8-124">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c61e8-125">Si la valeur est TRUE, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ DeviceFile**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="c61e8-125">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="c61e8-126">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="c61e8-126">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c61e8-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c61e8-127">Return value</span></span>

<span data-ttu-id="c61e8-128">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="c61e8-128">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="c61e8-129">0</span><span class="sxs-lookup"><span data-stu-id="c61e8-129">0</span></span>

<span data-ttu-id="c61e8-130">Réussite.</span><span class="sxs-lookup"><span data-stu-id="c61e8-130">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c61e8-131">2</span><span class="sxs-lookup"><span data-stu-id="c61e8-131">2</span></span>

<span data-ttu-id="c61e8-132">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="c61e8-132">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c61e8-133">8</span><span class="sxs-lookup"><span data-stu-id="c61e8-133">8</span></span>

<span data-ttu-id="c61e8-134">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="c61e8-134">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c61e8-135">9</span><span class="sxs-lookup"><span data-stu-id="c61e8-135">9</span></span>

<span data-ttu-id="c61e8-136">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="c61e8-136">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c61e8-137">10</span><span class="sxs-lookup"><span data-stu-id="c61e8-137">10</span></span>

<span data-ttu-id="c61e8-138">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="c61e8-138">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c61e8-139">11</span><span class="sxs-lookup"><span data-stu-id="c61e8-139">11</span></span>

<span data-ttu-id="c61e8-140">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="c61e8-140">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c61e8-141">12</span><span class="sxs-lookup"><span data-stu-id="c61e8-141">12</span></span>

<span data-ttu-id="c61e8-142">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="c61e8-142">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c61e8-143">13</span><span class="sxs-lookup"><span data-stu-id="c61e8-143">13</span></span>

<span data-ttu-id="c61e8-144">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="c61e8-144">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c61e8-145">14</span><span class="sxs-lookup"><span data-stu-id="c61e8-145">14</span></span>

<span data-ttu-id="c61e8-146">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="c61e8-146">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c61e8-147">15</span><span class="sxs-lookup"><span data-stu-id="c61e8-147">15</span></span>

<span data-ttu-id="c61e8-148">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="c61e8-148">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c61e8-149">16</span><span class="sxs-lookup"><span data-stu-id="c61e8-149">16</span></span>

<span data-ttu-id="c61e8-150">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="c61e8-150">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c61e8-151">17</span><span class="sxs-lookup"><span data-stu-id="c61e8-151">17</span></span>

<span data-ttu-id="c61e8-152">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="c61e8-152">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c61e8-153">21</span><span class="sxs-lookup"><span data-stu-id="c61e8-153">21</span></span>

<span data-ttu-id="c61e8-154">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="c61e8-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c61e8-155">Notes</span><span class="sxs-lookup"><span data-stu-id="c61e8-155">Remarks</span></span>

<span data-ttu-id="c61e8-156">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="c61e8-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c61e8-157">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c61e8-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c61e8-158">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="c61e8-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c61e8-159">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="c61e8-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c61e8-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c61e8-160">Requirements</span></span>



| <span data-ttu-id="c61e8-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c61e8-161">Requirement</span></span> | <span data-ttu-id="c61e8-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="c61e8-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c61e8-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c61e8-163">Minimum supported client</span></span><br/> | <span data-ttu-id="c61e8-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c61e8-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c61e8-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c61e8-165">Minimum supported server</span></span><br/> | <span data-ttu-id="c61e8-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c61e8-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c61e8-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c61e8-167">Namespace</span></span><br/>                | <span data-ttu-id="c61e8-168">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="c61e8-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c61e8-169">MOF</span><span class="sxs-lookup"><span data-stu-id="c61e8-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c61e8-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c61e8-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c61e8-171">DLL</span><span class="sxs-lookup"><span data-stu-id="c61e8-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c61e8-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c61e8-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c61e8-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c61e8-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c61e8-174">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="c61e8-174">CIM\_DeviceFile</span></span>](copyex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="c61e8-175">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="c61e8-175">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

