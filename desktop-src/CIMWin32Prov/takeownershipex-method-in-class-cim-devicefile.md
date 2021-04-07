---
description: Obtient la propriété du fichier d’unité logique spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode TakeOwnerShip et est héritée de CIM \_ LogicalFile.
ms.assetid: 084f755a-e837-4d21-8bd2-0f63f80302fc
ms.tgt_platform: multiple
title: Méthode TakeOwnerShipEx de la classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3c36239d7d0ea6b0bf3bfa67bfb2f59617ab209a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847046"
---
# <a name="takeownershipex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="0946c-104">Méthode TakeOwnerShipEx de la \_ classe CIM DeviceFile</span><span class="sxs-lookup"><span data-stu-id="0946c-104">TakeOwnerShipEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="0946c-105">La méthode **TakeOwnerShipEx** obtient la propriété du fichier d’unité logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0946c-105">The **TakeOwnerShipEx** method obtains ownership of the logical device file specified in the object path.</span></span> <span data-ttu-id="0946c-106">Cette méthode est une version étendue de la méthode [**TakeOwnership**](takeownership-method-in-class-cim-devicefile.md) et est héritée de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="0946c-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-devicefile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="0946c-107">Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en prenant possession de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="0946c-107">If the logical file is a directory, then this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0946c-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="0946c-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0946c-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0946c-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0946c-110">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="0946c-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0946c-111">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0946c-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0946c-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0946c-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="0946c-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0946c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0946c-114">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0946c-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0946c-115">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="0946c-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="0946c-116">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="0946c-116">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0946c-117">*StartFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0946c-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0946c-118">Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="0946c-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="0946c-119">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="0946c-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="0946c-120">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="0946c-120">If this parameter is **null**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="0946c-121">*Récursif* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0946c-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0946c-122">Si la **valeur est true**, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ DeviceFile**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="0946c-122">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="0946c-123">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="0946c-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0946c-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0946c-124">Return value</span></span>

<span data-ttu-id="0946c-125">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="0946c-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="0946c-126">0</span><span class="sxs-lookup"><span data-stu-id="0946c-126">0</span></span>

<span data-ttu-id="0946c-127">Réussite.</span><span class="sxs-lookup"><span data-stu-id="0946c-127">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0946c-128">2</span><span class="sxs-lookup"><span data-stu-id="0946c-128">2</span></span>

<span data-ttu-id="0946c-129">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="0946c-129">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0946c-130">8</span><span class="sxs-lookup"><span data-stu-id="0946c-130">8</span></span>

<span data-ttu-id="0946c-131">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="0946c-131">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0946c-132">9</span><span class="sxs-lookup"><span data-stu-id="0946c-132">9</span></span>

<span data-ttu-id="0946c-133">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="0946c-133">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0946c-134">10</span><span class="sxs-lookup"><span data-stu-id="0946c-134">10</span></span>

<span data-ttu-id="0946c-135">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="0946c-135">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0946c-136">11</span><span class="sxs-lookup"><span data-stu-id="0946c-136">11</span></span>

<span data-ttu-id="0946c-137">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="0946c-137">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0946c-138">12</span><span class="sxs-lookup"><span data-stu-id="0946c-138">12</span></span>

<span data-ttu-id="0946c-139">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="0946c-139">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0946c-140">13</span><span class="sxs-lookup"><span data-stu-id="0946c-140">13</span></span>

<span data-ttu-id="0946c-141">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="0946c-141">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0946c-142">14</span><span class="sxs-lookup"><span data-stu-id="0946c-142">14</span></span>

<span data-ttu-id="0946c-143">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="0946c-143">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0946c-144">15</span><span class="sxs-lookup"><span data-stu-id="0946c-144">15</span></span>

<span data-ttu-id="0946c-145">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="0946c-145">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0946c-146">16</span><span class="sxs-lookup"><span data-stu-id="0946c-146">16</span></span>

<span data-ttu-id="0946c-147">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="0946c-147">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0946c-148">17</span><span class="sxs-lookup"><span data-stu-id="0946c-148">17</span></span>

<span data-ttu-id="0946c-149">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="0946c-149">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0946c-150">21</span><span class="sxs-lookup"><span data-stu-id="0946c-150">21</span></span>

<span data-ttu-id="0946c-151">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="0946c-151">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0946c-152">Notes</span><span class="sxs-lookup"><span data-stu-id="0946c-152">Remarks</span></span>

<span data-ttu-id="0946c-153">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="0946c-153">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0946c-154">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0946c-154">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0946c-155">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="0946c-155">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0946c-156">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0946c-156">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0946c-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0946c-157">Requirements</span></span>



| <span data-ttu-id="0946c-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0946c-158">Requirement</span></span> | <span data-ttu-id="0946c-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="0946c-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0946c-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0946c-160">Minimum supported client</span></span><br/> | <span data-ttu-id="0946c-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0946c-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0946c-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0946c-162">Minimum supported server</span></span><br/> | <span data-ttu-id="0946c-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0946c-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0946c-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0946c-164">Namespace</span></span><br/>                | <span data-ttu-id="0946c-165">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0946c-165">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0946c-166">MOF</span><span class="sxs-lookup"><span data-stu-id="0946c-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0946c-167"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0946c-167"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0946c-168">DLL</span><span class="sxs-lookup"><span data-stu-id="0946c-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0946c-169"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0946c-169"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0946c-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0946c-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0946c-171">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="0946c-171">CIM\_DeviceFile</span></span>](takeownershipex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="0946c-172">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="0946c-172">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

