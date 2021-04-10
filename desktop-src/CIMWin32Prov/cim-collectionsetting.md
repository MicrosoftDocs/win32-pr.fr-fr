---
description: La \_ classe CIM CollectionSetting représente l’association entre un modèle CIM \_ CollectionOfMSEs et la classe de paramètres définie pour eux.
ms.assetid: f09bd656-5fdd-4ab1-8ef9-52d431a5117d
ms.tgt_platform: multiple
title: Classe CIM_CollectionSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionSetting
- CIM_CollectionSetting.Collection
- CIM_CollectionSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c290225ee38008f0345b695af794e57f311f2998
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861341"
---
# <a name="cim_collectionsetting-class"></a><span data-ttu-id="e0b69-103">\_Classe CIM CollectionSetting</span><span class="sxs-lookup"><span data-stu-id="e0b69-103">CIM\_CollectionSetting class</span></span>

<span data-ttu-id="e0b69-104">La classe **CIM \_ CollectionSetting** représente l’association entre un [**modèle CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) et la classe de paramètres définie pour eux.</span><span class="sxs-lookup"><span data-stu-id="e0b69-104">The **CIM\_CollectionSetting** class represents the association between a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) and the setting class defined for them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0b69-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e0b69-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e0b69-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e0b69-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e0b69-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e0b69-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e0b69-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e0b69-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b69-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0b69-109">Syntax</span></span>

``` syntax
class CIM_CollectionSetting
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="e0b69-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e0b69-110">Members</span></span>

<span data-ttu-id="e0b69-111">La classe **CIM \_ CollectionSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e0b69-111">The **CIM\_CollectionSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="e0b69-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0b69-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0b69-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0b69-113">Properties</span></span>

<span data-ttu-id="e0b69-114">La classe **CIM \_ CollectionSetting** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e0b69-114">The **CIM\_CollectionSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0b69-115">**Collection**</span><span class="sxs-lookup"><span data-stu-id="e0b69-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b69-116">Type de données : **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="e0b69-116">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="e0b69-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0b69-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0b69-118">Référence à la classe [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="e0b69-118">Reference to the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e0b69-119">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="e0b69-119">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0b69-120">Type de données **: \_ paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="e0b69-120">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="e0b69-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0b69-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0b69-122">Référence à l’objet de **paramètre** associé à la propriété de **collection** .</span><span class="sxs-lookup"><span data-stu-id="e0b69-122">Reference to the **Setting** object associated with the **Collection** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0b69-123">Notes</span><span class="sxs-lookup"><span data-stu-id="e0b69-123">Remarks</span></span>

<span data-ttu-id="e0b69-124">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="e0b69-124">WMI does not implement this class.</span></span> <span data-ttu-id="e0b69-125">Pour plus d’informations sur les classes WMI dérivées de **CIM \_ CollectionSetting**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e0b69-125">For more information about WMI classes derived from **CIM\_CollectionSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e0b69-126">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="e0b69-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e0b69-127">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e0b69-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b69-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0b69-128">Requirements</span></span>



| <span data-ttu-id="e0b69-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0b69-129">Requirement</span></span> | <span data-ttu-id="e0b69-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0b69-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b69-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0b69-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e0b69-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0b69-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e0b69-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0b69-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e0b69-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0b69-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0b69-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e0b69-135">Namespace</span></span><br/>                | <span data-ttu-id="e0b69-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e0b69-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e0b69-137">MOF</span><span class="sxs-lookup"><span data-stu-id="e0b69-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0b69-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0b69-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0b69-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e0b69-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0b69-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0b69-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




