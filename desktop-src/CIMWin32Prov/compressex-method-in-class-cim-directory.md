---
description: La méthode CompressEx compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode Compress et est héritée de la \_ LOGICALFILE CIM.
ms.assetid: 82a28a3b-b2e4-4834-b4a5-02ffe94f3fc7
ms.tgt_platform: multiple
title: Méthode CompressEx de la classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8bebd729d87e012c3fce6dd2eb87b1c61ffa423a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523100"
---
# <a name="compressex-method-of-the-cim_directory-class"></a><span data-ttu-id="9d95a-104">Méthode CompressEx de la \_ classe de répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="9d95a-104">CompressEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="9d95a-105">La méthode **CompressEx** compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9d95a-105">The **CompressEx** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="9d95a-106">Cette méthode est une version étendue de la méthode [**Compress**](compress-method-in-class-cim-directory.md) et est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="9d95a-106">This method is an extended version of the [**Compress**](compress-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9d95a-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="9d95a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9d95a-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9d95a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9d95a-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="9d95a-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9d95a-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9d95a-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d95a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d95a-111">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="9d95a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d95a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d95a-113">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9d95a-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d95a-114">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="9d95a-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="9d95a-115">Ce paramètre a la valeur null si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="9d95a-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="9d95a-116">*StartFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9d95a-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d95a-117">Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9d95a-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="9d95a-118">En général, ce paramètre est le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="9d95a-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="9d95a-119">Si ce paramètre a la valeur null, l’opération est effectuée sur le fichier (ou le répertoire) spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="9d95a-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="9d95a-120">*Récursif* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9d95a-120">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d95a-121">Si la **valeur est true**, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance de [**\_ répertoire CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="9d95a-121">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="9d95a-122">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="9d95a-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d95a-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d95a-123">Return value</span></span>

<span data-ttu-id="9d95a-124">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="9d95a-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="9d95a-125">0</span><span class="sxs-lookup"><span data-stu-id="9d95a-125">0</span></span>

<span data-ttu-id="9d95a-126">Réussite.</span><span class="sxs-lookup"><span data-stu-id="9d95a-126">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9d95a-127">2</span><span class="sxs-lookup"><span data-stu-id="9d95a-127">2</span></span>

<span data-ttu-id="9d95a-128">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="9d95a-128">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9d95a-129">8</span><span class="sxs-lookup"><span data-stu-id="9d95a-129">8</span></span>

<span data-ttu-id="9d95a-130">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="9d95a-130">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9d95a-131">9</span><span class="sxs-lookup"><span data-stu-id="9d95a-131">9</span></span>

<span data-ttu-id="9d95a-132">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="9d95a-132">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9d95a-133">10</span><span class="sxs-lookup"><span data-stu-id="9d95a-133">10</span></span>

<span data-ttu-id="9d95a-134">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="9d95a-134">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9d95a-135">11</span><span class="sxs-lookup"><span data-stu-id="9d95a-135">11</span></span>

<span data-ttu-id="9d95a-136">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="9d95a-136">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9d95a-137">12</span><span class="sxs-lookup"><span data-stu-id="9d95a-137">12</span></span>

<span data-ttu-id="9d95a-138">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="9d95a-138">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9d95a-139">13</span><span class="sxs-lookup"><span data-stu-id="9d95a-139">13</span></span>

<span data-ttu-id="9d95a-140">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="9d95a-140">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9d95a-141">14</span><span class="sxs-lookup"><span data-stu-id="9d95a-141">14</span></span>

<span data-ttu-id="9d95a-142">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="9d95a-142">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9d95a-143">15</span><span class="sxs-lookup"><span data-stu-id="9d95a-143">15</span></span>

<span data-ttu-id="9d95a-144">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="9d95a-144">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9d95a-145">16</span><span class="sxs-lookup"><span data-stu-id="9d95a-145">16</span></span>

<span data-ttu-id="9d95a-146">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="9d95a-146">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9d95a-147">17</span><span class="sxs-lookup"><span data-stu-id="9d95a-147">17</span></span>

<span data-ttu-id="9d95a-148">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="9d95a-148">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9d95a-149">21</span><span class="sxs-lookup"><span data-stu-id="9d95a-149">21</span></span>

<span data-ttu-id="9d95a-150">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="9d95a-150">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d95a-151">Notes</span><span class="sxs-lookup"><span data-stu-id="9d95a-151">Remarks</span></span>

<span data-ttu-id="9d95a-152">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="9d95a-152">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9d95a-153">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9d95a-153">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9d95a-154">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="9d95a-154">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9d95a-155">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9d95a-155">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d95a-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d95a-156">Requirements</span></span>



| <span data-ttu-id="9d95a-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d95a-157">Requirement</span></span> | <span data-ttu-id="9d95a-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d95a-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d95a-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d95a-159">Minimum supported client</span></span><br/> | <span data-ttu-id="9d95a-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d95a-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9d95a-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d95a-161">Minimum supported server</span></span><br/> | <span data-ttu-id="9d95a-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d95a-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9d95a-163">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9d95a-163">Namespace</span></span><br/>                | <span data-ttu-id="9d95a-164">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9d95a-164">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9d95a-165">MOF</span><span class="sxs-lookup"><span data-stu-id="9d95a-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d95a-166"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d95a-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d95a-167">DLL</span><span class="sxs-lookup"><span data-stu-id="9d95a-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d95a-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d95a-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d95a-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d95a-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d95a-170">\_Répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="9d95a-170">CIM\_Directory</span></span>](compressex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="9d95a-171">**\_Répertoire CIM**</span><span class="sxs-lookup"><span data-stu-id="9d95a-171">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

