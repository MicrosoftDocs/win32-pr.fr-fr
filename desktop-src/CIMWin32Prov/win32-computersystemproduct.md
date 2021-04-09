---
description: Représente un produit. Cela comprend les logiciels et le matériel utilisés sur ce système informatique.
ms.assetid: 6241e703-4ce9-435f-bf36-4388e38a3ea5
ms.tgt_platform: multiple
title: Classe Win32_ComputerSystemProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProduct
- Win32_ComputerSystemProduct.Caption
- Win32_ComputerSystemProduct.Description
- Win32_ComputerSystemProduct.IdentifyingNumber
- Win32_ComputerSystemProduct.Name
- Win32_ComputerSystemProduct.SKUNumber
- Win32_ComputerSystemProduct.Vendor
- Win32_ComputerSystemProduct.Version
- Win32_ComputerSystemProduct.UUID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8cab3dc8679c606076eca2f5cf704867aa9833c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110342"
---
# <a name="win32_computersystemproduct-class"></a><span data-ttu-id="36f1c-104">\_Classe ComputerSystemProduct Win32</span><span class="sxs-lookup"><span data-stu-id="36f1c-104">Win32\_ComputerSystemProduct class</span></span>

<span data-ttu-id="36f1c-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ ComputerSystemProduct** représente un produit.</span><span class="sxs-lookup"><span data-stu-id="36f1c-105">The **Win32\_ComputerSystemProduct** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a product.</span></span> <span data-ttu-id="36f1c-106">Cela comprend les logiciels et le matériel utilisés sur ce système informatique.</span><span class="sxs-lookup"><span data-stu-id="36f1c-106">This includes software and hardware used on this computer system.</span></span>

