---
description: La \_ classe FRU CIM représente une collection définie par le fournisseur de produits et d’éléments physiques associés à une unité remplaçable sur site (FRU) pour la prise en charge, la maintenance ou la mise à niveau d’un produit à l’emplacement du client.
ms.assetid: 4464ec3a-5509-4e15-9020-4abb2edd2570
ms.tgt_platform: multiple
title: Classe CIM_FRU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRU
- CIM_FRU.Caption
- CIM_FRU.Description
- CIM_FRU.FRUNumber
- CIM_FRU.IdentifyingNumber
- CIM_FRU.Name
- CIM_FRU.RevisionLevel
- CIM_FRU.Vendor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d163c3c223159ad8e09aa6e36d63187ff0aa97f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748468"
---
# <a name="cim_fru-class"></a><span data-ttu-id="98402-103">\_Classe FRU CIM</span><span class="sxs-lookup"><span data-stu-id="98402-103">CIM\_FRU class</span></span>

<span data-ttu-id="98402-104">La **classe \_ FRU CIM** représente une collection définie par le fournisseur de produits et d’éléments physiques associés à une unité remplaçable sur site (FRU) pour la prise en charge, la maintenance ou la mise à niveau d’un produit à l’emplacement du client.</span><span class="sxs-lookup"><span data-stu-id="98402-104">The **CIM\_FRU** class represents a vendor-defined collection of products and physical elements that are associated with a field replaceable unit (FRU) to support, maintain, or upgrade a product at the customer's location.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98402-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="98402-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="98402-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="98402-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="98402-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="98402-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="98402-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="98402-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="98402-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98402-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{778C74EE-DB2A-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_FRU
{
  string Caption;
  string Description;
  string FRUNumber;
  string IdentifyingNumber;
  string Name;
  string RevisionLevel;
  string Vendor;
};
```

## <a name="members"></a><span data-ttu-id="98402-110">Membres</span><span class="sxs-lookup"><span data-stu-id="98402-110">Members</span></span>

<span data-ttu-id="98402-111">La **classe \_ FRU CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="98402-111">The **CIM\_FRU** class has these types of members:</span></span>

-   [<span data-ttu-id="98402-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="98402-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98402-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="98402-113">Properties</span></span>

<span data-ttu-id="98402-114">La **classe \_ FRU CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="98402-114">The **CIM\_FRU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98402-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="98402-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98402-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98402-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98402-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98402-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98402-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="98402-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="98402-119">Description courte de la FRU.</span><span class="sxs-lookup"><span data-stu-id="98402-119">Short textual description for the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="98402-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="98402-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98402-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98402-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98402-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98402-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98402-123">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|FRU DMTF \| 002,3 ")</span><span class="sxs-lookup"><span data-stu-id="98402-123">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.3")</span></span>
</dt> </dl>

<span data-ttu-id="98402-124">Description de la FRU.</span><span class="sxs-lookup"><span data-stu-id="98402-124">Description of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="98402-125">**FRUNumber**</span><span class="sxs-lookup"><span data-stu-id="98402-125">**FRUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98402-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98402-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98402-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98402-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98402-128">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|FRU DMTF \| 002,6 "), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="98402-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.6"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="98402-129">Informations de classement FRU.</span><span class="sxs-lookup"><span data-stu-id="98402-129">FRU ordering information.</span></span>

</dd> <dt>

<span data-ttu-id="98402-130">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="98402-130">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98402-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98402-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98402-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98402-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98402-133">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|FRU DMTF \| 002,7 "), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="98402-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.7"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="98402-134">Identification d’un logiciel, tel qu’un numéro de série ou un numéro gravé sur une puce matérielle.</span><span class="sxs-lookup"><span data-stu-id="98402-134">Identification on software, such as a serial number, or a die number on a hardware chip.</span></span>

</dd> <dt>

<span data-ttu-id="98402-135">**Nom**</span><span class="sxs-lookup"><span data-stu-id="98402-135">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98402-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98402-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98402-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98402-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98402-138">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="98402-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="98402-139">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="98402-139">Label by which the object is known.</span></span>

</dd> <dt>

<span data-ttu-id="98402-140">**RevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="98402-140">**RevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98402-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98402-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98402-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98402-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98402-143">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|FRU DMTF \| 002,8 "), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="98402-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.8"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="98402-144">Niveau de révision de la FRU.</span><span class="sxs-lookup"><span data-stu-id="98402-144">Revision level of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="98402-145">**Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="98402-145">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98402-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98402-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98402-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="98402-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98402-148">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|FRU DMTF \| 002,4 "), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="98402-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.4"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="98402-149">Nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="98402-149">Name of the supplier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98402-150">Notes</span><span class="sxs-lookup"><span data-stu-id="98402-150">Remarks</span></span>

<span data-ttu-id="98402-151">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="98402-151">WMI does not implement this class.</span></span>

<span data-ttu-id="98402-152">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="98402-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="98402-153">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="98402-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="98402-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98402-154">Requirements</span></span>



| <span data-ttu-id="98402-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98402-155">Requirement</span></span> | <span data-ttu-id="98402-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="98402-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98402-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98402-157">Minimum supported client</span></span><br/> | <span data-ttu-id="98402-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98402-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="98402-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98402-159">Minimum supported server</span></span><br/> | <span data-ttu-id="98402-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98402-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="98402-161">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="98402-161">Namespace</span></span><br/>                | <span data-ttu-id="98402-162">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="98402-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="98402-163">MOF</span><span class="sxs-lookup"><span data-stu-id="98402-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98402-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98402-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="98402-165">DLL</span><span class="sxs-lookup"><span data-stu-id="98402-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98402-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98402-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

