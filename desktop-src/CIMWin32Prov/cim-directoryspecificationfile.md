---
description: L' \_ Association CIM DirectorySpecificationFile représente le répertoire qui contient le fichier spécifié en référençant la \_ classe CIM DirectorySpecification.
ms.assetid: 57fe996e-6bd4-4070-9e99-460b2a36243f
ms.tgt_platform: multiple
title: Classe CIM_DirectorySpecificationFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecificationFile
- CIM_DirectorySpecificationFile.DirectorySpecification
- CIM_DirectorySpecificationFile.FileSpecification
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1877d9864a76334c2b2e00fc7822adb09b91028b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111067"
---
# <a name="cim_directoryspecificationfile-class"></a><span data-ttu-id="3a39e-103">\_Classe CIM DirectorySpecificationFile</span><span class="sxs-lookup"><span data-stu-id="3a39e-103">CIM\_DirectorySpecificationFile class</span></span>

<span data-ttu-id="3a39e-104">L’Association **CIM \_ DirectorySpecificationFile** représente le répertoire qui contient le fichier spécifié en référençant la classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) .</span><span class="sxs-lookup"><span data-stu-id="3a39e-104">The **CIM\_DirectorySpecificationFile** association represents the directory that contains the file specified by referencing the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3a39e-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="3a39e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3a39e-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3a39e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3a39e-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3a39e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3a39e-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="3a39e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a39e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a39e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{BCD64CCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_DirectorySpecificationFile
{
  CIM_DirectorySpecification REF DirectorySpecification;
  CIM_FileSpecification      REF FileSpecification;
};
```

## <a name="members"></a><span data-ttu-id="3a39e-110">Membres</span><span class="sxs-lookup"><span data-stu-id="3a39e-110">Members</span></span>

<span data-ttu-id="3a39e-111">La classe **CIM \_ DirectorySpecificationFile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3a39e-111">The **CIM\_DirectorySpecificationFile** class has these types of members:</span></span>

-   [<span data-ttu-id="3a39e-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3a39e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a39e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3a39e-113">Properties</span></span>

<span data-ttu-id="3a39e-114">La classe **CIM \_ DirectorySpecificationFile** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a39e-114">The **CIM\_DirectorySpecificationFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a39e-115">**DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="3a39e-115">**DirectorySpecification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a39e-116">Type de données : **CIM \_ DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="3a39e-116">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="3a39e-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a39e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a39e-118">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="3a39e-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="3a39e-119">Référence à la spécification de répertoire.</span><span class="sxs-lookup"><span data-stu-id="3a39e-119">Reference to the directory specification.</span></span>

</dd> <dt>

<span data-ttu-id="3a39e-120">**FileSpecification**</span><span class="sxs-lookup"><span data-stu-id="3a39e-120">**FileSpecification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a39e-121">Type de données : **CIM \_ FileSpecification**</span><span class="sxs-lookup"><span data-stu-id="3a39e-121">Data type: **CIM\_FileSpecification**</span></span>
</dt> <dt>

<span data-ttu-id="3a39e-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a39e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a39e-123">Qualificateurs : [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="3a39e-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="3a39e-124">Référence à la spécification de fichier.</span><span class="sxs-lookup"><span data-stu-id="3a39e-124">Reference to the file specification.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a39e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="3a39e-125">Remarks</span></span>

<span data-ttu-id="3a39e-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="3a39e-126">WMI does not implement this class.</span></span>

<span data-ttu-id="3a39e-127">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="3a39e-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3a39e-128">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="3a39e-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a39e-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a39e-129">Requirements</span></span>



| <span data-ttu-id="3a39e-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a39e-130">Requirement</span></span> | <span data-ttu-id="3a39e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a39e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a39e-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a39e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3a39e-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a39e-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a39e-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a39e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3a39e-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a39e-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a39e-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3a39e-136">Namespace</span></span><br/>                | <span data-ttu-id="3a39e-137">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3a39e-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3a39e-138">MOF</span><span class="sxs-lookup"><span data-stu-id="3a39e-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a39e-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a39e-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a39e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3a39e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a39e-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a39e-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

