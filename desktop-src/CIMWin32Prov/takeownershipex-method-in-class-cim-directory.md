---
description: Obtient la propriété du fichier d’entrée de répertoire logique spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode TakeOwnerShip et est héritée de CIM \_ LogicalFile.
ms.assetid: a13acaa2-2203-470a-b989-15f8276e46c6
ms.tgt_platform: multiple
title: Méthode TakeOwnerShipEx de la classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b02a6c40e99405c150a372f8eb15fe648f2df60a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110170"
---
# <a name="takeownershipex-method-of-the-cim_directory-class"></a><span data-ttu-id="e425f-104">Méthode TakeOwnerShipEx de la \_ classe de répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="e425f-104">TakeOwnerShipEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="e425f-105">La méthode **TakeOwnerShipEx** obtient la propriété du fichier d’entrée de répertoire logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e425f-105">The **TakeOwnerShipEx** method obtains ownership of the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="e425f-106">Cette méthode est une version étendue de la méthode [**TakeOwnership**](takeownership-method-in-class-cim-directory.md) et est héritée de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="e425f-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="e425f-107">Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en prenant possession de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="e425f-107">If the logical file is a directory, then this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e425f-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e425f-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e425f-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e425f-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e425f-110">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="e425f-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e425f-111">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e425f-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e425f-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e425f-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="e425f-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e425f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e425f-114">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e425f-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e425f-115">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="e425f-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="e425f-116">Ce paramètre a la valeur null si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="e425f-116">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="e425f-117">*StartFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e425f-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e425f-118">Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e425f-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="e425f-119">En général, ce paramètre est le paramètre *StopFileName* qui spécifie le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="e425f-119">Typically, this parameter is the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="e425f-120">Si ce paramètre a la valeur null, l’opération est effectuée sur le fichier (ou le répertoire) spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="e425f-120">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="e425f-121">*Récursif* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e425f-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e425f-122">Si la **valeur est true**, la méthode est appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance de [**\_ répertoire CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="e425f-122">If **True**, the method is applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="e425f-123">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="e425f-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e425f-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e425f-124">Return value</span></span>

<span data-ttu-id="e425f-125">Retourne la valeur 0 en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="e425f-125">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="e425f-126">0</span><span class="sxs-lookup"><span data-stu-id="e425f-126">0</span></span>

<span data-ttu-id="e425f-127">Réussite.</span><span class="sxs-lookup"><span data-stu-id="e425f-127">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e425f-128">2</span><span class="sxs-lookup"><span data-stu-id="e425f-128">2</span></span>

<span data-ttu-id="e425f-129">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="e425f-129">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e425f-130">8</span><span class="sxs-lookup"><span data-stu-id="e425f-130">8</span></span>

<span data-ttu-id="e425f-131">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="e425f-131">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e425f-132">9</span><span class="sxs-lookup"><span data-stu-id="e425f-132">9</span></span>

<span data-ttu-id="e425f-133">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="e425f-133">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e425f-134">10</span><span class="sxs-lookup"><span data-stu-id="e425f-134">10</span></span>

<span data-ttu-id="e425f-135">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="e425f-135">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e425f-136">11</span><span class="sxs-lookup"><span data-stu-id="e425f-136">11</span></span>

<span data-ttu-id="e425f-137">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="e425f-137">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e425f-138">12</span><span class="sxs-lookup"><span data-stu-id="e425f-138">12</span></span>

<span data-ttu-id="e425f-139">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="e425f-139">The platform is not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e425f-140">13</span><span class="sxs-lookup"><span data-stu-id="e425f-140">13</span></span>

<span data-ttu-id="e425f-141">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="e425f-141">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e425f-142">14</span><span class="sxs-lookup"><span data-stu-id="e425f-142">14</span></span>

<span data-ttu-id="e425f-143">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="e425f-143">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e425f-144">15</span><span class="sxs-lookup"><span data-stu-id="e425f-144">15</span></span>

<span data-ttu-id="e425f-145">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="e425f-145">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e425f-146">16</span><span class="sxs-lookup"><span data-stu-id="e425f-146">16</span></span>

<span data-ttu-id="e425f-147">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="e425f-147">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e425f-148">17</span><span class="sxs-lookup"><span data-stu-id="e425f-148">17</span></span>

<span data-ttu-id="e425f-149">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="e425f-149">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e425f-150">21</span><span class="sxs-lookup"><span data-stu-id="e425f-150">21</span></span>

<span data-ttu-id="e425f-151">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="e425f-151">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e425f-152">Notes</span><span class="sxs-lookup"><span data-stu-id="e425f-152">Remarks</span></span>

<span data-ttu-id="e425f-153">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="e425f-153">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e425f-154">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e425f-154">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="e425f-155">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="e425f-155">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e425f-156">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e425f-156">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="examples"></a><span data-ttu-id="e425f-157">Exemples</span><span class="sxs-lookup"><span data-stu-id="e425f-157">Examples</span></span>

<span data-ttu-id="e425f-158">L’Visual Basic Code de script suivant appelle la méthode **TakeOwnerShipEx** pour prendre possession du dossier C : \\ temp.</span><span class="sxs-lookup"><span data-stu-id="e425f-158">The following Visual Basic Script code calls the **TakeOwnerShipEx** method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx"). _
    inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="e425f-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e425f-159">Requirements</span></span>



| <span data-ttu-id="e425f-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e425f-160">Requirement</span></span> | <span data-ttu-id="e425f-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="e425f-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e425f-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e425f-162">Minimum supported client</span></span><br/> | <span data-ttu-id="e425f-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e425f-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e425f-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e425f-164">Minimum supported server</span></span><br/> | <span data-ttu-id="e425f-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e425f-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e425f-166">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e425f-166">Namespace</span></span><br/>                | <span data-ttu-id="e425f-167">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e425f-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e425f-168">MOF</span><span class="sxs-lookup"><span data-stu-id="e425f-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e425f-169"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e425f-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e425f-170">DLL</span><span class="sxs-lookup"><span data-stu-id="e425f-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e425f-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e425f-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e425f-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e425f-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e425f-173">\_Répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="e425f-173">CIM\_Directory</span></span>](takeownershipex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="e425f-174">**\_Répertoire CIM**</span><span class="sxs-lookup"><span data-stu-id="e425f-174">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

