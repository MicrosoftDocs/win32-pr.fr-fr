---
description: Méthode DeleteEx de la classe CIM_DeviceFile-la méthode DeleteEx supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode Delete et est héritée de la \_ LOGICALFILE CIM.
ms.assetid: ef4d08cd-7287-47be-bcfc-edc248ac5c9b
ms.tgt_platform: multiple
title: Méthode DeleteEx de la classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e21fb57558d7704bf98740de8634bc91289e0038
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089596"
---
# <a name="deleteex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="93c9a-104">Méthode DeleteEx de la \_ classe CIM DeviceFile</span><span class="sxs-lookup"><span data-stu-id="93c9a-104">DeleteEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="93c9a-105">La méthode **DeleteEx** supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="93c9a-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="93c9a-106">Cette méthode est une version étendue de la méthode [**Delete**](delete-method-in-class-cim-devicefile.md) et est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="93c9a-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-devicefile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93c9a-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="93c9a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="93c9a-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="93c9a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="93c9a-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="93c9a-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="93c9a-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="93c9a-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="93c9a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93c9a-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="93c9a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93c9a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93c9a-113">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="93c9a-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93c9a-114">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="93c9a-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="93c9a-115">Ce paramètre a la valeur null si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="93c9a-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="93c9a-116">*StartFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93c9a-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93c9a-117">Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="93c9a-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="93c9a-118">En règle générale, le paramètre **StartFileName** est le paramètre **StopFileName** spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="93c9a-118">Typically, the **StartFileName** parameter is the **StopFileName** parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="93c9a-119">Si ce paramètre a la valeur null, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="93c9a-119">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93c9a-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="93c9a-120">Return value</span></span>

<span data-ttu-id="93c9a-121">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="93c9a-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="93c9a-122">0</span><span class="sxs-lookup"><span data-stu-id="93c9a-122">0</span></span>

<span data-ttu-id="93c9a-123">Réussite.</span><span class="sxs-lookup"><span data-stu-id="93c9a-123">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="93c9a-124">2</span><span class="sxs-lookup"><span data-stu-id="93c9a-124">2</span></span>

<span data-ttu-id="93c9a-125">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="93c9a-125">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="93c9a-126">8</span><span class="sxs-lookup"><span data-stu-id="93c9a-126">8</span></span>

<span data-ttu-id="93c9a-127">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="93c9a-127">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="93c9a-128">9</span><span class="sxs-lookup"><span data-stu-id="93c9a-128">9</span></span>

<span data-ttu-id="93c9a-129">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="93c9a-129">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="93c9a-130">10</span><span class="sxs-lookup"><span data-stu-id="93c9a-130">10</span></span>

<span data-ttu-id="93c9a-131">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="93c9a-131">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="93c9a-132">11</span><span class="sxs-lookup"><span data-stu-id="93c9a-132">11</span></span>

<span data-ttu-id="93c9a-133">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="93c9a-133">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="93c9a-134">12</span><span class="sxs-lookup"><span data-stu-id="93c9a-134">12</span></span>

<span data-ttu-id="93c9a-135">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="93c9a-135">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="93c9a-136">13</span><span class="sxs-lookup"><span data-stu-id="93c9a-136">13</span></span>

<span data-ttu-id="93c9a-137">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="93c9a-137">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="93c9a-138">14</span><span class="sxs-lookup"><span data-stu-id="93c9a-138">14</span></span>

<span data-ttu-id="93c9a-139">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="93c9a-139">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="93c9a-140">15</span><span class="sxs-lookup"><span data-stu-id="93c9a-140">15</span></span>

<span data-ttu-id="93c9a-141">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="93c9a-141">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="93c9a-142">16</span><span class="sxs-lookup"><span data-stu-id="93c9a-142">16</span></span>

<span data-ttu-id="93c9a-143">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="93c9a-143">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="93c9a-144">17</span><span class="sxs-lookup"><span data-stu-id="93c9a-144">17</span></span>

<span data-ttu-id="93c9a-145">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="93c9a-145">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="93c9a-146">21</span><span class="sxs-lookup"><span data-stu-id="93c9a-146">21</span></span>

<span data-ttu-id="93c9a-147">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="93c9a-147">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93c9a-148">Notes </span><span class="sxs-lookup"><span data-stu-id="93c9a-148">Remarks</span></span>

<span data-ttu-id="93c9a-149">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="93c9a-149">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="93c9a-150">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="93c9a-150">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="93c9a-151">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="93c9a-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="93c9a-152">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="93c9a-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="93c9a-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93c9a-153">Requirements</span></span>



| <span data-ttu-id="93c9a-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93c9a-154">Requirement</span></span> | <span data-ttu-id="93c9a-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="93c9a-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93c9a-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93c9a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="93c9a-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93c9a-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93c9a-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93c9a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="93c9a-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93c9a-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93c9a-160">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="93c9a-160">Namespace</span></span><br/>                | <span data-ttu-id="93c9a-161">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="93c9a-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="93c9a-162">MOF</span><span class="sxs-lookup"><span data-stu-id="93c9a-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93c9a-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93c9a-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="93c9a-164">DLL</span><span class="sxs-lookup"><span data-stu-id="93c9a-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93c9a-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93c9a-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93c9a-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93c9a-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93c9a-167">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="93c9a-167">CIM\_DeviceFile</span></span>](deleteex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="93c9a-168">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="93c9a-168">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

