---
description: La \_ classe de produit CIM est une classe concrète qui représente une collection d’éléments physiques, de fonctionnalités logicielles et d’autres produits acquis en tant qu’unité.
ms.assetid: beb20f61-de39-4221-8d29-4727104518d5
ms.tgt_platform: multiple
title: Classe CIM_Product
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Product
- CIM_Product.Caption
- CIM_Product.Description
- CIM_Product.IdentifyingNumber
- CIM_Product.Name
- CIM_Product.SKUNumber
- CIM_Product.Vendor
- CIM_Product.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16c8541a18185d721bbdcbf23acaeb67adf508c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748005"
---
# <a name="cim_product-class"></a><span data-ttu-id="af294-103">CIM ( \_ classe de produit)</span><span class="sxs-lookup"><span data-stu-id="af294-103">CIM\_Product class</span></span>

<span data-ttu-id="af294-104">La classe de **\_ produit CIM** est une classe concrète qui représente une collection d’éléments physiques, de fonctionnalités logicielles et d’autres produits acquis en tant qu’unité.</span><span class="sxs-lookup"><span data-stu-id="af294-104">The **CIM\_Product** class is a concrete class that represents a collection of physical elements, software features and, other products, acquired as a unit.</span></span> <span data-ttu-id="af294-105">L’acquisition implique un accord entre le fournisseur et le consommateur, qui peut avoir des implications sur la licence, le support et la garantie du produit.</span><span class="sxs-lookup"><span data-stu-id="af294-105">Acquisition implies an agreement between the supplier and consumer, which can have implications on product licensing, support, and warranty.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af294-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="af294-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="af294-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="af294-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="af294-108">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="af294-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="af294-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="af294-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="af294-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af294-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B63-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="af294-111">Membres</span><span class="sxs-lookup"><span data-stu-id="af294-111">Members</span></span>

<span data-ttu-id="af294-112">La classe de **\_ produit CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="af294-112">The **CIM\_Product** class has these types of members:</span></span>

-   [<span data-ttu-id="af294-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="af294-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="af294-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="af294-114">Properties</span></span>

<span data-ttu-id="af294-115">La classe de **\_ produit CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="af294-115">The **CIM\_Product** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af294-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="af294-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af294-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="af294-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af294-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af294-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af294-119">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="af294-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="af294-120">Description courte du produit.</span><span class="sxs-lookup"><span data-stu-id="af294-120">Short textual description for the product.</span></span>

</dd> <dt>

<span data-ttu-id="af294-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="af294-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af294-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="af294-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af294-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af294-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af294-124">Description textuelle du produit.</span><span class="sxs-lookup"><span data-stu-id="af294-124">Textual description of the product.</span></span>

</dd> <dt>

<span data-ttu-id="af294-125">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="af294-125">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af294-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="af294-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af294-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af294-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af294-128">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="af294-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="af294-129">Identification du produit, telle qu’un numéro de série sur un logiciel, un numéro gravé sur une puce matérielle, ou (pour les produits incommercials) un numéro de projet.</span><span class="sxs-lookup"><span data-stu-id="af294-129">Product identification, such as a serial number on software, a die number on a hardware chip, or (for noncommercial products) a project number.</span></span>

</dd> <dt>

<span data-ttu-id="af294-130">**Nom**</span><span class="sxs-lookup"><span data-stu-id="af294-130">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af294-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="af294-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af294-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af294-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af294-133">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="af294-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="af294-134">Nom de produit couramment utilisé.</span><span class="sxs-lookup"><span data-stu-id="af294-134">Commonly used product name.</span></span>

</dd> <dt>

<span data-ttu-id="af294-135">**SKUNumber**</span><span class="sxs-lookup"><span data-stu-id="af294-135">**SKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af294-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="af294-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af294-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af294-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af294-138">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="af294-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="af294-139">Informations relatives à la référence (SKU) du produit.</span><span class="sxs-lookup"><span data-stu-id="af294-139">Product's stock-keeping unit (SKU) information.</span></span>

</dd> <dt>

<span data-ttu-id="af294-140">**Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="af294-140">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af294-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="af294-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af294-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af294-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af294-143">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="af294-143">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="af294-144">Nom du fournisseur du produit ou de l’entité vendant le produit (fabricant, revendeur, OEM, etc.).</span><span class="sxs-lookup"><span data-stu-id="af294-144">Name of the product's supplier, or the entity selling the product (the manufacturer, reseller, OEM, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="af294-145">**Version**</span><span class="sxs-lookup"><span data-stu-id="af294-145">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af294-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="af294-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af294-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="af294-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af294-148">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="af294-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="af294-149">Informations sur la version du produit.</span><span class="sxs-lookup"><span data-stu-id="af294-149">Product version information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af294-150">Notes</span><span class="sxs-lookup"><span data-stu-id="af294-150">Remarks</span></span>

<span data-ttu-id="af294-151">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="af294-151">WMI does not implement this class.</span></span> <span data-ttu-id="af294-152">Pour les classes WMI dérivées du **\_ produit CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="af294-152">For WMI classes that are derived from **CIM\_Product**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="af294-153">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="af294-153">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="af294-154">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="af294-154">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="af294-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af294-155">Requirements</span></span>



| <span data-ttu-id="af294-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af294-156">Requirement</span></span> | <span data-ttu-id="af294-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="af294-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af294-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af294-158">Minimum supported client</span></span><br/> | <span data-ttu-id="af294-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af294-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="af294-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af294-160">Minimum supported server</span></span><br/> | <span data-ttu-id="af294-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af294-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="af294-162">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="af294-162">Namespace</span></span><br/>                | <span data-ttu-id="af294-163">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="af294-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="af294-164">MOF</span><span class="sxs-lookup"><span data-stu-id="af294-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af294-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af294-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="af294-166">DLL</span><span class="sxs-lookup"><span data-stu-id="af294-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af294-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af294-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

