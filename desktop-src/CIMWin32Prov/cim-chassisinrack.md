---
description: L' \_ Association CIM ChassisInRack représente le &\# 0034 ; contenant&\# 0034 ; relation entre un rack et un châssis qu’il contient.
ms.assetid: 1c8a5058-58fe-42e0-b337-7e1a05120789
ms.tgt_platform: multiple
title: Classe CIM_ChassisInRack
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ChassisInRack
- CIM_ChassisInRack.LocationWithinContainer
- CIM_ChassisInRack.PartComponent
- CIM_ChassisInRack.GroupComponent
- CIM_ChassisInRack.BottomU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fd582991df30bc36cd71c4c3fa08d9a5a5153819
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110998"
---
# <a name="cim_chassisinrack-class"></a><span data-ttu-id="bfd5e-103">\_Classe CIM ChassisInRack</span><span class="sxs-lookup"><span data-stu-id="bfd5e-103">CIM\_ChassisInRack class</span></span>

<span data-ttu-id="bfd5e-104">L’Association **CIM \_ ChassisInRack** représente la relation « contenant » entre un rack et un châssis qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="bfd5e-104">The **CIM\_ChassisInRack** association represents the "containing" relationship between a rack and a chassis that it contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bfd5e-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="bfd5e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bfd5e-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bfd5e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bfd5e-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="bfd5e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bfd5e-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="bfd5e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfd5e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfd5e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B73-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ChassisInRack : CIM_Container
{
  string          LocationWithinContainer;
  CIM_Chassis REF PartComponent;
  CIM_Rack    REF GroupComponent;
  uint16          BottomU;
};
```

## <a name="members"></a><span data-ttu-id="bfd5e-110">Membres</span><span class="sxs-lookup"><span data-stu-id="bfd5e-110">Members</span></span>

<span data-ttu-id="bfd5e-111">La classe **CIM \_ ChassisInRack** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bfd5e-111">The **CIM\_ChassisInRack** class has these types of members:</span></span>

-   [<span data-ttu-id="bfd5e-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bfd5e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bfd5e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bfd5e-113">Properties</span></span>

<span data-ttu-id="bfd5e-114">La classe **CIM \_ ChassisInRack** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="bfd5e-114">The **CIM\_ChassisInRack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bfd5e-115">**Inférieur**</span><span class="sxs-lookup"><span data-stu-id="bfd5e-115">**BottomU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd5e-116">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfd5e-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfd5e-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bfd5e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfd5e-118">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("US")</span><span class="sxs-lookup"><span data-stu-id="bfd5e-118">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")</span></span>
</dt> </dl>

<span data-ttu-id="bfd5e-119">Entier qui indique le « U » inférieur ou inférieur dans lequel le châssis est monté.</span><span class="sxs-lookup"><span data-stu-id="bfd5e-119">Integer that indicates the lowest or bottom "U" in which the chassis is mounted.</span></span> <span data-ttu-id="bfd5e-120">Un « U » est une unité de mesure standard pour la hauteur d’un rack, ou un composant montable en rack et est égal à 1,75 pouces ou 4,445 centimètres.</span><span class="sxs-lookup"><span data-stu-id="bfd5e-120">A "U" is a standard unit of measure for the height of a rack, or rack-mountable component, and is equal to 1.75 inches or 4.445 centimeters.</span></span>

</dd> <dt>

<span data-ttu-id="bfd5e-121">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="bfd5e-121">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd5e-122">Type de données **: \_ rack CIM**</span><span class="sxs-lookup"><span data-stu-id="bfd5e-122">Data type: **CIM\_Rack**</span></span>
</dt> <dt>

<span data-ttu-id="bfd5e-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bfd5e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfd5e-124">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="bfd5e-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="bfd5e-125">Un [**\_ rack CIM**](cim-rack.md) qui décrit le rack qui contient le châssis.</span><span class="sxs-lookup"><span data-stu-id="bfd5e-125">A [**CIM\_Rack**](cim-rack.md) that describes the rack that contains the chassis.</span></span>

</dd> <dt>

<span data-ttu-id="bfd5e-126">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="bfd5e-126">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd5e-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bfd5e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfd5e-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bfd5e-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfd5e-129">Chaîne de forme libre qui représente le positionnement de l’élément physique dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="bfd5e-129">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="bfd5e-130">Les informations relatives aux éléments stationnaires dans le conteneur (par exemple, « deuxième baie de lecteur à partir du haut »), des angles, des altitudes et d’autres données peuvent être enregistrées dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="bfd5e-130">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="bfd5e-131">Cette chaîne peut compléter ou être utilisée à la place de l’instanciation de l’objet d' [**\_ emplacement CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="bfd5e-131">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="bfd5e-132">Cette propriété est héritée [**du \_ conteneur CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="bfd5e-132">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfd5e-133">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="bfd5e-133">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd5e-134">Type de données **: \_ châssis CIM**</span><span class="sxs-lookup"><span data-stu-id="bfd5e-134">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="bfd5e-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bfd5e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfd5e-136">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="bfd5e-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="bfd5e-137">[**\_ Châssis CIM**](cim-chassis.md) qui décrit le châssis monté dans le rack.</span><span class="sxs-lookup"><span data-stu-id="bfd5e-137">A [**CIM\_Chassis**](cim-chassis.md) that describes the chassis which is mounted in the rack.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfd5e-138">Notes</span><span class="sxs-lookup"><span data-stu-id="bfd5e-138">Remarks</span></span>

<span data-ttu-id="bfd5e-139">La classe **CIM \_ ChassisInRack** est dérivée [**du \_ conteneur CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="bfd5e-139">The **CIM\_ChassisInRack** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="bfd5e-140">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="bfd5e-140">WMI does not implement this class.</span></span>

<span data-ttu-id="bfd5e-141">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="bfd5e-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bfd5e-142">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="bfd5e-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfd5e-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfd5e-143">Requirements</span></span>



| <span data-ttu-id="bfd5e-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfd5e-144">Requirement</span></span> | <span data-ttu-id="bfd5e-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfd5e-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfd5e-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfd5e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="bfd5e-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bfd5e-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bfd5e-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfd5e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="bfd5e-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfd5e-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bfd5e-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bfd5e-150">Namespace</span></span><br/>                | <span data-ttu-id="bfd5e-151">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="bfd5e-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bfd5e-152">MOF</span><span class="sxs-lookup"><span data-stu-id="bfd5e-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfd5e-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfd5e-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bfd5e-154">DLL</span><span class="sxs-lookup"><span data-stu-id="bfd5e-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfd5e-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfd5e-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfd5e-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfd5e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfd5e-157">**\_Conteneur CIM**</span><span class="sxs-lookup"><span data-stu-id="bfd5e-157">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

