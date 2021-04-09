---
description: Renomme le fichier d’appareil (ou le répertoire) spécifié dans le chemin d’accès de l’objet.
ms.assetid: 48c2eab3-c76d-4e4b-927e-dbb17584cccd
ms.tgt_platform: multiple
title: Renommer la méthode de la classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 484d66a1b98ea58b7cb5de25c8f7d15065ce905b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111254"
---
# <a name="rename-method-of-the-cim_devicefile-class"></a><span data-ttu-id="3b1b8-103">Renommer la méthode de la \_ classe CIM DeviceFile</span><span class="sxs-lookup"><span data-stu-id="3b1b8-103">Rename method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="3b1b8-104">La méthode **Rename** renomme le fichier d’appareil (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-104">The **Rename** method renames the device file (or directory) specified in the object path.</span></span> <span data-ttu-id="3b1b8-105">Le changement de nom n’est pas pris en charge si la destination se trouve sur un autre lecteur ou si le remplacement d’un fichier logique existant est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-105">Renaming is not supported if the destination is on another drive or overwriting an existing logical file is required.</span></span> <span data-ttu-id="3b1b8-106">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3b1b8-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b1b8-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3b1b8-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3b1b8-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3b1b8-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3b1b8-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3b1b8-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3b1b8-110">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b1b8-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b1b8-111">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="3b1b8-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b1b8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b1b8-113">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b1b8-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b1b8-114">Nouveau nom complet du fichier (ou répertoire).</span><span class="sxs-lookup"><span data-stu-id="3b1b8-114">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="3b1b8-115">Exemple : « c : \\ temp \\newfile.txt »</span><span class="sxs-lookup"><span data-stu-id="3b1b8-115">Example: "c:\\temp\\newfile.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b1b8-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b1b8-116">Return value</span></span>

<span data-ttu-id="3b1b8-117">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3b1b8-118">**0**</span><span class="sxs-lookup"><span data-stu-id="3b1b8-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3b1b8-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="3b1b8-120">**2**</span><span class="sxs-lookup"><span data-stu-id="3b1b8-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3b1b8-121">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="3b1b8-122">**8**</span><span class="sxs-lookup"><span data-stu-id="3b1b8-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3b1b8-123">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="3b1b8-124">**9**</span><span class="sxs-lookup"><span data-stu-id="3b1b8-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3b1b8-125">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="3b1b8-126">**10**</span><span class="sxs-lookup"><span data-stu-id="3b1b8-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3b1b8-127">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3b1b8-128">**11**</span><span class="sxs-lookup"><span data-stu-id="3b1b8-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3b1b8-129">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="3b1b8-130">**12**</span><span class="sxs-lookup"><span data-stu-id="3b1b8-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3b1b8-131">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3b1b8-132">**13**</span><span class="sxs-lookup"><span data-stu-id="3b1b8-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3b1b8-133">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3b1b8-134">**14**</span><span class="sxs-lookup"><span data-stu-id="3b1b8-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3b1b8-135">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3b1b8-136">**15**</span><span class="sxs-lookup"><span data-stu-id="3b1b8-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3b1b8-137">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3b1b8-138">**16**</span><span class="sxs-lookup"><span data-stu-id="3b1b8-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3b1b8-139">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="3b1b8-140">**17**</span><span class="sxs-lookup"><span data-stu-id="3b1b8-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3b1b8-141">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="3b1b8-142">**21**</span><span class="sxs-lookup"><span data-stu-id="3b1b8-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3b1b8-143">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b1b8-144">Notes</span><span class="sxs-lookup"><span data-stu-id="3b1b8-144">Remarks</span></span>

<span data-ttu-id="3b1b8-145">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3b1b8-146">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3b1b8-147">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3b1b8-148">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="3b1b8-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b1b8-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b1b8-149">Requirements</span></span>



| <span data-ttu-id="3b1b8-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b1b8-150">Requirement</span></span> | <span data-ttu-id="3b1b8-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b1b8-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b1b8-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b1b8-152">Minimum supported client</span></span><br/> | <span data-ttu-id="3b1b8-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b1b8-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b1b8-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b1b8-154">Minimum supported server</span></span><br/> | <span data-ttu-id="3b1b8-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b1b8-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b1b8-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3b1b8-156">Namespace</span></span><br/>                | <span data-ttu-id="3b1b8-157">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3b1b8-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3b1b8-158">MOF</span><span class="sxs-lookup"><span data-stu-id="3b1b8-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b1b8-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b1b8-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b1b8-160">DLL</span><span class="sxs-lookup"><span data-stu-id="3b1b8-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b1b8-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b1b8-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b1b8-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b1b8-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b1b8-163">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="3b1b8-163">CIM\_DeviceFile</span></span>](rename-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="3b1b8-164">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="3b1b8-164">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

