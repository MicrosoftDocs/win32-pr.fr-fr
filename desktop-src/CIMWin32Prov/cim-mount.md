---
description: La \_ classe Mount CIM représente une association entre un système de fichiers et un répertoire auquel elle est attachée.
ms.assetid: abf1833b-9b39-45c0-8400-2be2bf3a1c3c
ms.tgt_platform: multiple
title: Classe CIM_Mount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Mount
- CIM_Mount.Dependent
- CIM_Mount.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b86587466517a10302b3109a521e902a66892c4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110963"
---
# <a name="cim_mount-class"></a><span data-ttu-id="bda06-103">\_Classe Mount CIM</span><span class="sxs-lookup"><span data-stu-id="bda06-103">CIM\_Mount class</span></span>

<span data-ttu-id="bda06-104">La **classe \_ Mount CIM** représente une association entre un système de fichiers et un répertoire auquel elle est attachée.</span><span class="sxs-lookup"><span data-stu-id="bda06-104">The **CIM\_Mount** class represents an association between a file system and a directory to which it is attached.</span></span>

<span data-ttu-id="bda06-105">La sémantique de cette relation exige que le répertoire monté soit contenu dans un système de fichiers (via l’Association de stockage file) qui est différent du système de fichiers référencé comme dépendant.</span><span class="sxs-lookup"><span data-stu-id="bda06-105">The semantics of this relationship require that the mounted directory be contained by a file system (via the file storage association) that is different from the file system referenced as the dependent.</span></span> <span data-ttu-id="bda06-106">Le système de fichiers contenant le répertoire peut être local ou distant.</span><span class="sxs-lookup"><span data-stu-id="bda06-106">The directory's containing file system can be local or remote.</span></span> <span data-ttu-id="bda06-107">Par exemple, un système de fichiers local sur un système d’ordinateur Solaris peut monter un répertoire à partir du système de fichiers accessible via le lecteur de CD-ROM de l’ordinateur (autrement dit, un autre système de fichiers local).</span><span class="sxs-lookup"><span data-stu-id="bda06-107">For example, a local file system on a Solaris computer system can mount a directory from the file system accessed via the computer's CDROM drive (that is, another local file system).</span></span> <span data-ttu-id="bda06-108">En revanche, dans un cas « distant », le répertoire est d’abord exporté par son système de fichiers, qui est hébergé sur un autre système informatique, par exemple, en tant que serveur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="bda06-108">On the other hand, in a "remote" case, the directory is first exported by its file system, which is hosted on another computer system acting, for example, as a file server.</span></span> <span data-ttu-id="bda06-109">Pour distinguer les deux montages, une association d' [**\_ exportation CIM**](cim-export.md) doit toujours être définie pour les répertoires accessibles/montés à distance.</span><span class="sxs-lookup"><span data-stu-id="bda06-109">To distinguish the two mounts, a [**CIM\_Export**](cim-export.md) association should always be defined for the remotely accessed/mounted directories.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bda06-110">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="bda06-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bda06-111">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bda06-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bda06-112">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="bda06-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bda06-113">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="bda06-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bda06-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bda06-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4F6-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Mount : CIM_Dependency
{
  CIM_NFS       REF Dependent;
  CIM_Directory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="bda06-115">Membres</span><span class="sxs-lookup"><span data-stu-id="bda06-115">Members</span></span>

<span data-ttu-id="bda06-116">La **classe \_ Mount CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bda06-116">The **CIM\_Mount** class has these types of members:</span></span>

-   [<span data-ttu-id="bda06-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bda06-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bda06-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bda06-118">Properties</span></span>

<span data-ttu-id="bda06-119">La **classe \_ Mount CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bda06-119">The **CIM\_Mount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bda06-120">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="bda06-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bda06-121">Type de données **: \_ répertoire CIM**</span><span class="sxs-lookup"><span data-stu-id="bda06-121">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="bda06-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bda06-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bda06-123">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Antecedent »)</span><span class="sxs-lookup"><span data-stu-id="bda06-123">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="bda06-124">[**\_ Répertoire CIM**](cim-directory.md) décrivant le répertoire monté.</span><span class="sxs-lookup"><span data-stu-id="bda06-124">A [**CIM\_Directory**](cim-directory.md) describing the directory mounted.</span></span>

</dd> <dt>

<span data-ttu-id="bda06-125">**Charge**</span><span class="sxs-lookup"><span data-stu-id="bda06-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bda06-126">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="bda06-126">Data type: **CIM\_NFS**</span></span>
</dt> <dt>

<span data-ttu-id="bda06-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bda06-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bda06-128">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="bda06-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="bda06-129">Un [**\_ NFS CIM**](cim-nfs.md) décrivant le système de fichiers sur lequel le répertoire est monté.</span><span class="sxs-lookup"><span data-stu-id="bda06-129">A [**CIM\_NFS**](cim-nfs.md) describing the FileSystem the Directory is mounted on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bda06-130">Notes</span><span class="sxs-lookup"><span data-stu-id="bda06-130">Remarks</span></span>

<span data-ttu-id="bda06-131">**CIM \_ Le montage** est dérivé de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="bda06-131">**CIM\_Mount** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="bda06-132">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="bda06-132">WMI does not implement this class.</span></span>

<span data-ttu-id="bda06-133">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="bda06-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bda06-134">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="bda06-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bda06-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bda06-135">Requirements</span></span>



| <span data-ttu-id="bda06-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bda06-136">Requirement</span></span> | <span data-ttu-id="bda06-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="bda06-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bda06-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bda06-138">Minimum supported client</span></span><br/> | <span data-ttu-id="bda06-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bda06-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bda06-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bda06-140">Minimum supported server</span></span><br/> | <span data-ttu-id="bda06-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bda06-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bda06-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bda06-142">Namespace</span></span><br/>                | <span data-ttu-id="bda06-143">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="bda06-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bda06-144">MOF</span><span class="sxs-lookup"><span data-stu-id="bda06-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bda06-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bda06-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bda06-146">DLL</span><span class="sxs-lookup"><span data-stu-id="bda06-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bda06-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bda06-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bda06-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bda06-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bda06-149">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="bda06-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

