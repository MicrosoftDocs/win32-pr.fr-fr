---
description: La \_ classe d’emplacement CIM représente la position et l’adresse d’un élément physique.
ms.assetid: c1ec467c-a338-4beb-a8fe-1ebc5b05c754
ms.tgt_platform: multiple
title: Classe CIM_Location
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Location
- CIM_Location.Address
- CIM_Location.Name
- CIM_Location.PhysicalPosition
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd5a1c1c23d07020b45c1c5979a941f01baff0d0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201021"
---
# <a name="cim_location-class"></a><span data-ttu-id="5b3d5-103">\_Classe d’emplacement CIM</span><span class="sxs-lookup"><span data-stu-id="5b3d5-103">CIM\_Location class</span></span>

<span data-ttu-id="5b3d5-104">La classe d' **\_ emplacement CIM** représente la position et l’adresse d’un élément physique.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-104">The **CIM\_Location** class represents the position and address of a physical element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b3d5-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5b3d5-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5b3d5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5b3d5-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5b3d5-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b3d5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b3d5-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B67-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Location
{
  string Address;
  string Name;
  string PhysicalPosition;
};
```

## <a name="members"></a><span data-ttu-id="5b3d5-110">Membres</span><span class="sxs-lookup"><span data-stu-id="5b3d5-110">Members</span></span>

<span data-ttu-id="5b3d5-111">La classe d' **\_ emplacement CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5b3d5-111">The **CIM\_Location** class has these types of members:</span></span>

-   [<span data-ttu-id="5b3d5-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5b3d5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b3d5-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5b3d5-113">Properties</span></span>

<span data-ttu-id="5b3d5-114">La classe d' **\_ emplacement CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-114">The **CIM\_Location** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b3d5-115">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="5b3d5-115">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b3d5-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b3d5-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b3d5-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5b3d5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b3d5-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="5b3d5-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="5b3d5-119">Chaîne de forme libre qui indique une rue ou un autre type d’adresse pour l’emplacement de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-119">Free-form string that indicates a street or other type of address for the physical element's location.</span></span>

</dd> <dt>

<span data-ttu-id="5b3d5-120">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5b3d5-120">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b3d5-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b3d5-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b3d5-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5b3d5-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b3d5-123">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5b3d5-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5b3d5-124">Chaîne de forme libre qui définit une étiquette pour l’emplacement et qui fait partie de la clé de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-124">Free-form string that defines a label for the location and is part of the key for the object.</span></span>

</dd> <dt>

<span data-ttu-id="5b3d5-125">**PhysicalPosition**</span><span class="sxs-lookup"><span data-stu-id="5b3d5-125">**PhysicalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b3d5-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5b3d5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b3d5-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5b3d5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b3d5-128">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5b3d5-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5b3d5-129">Chaîne de forme libre qui indique le positionnement d’un élément physique.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-129">Free-form string that indicates the placement of a physical element.</span></span> <span data-ttu-id="5b3d5-130">Il peut spécifier des informations d’emplacement sur un tableau d’accueil, monter un site dans un fichier CAB ou obtenir des informations sur la latitude et la longitude.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-130">It can specify slot information on a hosting board, mounting site in a cabinet, or latitude and longitude information.</span></span> <span data-ttu-id="5b3d5-131">Il fait partie de la clé de l’objet d' **\_ emplacement CIM** .</span><span class="sxs-lookup"><span data-stu-id="5b3d5-131">It is part of the key of the **CIM\_Location** object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b3d5-132">Notes</span><span class="sxs-lookup"><span data-stu-id="5b3d5-132">Remarks</span></span>

<span data-ttu-id="5b3d5-133">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-133">WMI does not implement this class.</span></span> <span data-ttu-id="5b3d5-134">Pour les classes dérivées de l' **\_ emplacement CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5b3d5-134">For classes derived from **CIM\_Location**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5b3d5-135">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5b3d5-136">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="5b3d5-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b3d5-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b3d5-137">Requirements</span></span>



| <span data-ttu-id="5b3d5-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b3d5-138">Requirement</span></span> | <span data-ttu-id="5b3d5-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b3d5-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b3d5-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b3d5-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5b3d5-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b3d5-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5b3d5-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b3d5-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5b3d5-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b3d5-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b3d5-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5b3d5-144">Namespace</span></span><br/>                | <span data-ttu-id="5b3d5-145">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="5b3d5-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5b3d5-146">MOF</span><span class="sxs-lookup"><span data-stu-id="5b3d5-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b3d5-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b3d5-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b3d5-148">DLL</span><span class="sxs-lookup"><span data-stu-id="5b3d5-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b3d5-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b3d5-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

