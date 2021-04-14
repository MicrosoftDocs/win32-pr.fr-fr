---
title: Classe Win32_RDMSFileTypeAssociation
description: Gère une association de types de fichiers pour une application publiée.
ms.assetid: 22c945cb-4c47-431a-bc9b-d33ba15c8ab3
ms.tgt_platform: multiple
keywords:
- Win32_RDMSFileTypeAssociation de la classe Services Bureau à distance
- Win32_RDMSFileTypeAssociation de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSFileTypeAssociation
- Win32_RDMSFileTypeAssociation.AppAlias
- Win32_RDMSFileTypeAssociation.PoolName
- Win32_RDMSFileTypeAssociation.ExtName
- Win32_RDMSFileTypeAssociation.ProgIdHint
- Win32_RDMSFileTypeAssociation.IconPath
- Win32_RDMSFileTypeAssociation.IconIndex
- Win32_RDMSFileTypeAssociation.IconContents
- Win32_RDMSFileTypeAssociation.IsPrimaryHandler
- Win32_RDMSFileTypeAssociation.IsPublished
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2e569077bf47a2b0eba63db39ae1e86c39feb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383964"
---
# <a name="win32_rdmsfiletypeassociation-class"></a><span data-ttu-id="72d35-105">\_Classe RDMSFileTypeAssociation Win32</span><span class="sxs-lookup"><span data-stu-id="72d35-105">Win32\_RDMSFileTypeAssociation class</span></span>

<span data-ttu-id="72d35-106">Gère une association de types de fichiers pour une application publiée.</span><span class="sxs-lookup"><span data-stu-id="72d35-106">Manages a file type association for a published application.</span></span>

<span data-ttu-id="72d35-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="72d35-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="72d35-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72d35-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSFileTypeAssociation
{
  string  AppAlias;
  string  PoolName;
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean IsPrimaryHandler;
  boolean IsPublished;
};
```

## <a name="members"></a><span data-ttu-id="72d35-109">Membres</span><span class="sxs-lookup"><span data-stu-id="72d35-109">Members</span></span>

<span data-ttu-id="72d35-110">La classe **Win32 \_ RDMSFileTypeAssociation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="72d35-110">The **Win32\_RDMSFileTypeAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="72d35-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="72d35-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72d35-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="72d35-112">Properties</span></span>

<span data-ttu-id="72d35-113">La classe **Win32 \_ RDMSFileTypeAssociation** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="72d35-113">The **Win32\_RDMSFileTypeAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72d35-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="72d35-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72d35-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="72d35-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72d35-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="72d35-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="72d35-117">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="72d35-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="72d35-118">Obtient et définit l’alias de l’application associée au type de fichier.</span><span class="sxs-lookup"><span data-stu-id="72d35-118">Gets and sets the alias of the application that is associated with the file type.</span></span>

</dd> <dt>

<span data-ttu-id="72d35-119">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="72d35-119">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72d35-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="72d35-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72d35-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72d35-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72d35-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="72d35-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="72d35-123">Obtient le nom de l’extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="72d35-123">Gets the name of the file extension.</span></span>

</dd> <dt>

<span data-ttu-id="72d35-124">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="72d35-124">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72d35-125">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="72d35-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="72d35-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="72d35-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="72d35-127">Obtient et définit le contenu de l’icône pour le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="72d35-127">Gets and sets the content of the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="72d35-128">**IndexIcône**</span><span class="sxs-lookup"><span data-stu-id="72d35-128">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72d35-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="72d35-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72d35-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="72d35-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="72d35-131">Obtient et définit l’index de l’icône pour le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="72d35-131">Gets and sets the index to the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="72d35-132">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="72d35-132">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72d35-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="72d35-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72d35-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="72d35-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="72d35-135">Obtient et définit le chemin d’accès à l’icône pour le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="72d35-135">Gets and sets the path to the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="72d35-136">**IsPrimaryHandler**</span><span class="sxs-lookup"><span data-stu-id="72d35-136">**IsPrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72d35-137">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="72d35-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="72d35-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="72d35-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="72d35-139">Obtient et définit une valeur qui indique si l’Association de type de fichier est pour le gestionnaire principal.</span><span class="sxs-lookup"><span data-stu-id="72d35-139">Gets and sets a value that indicates whether the file type association is for the primary handler.</span></span> <span data-ttu-id="72d35-140">**True** si l’Association de types de fichiers est destinée au gestionnaire principal ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="72d35-140">**TRUE** if the file type association is for the primary handler; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="72d35-141">**IsPublished**</span><span class="sxs-lookup"><span data-stu-id="72d35-141">**IsPublished**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72d35-142">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="72d35-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="72d35-143">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="72d35-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="72d35-144">Indique si ce Association est publié.</span><span class="sxs-lookup"><span data-stu-id="72d35-144">Whether this FTA is published.</span></span>

<span data-ttu-id="72d35-145">Obtient et définit une valeur qui indique si l’Association de types de fichiers est publiée.</span><span class="sxs-lookup"><span data-stu-id="72d35-145">Gets and sets a value that indicates whether the file type association is published.</span></span> <span data-ttu-id="72d35-146">**True** si l’Association de types de fichiers est publiée ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="72d35-146">**TRUE** if the file type association is published; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="72d35-147">**PoolName**</span><span class="sxs-lookup"><span data-stu-id="72d35-147">**PoolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72d35-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="72d35-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72d35-149">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="72d35-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="72d35-150">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="72d35-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="72d35-151">Obtient et définit le nom du pool d’applications pour l’Association de types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="72d35-151">Gets and sets the name of the application pool for the file type association.</span></span>

</dd> <dt>

<span data-ttu-id="72d35-152">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="72d35-152">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72d35-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="72d35-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72d35-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72d35-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72d35-155">Obtient un indicateur pour aider les utilisateurs à ouvrir l’extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="72d35-155">Gets a hint to help users open the file extension.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72d35-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72d35-156">Requirements</span></span>



| <span data-ttu-id="72d35-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72d35-157">Requirement</span></span> | <span data-ttu-id="72d35-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="72d35-158">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="72d35-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72d35-159">Minimum supported client</span></span><br/> | <span data-ttu-id="72d35-160">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="72d35-160">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="72d35-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72d35-161">Minimum supported server</span></span><br/> | <span data-ttu-id="72d35-162">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72d35-162">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="72d35-163">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="72d35-163">Namespace</span></span><br/>                | <span data-ttu-id="72d35-164">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="72d35-164">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="72d35-165">MOF</span><span class="sxs-lookup"><span data-stu-id="72d35-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72d35-166"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72d35-166"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="72d35-167">DLL</span><span class="sxs-lookup"><span data-stu-id="72d35-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72d35-168"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72d35-168"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="72d35-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72d35-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d35-170">Fournisseur de services de gestion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="72d35-170">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

