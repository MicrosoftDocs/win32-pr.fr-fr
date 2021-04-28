---
description: Méthode TakeOwnerShip de la classe CIM_DeviceFile-la méthode TakeOwnerShip obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.
ms.assetid: ef7d5ce7-99fb-464f-9739-ec9189148f94
ms.tgt_platform: multiple
title: Méthode TakeOwnerShip de la classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e7c745df18e1725199c4027d22882a00f6143a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086047"
---
# <a name="takeownership-method-of-the-cim_devicefile-class"></a><span data-ttu-id="c81e7-103">Méthode TakeOwnerShip de la \_ classe CIM DeviceFile</span><span class="sxs-lookup"><span data-stu-id="c81e7-103">TakeOwnerShip method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="c81e7-104">La méthode **TakeOwnership** obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c81e7-104">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="c81e7-105">Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en prenant possession de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="c81e7-105">If the logical file is a directory, then this method will act recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="c81e7-106">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c81e7-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c81e7-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="c81e7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c81e7-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c81e7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c81e7-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c81e7-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c81e7-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c81e7-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c81e7-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c81e7-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="c81e7-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c81e7-112">Parameters</span></span>

<span data-ttu-id="c81e7-113">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c81e7-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c81e7-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c81e7-114">Return value</span></span>

<span data-ttu-id="c81e7-115">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="c81e7-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c81e7-116">**0**</span><span class="sxs-lookup"><span data-stu-id="c81e7-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c81e7-117">Réussite.</span><span class="sxs-lookup"><span data-stu-id="c81e7-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="c81e7-118">**2**</span><span class="sxs-lookup"><span data-stu-id="c81e7-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c81e7-119">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="c81e7-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="c81e7-120">**8**</span><span class="sxs-lookup"><span data-stu-id="c81e7-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c81e7-121">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="c81e7-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="c81e7-122">**9**</span><span class="sxs-lookup"><span data-stu-id="c81e7-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c81e7-123">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="c81e7-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="c81e7-124">**10**</span><span class="sxs-lookup"><span data-stu-id="c81e7-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c81e7-125">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="c81e7-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c81e7-126">**11**</span><span class="sxs-lookup"><span data-stu-id="c81e7-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c81e7-127">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="c81e7-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c81e7-128">**12**</span><span class="sxs-lookup"><span data-stu-id="c81e7-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c81e7-129">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="c81e7-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c81e7-130">**13**</span><span class="sxs-lookup"><span data-stu-id="c81e7-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c81e7-131">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="c81e7-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c81e7-132">**14**</span><span class="sxs-lookup"><span data-stu-id="c81e7-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c81e7-133">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="c81e7-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c81e7-134">**15**</span><span class="sxs-lookup"><span data-stu-id="c81e7-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c81e7-135">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="c81e7-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c81e7-136">**16**</span><span class="sxs-lookup"><span data-stu-id="c81e7-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c81e7-137">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="c81e7-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="c81e7-138">**17**</span><span class="sxs-lookup"><span data-stu-id="c81e7-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c81e7-139">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="c81e7-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="c81e7-140">**21**</span><span class="sxs-lookup"><span data-stu-id="c81e7-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c81e7-141">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="c81e7-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c81e7-142">Notes </span><span class="sxs-lookup"><span data-stu-id="c81e7-142">Remarks</span></span>

<span data-ttu-id="c81e7-143">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="c81e7-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c81e7-144">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c81e7-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c81e7-145">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="c81e7-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c81e7-146">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="c81e7-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c81e7-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c81e7-147">Requirements</span></span>



| <span data-ttu-id="c81e7-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c81e7-148">Requirement</span></span> | <span data-ttu-id="c81e7-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="c81e7-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c81e7-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c81e7-150">Minimum supported client</span></span><br/> | <span data-ttu-id="c81e7-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c81e7-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c81e7-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c81e7-152">Minimum supported server</span></span><br/> | <span data-ttu-id="c81e7-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c81e7-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c81e7-154">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c81e7-154">Namespace</span></span><br/>                | <span data-ttu-id="c81e7-155">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="c81e7-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c81e7-156">MOF</span><span class="sxs-lookup"><span data-stu-id="c81e7-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c81e7-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c81e7-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c81e7-158">DLL</span><span class="sxs-lookup"><span data-stu-id="c81e7-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c81e7-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c81e7-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c81e7-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c81e7-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c81e7-161">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="c81e7-161">CIM\_DeviceFile</span></span>](takeownership-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="c81e7-162">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="c81e7-162">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

