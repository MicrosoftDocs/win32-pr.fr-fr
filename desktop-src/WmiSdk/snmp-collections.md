---
description: Une collection SNMP mappe à une classe CIM et les éléments d’une collection sont mappés aux propriétés d’une classe CIM. Toutes les définitions de classe CIM générées doivent être dérivées de la classe SnmpObjectType.
ms.assetid: e6f82fd6-e3d8-48c5-8c7b-a30a2d502f41
ms.tgt_platform: multiple
title: Regroupements SNMP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a85473a394ce715ff9759e974a47824e5621509f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543483"
---
# <a name="snmp-collections"></a><span data-ttu-id="49235-104">Regroupements SNMP</span><span class="sxs-lookup"><span data-stu-id="49235-104">SNMP Collections</span></span>

<span data-ttu-id="49235-105">Une collection SNMP mappe à une classe CIM et les éléments d’une collection sont mappés aux propriétés d’une classe CIM.</span><span class="sxs-lookup"><span data-stu-id="49235-105">An SNMP collection maps to a CIM class and the elements of a collection map to the properties of a CIM class.</span></span> <span data-ttu-id="49235-106">Toutes les définitions de classe CIM générées doivent être dérivées de la classe **SnmpObjectType** .</span><span class="sxs-lookup"><span data-stu-id="49235-106">All generated CIM class definitions must be derived from the **SnmpObjectType** class.</span></span>

> [!Note]  
> <span data-ttu-id="49235-107">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="49235-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="49235-108">Les définitions de classe suivantes parent toutes les définitions de classe générées :</span><span class="sxs-lookup"><span data-stu-id="49235-108">The following class definitions parent all generated class definitions:</span></span>

``` syntax
[abstract]
class SnmpMacro
{
};

[abstract]
class SnmpObjectType:SnmpMacro
{
};
```

## <a name="remarks"></a><span data-ttu-id="49235-109">Notes</span><span class="sxs-lookup"><span data-stu-id="49235-109">Remarks</span></span>

<span data-ttu-id="49235-110">Les règles suivantes s’appliquent lors du mappage de regroupements SNMP à des classes CIM.</span><span class="sxs-lookup"><span data-stu-id="49235-110">The following rules apply when mapping SNMP collections to CIM classes.</span></span> <span data-ttu-id="49235-111">Sauf indication contraire, ces règles s’appliquent à la fois aux collections scalaires et aux collections de tables :</span><span class="sxs-lookup"><span data-stu-id="49235-111">Unless otherwise specified, these rules apply to both scalar and table collections:</span></span>

-   <span data-ttu-id="49235-112">Le processus de mappage génère des noms de classe CIM en concaténant « SNMP \_ », le nom d’identité du module MIB, « \_ » et le descripteur d’objet de la collection.</span><span class="sxs-lookup"><span data-stu-id="49235-112">The mapping process generates CIM class names by concatenating "SNMP\_", the MIB module identity name, "\_", and the collection's object descriptor.</span></span>

    <span data-ttu-id="49235-113">Par exemple : le **système** se convertit en **\_ \_ \_ système SNMP RFC1213 MIB**, tandis que **ifTable** se traduit en **SNMP \_ RFC1213 \_ MIB \_ ifTable**.</span><span class="sxs-lookup"><span data-stu-id="49235-113">For example: **system** translates to **SNMP\_RFC1213\_MIB\_system**, while **ifTable** translates to **SNMP\_RFC1213\_MIB\_ifTable**.</span></span>

-   <span data-ttu-id="49235-114">Dans tous les cas, les traits d’Union (-) dans les identificateurs MIB SNMP sont mappés aux traits de soulignement ( \_ ) dans les noms de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="49235-114">In all cases, hyphens (-) in SNMP MIB identifiers map to underscores (\_) in CIM class names.</span></span>
-   <span data-ttu-id="49235-115">Des conflits de noms peuvent se produire en raison du non-respect de la casse du nom CIM.</span><span class="sxs-lookup"><span data-stu-id="49235-115">Naming conflicts can occur due to CIM name case-insensitivity.</span></span> <span data-ttu-id="49235-116">Si un conflit de noms se produit, le fournisseur choisit l’une des définitions de groupe conflictuelles et ignore les définitions restantes.</span><span class="sxs-lookup"><span data-stu-id="49235-116">If a naming conflict occurs, the provider chooses one of the conflicting group definitions and ignores the remaining definitions.</span></span>
-   <span data-ttu-id="49235-117">Le nom d’identité du module MIB qui contient la collection est mappé au **\_ nom du module** qualificateur de la classe CIM.</span><span class="sxs-lookup"><span data-stu-id="49235-117">The identity name of the MIB module that contains the collection maps to the CIM class qualifier **Module\_Name**.</span></span>
-   <span data-ttu-id="49235-118">L’identificateur d’objet de la collection fabriquée est mappé à l' **\_ ObjectID du groupe** de qualificateurs de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="49235-118">The object identifier of the fabricated collection maps to the CIM class qualifier **Group\_Objectid**.</span></span>
-   <span data-ttu-id="49235-119">La liste d’importations du module MIB (obtenue à partir de la définition de macro **module-Identity** ) est mappée aux **\_ importations du module** qualificateur de la classe CIM.</span><span class="sxs-lookup"><span data-stu-id="49235-119">The MIB module imports list (obtained from the **MODULE-IDENTITY** macro definition) maps to the CIM class qualifier **module\_imports**.</span></span> <span data-ttu-id="49235-120">Ce qualificateur contient une liste de noms de module séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="49235-120">This qualifier contains a comma-separated list of module names.</span></span>

 

 