<span data-ttu-id="36f1c-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="36f1c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="36f1c-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="36f1c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f1c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36f1c-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B96-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystemProduct : CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
  string UUID;
};
```

## <a name="members"></a><span data-ttu-id="36f1c-110">Membres</span><span class="sxs-lookup"><span data-stu-id="36f1c-110">Members</span></span>

<span data-ttu-id="36f1c-111">La classe **Win32 \_ ComputerSystemProduct** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="36f1c-111">The **Win32\_ComputerSystemProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="36f1c-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="36f1c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36f1c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="36f1c-113">Properties</span></span>

<span data-ttu-id="36f1c-114">La classe **Win32 \_ ComputerSystemProduct** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="36f1c-114">The **Win32\_ComputerSystemProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36f1c-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="36f1c-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f1c-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="36f1c-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f1c-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36f1c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f1c-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="36f1c-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="36f1c-119">Description courte du produit.</span><span class="sxs-lookup"><span data-stu-id="36f1c-119">Short textual description for the product.</span></span>

<span data-ttu-id="36f1c-120">Cette propriété est héritée [**du \_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="36f1c-120">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="36f1c-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="36f1c-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f1c-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="36f1c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f1c-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36f1c-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36f1c-124">Description textuelle du produit.</span><span class="sxs-lookup"><span data-stu-id="36f1c-124">Textual description of the product.</span></span>

<span data-ttu-id="36f1c-125">Cette propriété est héritée [**du \_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="36f1c-125">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="36f1c-126">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="36f1c-126">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f1c-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="36f1c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f1c-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36f1c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f1c-129">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="36f1c-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="36f1c-130">Identification du produit, telle qu’un numéro de série sur un logiciel, un numéro gravé sur une puce matérielle, ou (pour les produits incommercials) un numéro de projet.</span><span class="sxs-lookup"><span data-stu-id="36f1c-130">Product identification, such as a serial number on software, a die number on a hardware chip, or (for noncommercial products) a project number.</span></span>

<span data-ttu-id="36f1c-131">Cette propriété est héritée [**du \_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="36f1c-131">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="36f1c-132">**Nom**</span><span class="sxs-lookup"><span data-stu-id="36f1c-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f1c-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="36f1c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f1c-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36f1c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f1c-135">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="36f1c-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="36f1c-136">Nom de produit couramment utilisé.</span><span class="sxs-lookup"><span data-stu-id="36f1c-136">Commonly used product name.</span></span>

<span data-ttu-id="36f1c-137">Cette propriété est héritée [**du \_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="36f1c-137">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="36f1c-138">**SKUNumber**</span><span class="sxs-lookup"><span data-stu-id="36f1c-138">**SKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f1c-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="36f1c-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f1c-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36f1c-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f1c-141">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="36f1c-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="36f1c-142">Informations relatives à la référence (SKU) du produit.</span><span class="sxs-lookup"><span data-stu-id="36f1c-142">Product's stock-keeping unit (SKU) information.</span></span>

<span data-ttu-id="36f1c-143">Cette propriété est héritée [**du \_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="36f1c-143">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="36f1c-144">**UUID**</span><span class="sxs-lookup"><span data-stu-id="36f1c-144">**UUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f1c-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="36f1c-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f1c-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36f1c-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f1c-147">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 1 \| UUID")</span><span class="sxs-lookup"><span data-stu-id="36f1c-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|UUID")</span></span>
</dt> </dl>

<span data-ttu-id="36f1c-148">Identificateur unique universel (UUID) de ce produit.</span><span class="sxs-lookup"><span data-stu-id="36f1c-148">Universally unique identifier (UUID) for this product.</span></span> <span data-ttu-id="36f1c-149">Un UUID est un identificateur 128 bits qui est garanti être différent des autres UUID générés.</span><span class="sxs-lookup"><span data-stu-id="36f1c-149">A UUID is a 128-bit identifier that is guaranteed to be different from other generated UUIDs.</span></span> <span data-ttu-id="36f1c-150">Si un UUID n’est pas disponible, un UUID de tous les zéros est utilisé.</span><span class="sxs-lookup"><span data-stu-id="36f1c-150">If a UUID is not available, a UUID of all zeros is used.</span></span>

<span data-ttu-id="36f1c-151">Cette valeur provient du membre **UUID** de la structure des **informations système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="36f1c-151">This value comes from the **UUID** member of the **System Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="36f1c-152">**Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="36f1c-152">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f1c-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="36f1c-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f1c-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36f1c-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f1c-155">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="36f1c-155">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="36f1c-156">Nom du fournisseur du produit ou de l’entité vendant le produit (fabricant, revendeur, OEM, etc.).</span><span class="sxs-lookup"><span data-stu-id="36f1c-156">Name of the product's supplier, or the entity selling the product (the manufacturer, reseller, OEM, and so on).</span></span>

<span data-ttu-id="36f1c-157">Cette propriété est héritée [**du \_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="36f1c-157">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="36f1c-158">**Version**</span><span class="sxs-lookup"><span data-stu-id="36f1c-158">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f1c-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="36f1c-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f1c-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36f1c-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f1c-161">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="36f1c-161">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="36f1c-162">Informations sur la version du produit.</span><span class="sxs-lookup"><span data-stu-id="36f1c-162">Product version information.</span></span>

<span data-ttu-id="36f1c-163">Cette propriété est héritée [**du \_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="36f1c-163">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36f1c-164">Notes</span><span class="sxs-lookup"><span data-stu-id="36f1c-164">Remarks</span></span>

<span data-ttu-id="36f1c-165">La classe **Win32 \_ ComputerSystemProduct** est dérivée [**du \_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="36f1c-165">The **Win32\_ComputerSystemProduct** class is derived from [**CIM\_Product**](cim-product.md).</span></span>

## <a name="examples"></a><span data-ttu-id="36f1c-166">Exemples</span><span class="sxs-lookup"><span data-stu-id="36f1c-166">Examples</span></span>

<span data-ttu-id="36f1c-167">L’exemple [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell de la Galerie TechNet utilise pour **Win32 \_ ComputerSystemProduct** pour récupérer une liste de matériel non opérationnel à l’aide de WMI.</span><span class="sxs-lookup"><span data-stu-id="36f1c-167">The [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell sample on TechNet Gallery uses to **Win32\_ComputerSystemProduct** to retrieve a list of non-working hardware using WMI.</span></span>

## <a name="requirements"></a><span data-ttu-id="36f1c-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36f1c-168">Requirements</span></span>



| <span data-ttu-id="36f1c-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36f1c-169">Requirement</span></span> | <span data-ttu-id="36f1c-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="36f1c-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36f1c-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36f1c-171">Minimum supported client</span></span><br/> | <span data-ttu-id="36f1c-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36f1c-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="36f1c-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36f1c-173">Minimum supported server</span></span><br/> | <span data-ttu-id="36f1c-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36f1c-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="36f1c-175">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="36f1c-175">Namespace</span></span><br/>                | <span data-ttu-id="36f1c-176">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="36f1c-176">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="36f1c-177">MOF</span><span class="sxs-lookup"><span data-stu-id="36f1c-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36f1c-178"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36f1c-178"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="36f1c-179">DLL</span><span class="sxs-lookup"><span data-stu-id="36f1c-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36f1c-180"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36f1c-180"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36f1c-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36f1c-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f1c-182">**\_Produit CIM**</span><span class="sxs-lookup"><span data-stu-id="36f1c-182">**CIM\_Product**</span></span>](cim-product.md)
</dt> <dt>

<span data-ttu-id="36f1c-183">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="36f1c-183">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

