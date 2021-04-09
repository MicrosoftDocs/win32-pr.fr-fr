---
description: L' \_ Association CIM ElementConfiguration associe un \_ objet de configuration CIM à un ou plusieurs éléments système gérés. L' \_ objet de configuration CIM représente un comportement spécifique ou un état fonctionnel souhaité pour le MANAGEDSYSTEMELEMENT CIM associé \_ .
ms.assetid: 4d2af009-7466-4394-af42-72c8d96e0786
ms.tgt_platform: multiple
title: Classe CIM_ElementConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConfiguration
- CIM_ElementConfiguration.Configuration
- CIM_ElementConfiguration.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7707338a3c2268cba51146aa8462b3b244b149ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033704"
---
# <a name="cim_elementconfiguration-class"></a><span data-ttu-id="158e1-104">\_Classe CIM ElementConfiguration</span><span class="sxs-lookup"><span data-stu-id="158e1-104">CIM\_ElementConfiguration class</span></span>

<span data-ttu-id="158e1-105">L’Association **CIM \_ ElementConfiguration** associe un objet de [**\_ configuration CIM**](cim-configuration.md) à un ou plusieurs éléments système gérés.</span><span class="sxs-lookup"><span data-stu-id="158e1-105">The **CIM\_ElementConfiguration** association relates a [**CIM\_Configuration**](cim-configuration.md) object to one or more managed system elements.</span></span> <span data-ttu-id="158e1-106">L’objet de **\_ configuration CIM** représente un comportement spécifique ou un état fonctionnel souhaité pour le [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md)associé.</span><span class="sxs-lookup"><span data-stu-id="158e1-106">The **CIM\_Configuration** object represents a certain behavior, or a desired functional state for the associated [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="158e1-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="158e1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="158e1-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="158e1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="158e1-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="158e1-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="158e1-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="158e1-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="158e1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="158e1-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FC049DCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ElementConfiguration
{
  CIM_Configuration        REF Configuration;
  CIM_ManagedSystemElement REF Element;
};
```

## <a name="members"></a><span data-ttu-id="158e1-112">Membres</span><span class="sxs-lookup"><span data-stu-id="158e1-112">Members</span></span>

<span data-ttu-id="158e1-113">La classe **CIM \_ ElementConfiguration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="158e1-113">The **CIM\_ElementConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="158e1-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="158e1-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="158e1-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="158e1-115">Properties</span></span>

<span data-ttu-id="158e1-116">La classe **CIM \_ ElementConfiguration** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="158e1-116">The **CIM\_ElementConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="158e1-117">**Configuration**</span><span class="sxs-lookup"><span data-stu-id="158e1-117">**Configuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158e1-118">Type de données **: \_ configuration CIM**</span><span class="sxs-lookup"><span data-stu-id="158e1-118">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="158e1-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="158e1-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="158e1-120">Référence à l’objet de [**\_ configuration CIM**](cim-configuration.md) qui regroupe les paramètres et les dépendances associés à l’élément système géré.</span><span class="sxs-lookup"><span data-stu-id="158e1-120">Reference to the [**CIM\_Configuration**](cim-configuration.md) object that groups the settings and dependencies associated with the managed system element.</span></span>

</dd> <dt>

<span data-ttu-id="158e1-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="158e1-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="158e1-122">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="158e1-122">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="158e1-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="158e1-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="158e1-124">Référence à l’élément système managé.</span><span class="sxs-lookup"><span data-stu-id="158e1-124">Reference to the managed system element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="158e1-125">Notes</span><span class="sxs-lookup"><span data-stu-id="158e1-125">Remarks</span></span>

<span data-ttu-id="158e1-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="158e1-126">WMI does not implement this class.</span></span>

<span data-ttu-id="158e1-127">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="158e1-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="158e1-128">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="158e1-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="158e1-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="158e1-129">Requirements</span></span>



| <span data-ttu-id="158e1-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="158e1-130">Requirement</span></span> | <span data-ttu-id="158e1-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="158e1-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="158e1-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="158e1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="158e1-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="158e1-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="158e1-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="158e1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="158e1-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="158e1-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="158e1-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="158e1-136">Namespace</span></span><br/>                | <span data-ttu-id="158e1-137">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="158e1-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="158e1-138">MOF</span><span class="sxs-lookup"><span data-stu-id="158e1-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="158e1-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="158e1-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="158e1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="158e1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="158e1-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="158e1-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




