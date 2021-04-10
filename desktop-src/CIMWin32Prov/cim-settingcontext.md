---
description: La \_ classe SETTINGCONTEXT CIM associe les objets de configuration aux objets Setting.
ms.assetid: 8ed7e150-b4e6-4fd4-809b-32e870b559c4
ms.tgt_platform: multiple
title: Classe CIM_SettingContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingContext
- CIM_SettingContext.Context
- CIM_SettingContext.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 867be99e1630f02c0163516ad7a86cf84c2fac13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950517"
---
# <a name="cim_settingcontext-class"></a><span data-ttu-id="0beb4-103">\_Classe CIM SettingContext</span><span class="sxs-lookup"><span data-stu-id="0beb4-103">CIM\_SettingContext class</span></span>

<span data-ttu-id="0beb4-104">La **classe \_ SettingContext CIM** associe les objets de configuration aux objets Setting.</span><span class="sxs-lookup"><span data-stu-id="0beb4-104">The **CIM\_SettingContext** class associates configuration objects with setting objects.</span></span> <span data-ttu-id="0beb4-105">Par exemple, les paramètres d’une carte réseau peuvent changer en fonction du site ou du réseau auquel son système informatique d’hébergement est attaché.</span><span class="sxs-lookup"><span data-stu-id="0beb4-105">For example, a network adapter's settings could change based on the site or network to which its hosting computer system is attached.</span></span> <span data-ttu-id="0beb4-106">Dans ce cas, le système informatique a deux objets de configuration différents, qui correspondent aux différences de configuration réseau pour les deux segments de réseau.</span><span class="sxs-lookup"><span data-stu-id="0beb4-106">In which case, the computer system would have two different configuration objects, corresponding to the differences in network configuration for the two network segments.</span></span> <span data-ttu-id="0beb4-107">Une configuration agrège un objet de paramètre pour la carte réseau lors de l’utilisation d’un segment ; en revanche, l’autre configuration agrège un autre objet de paramètre de carte réseau, propre à un autre segment.</span><span class="sxs-lookup"><span data-stu-id="0beb4-107">One configuration would aggregate a setting object for the network adapter when operating on one segment; whereas, the other configuration would aggregate a different network adapter setting object, specific to another segment.</span></span> <span data-ttu-id="0beb4-108">Notez que de nombreux paramètres de l’ordinateur sont indépendants de la configuration du réseau.</span><span class="sxs-lookup"><span data-stu-id="0beb4-108">Note that many computer settings are independent of the network configuration.</span></span> <span data-ttu-id="0beb4-109">Par exemple, les deux configurations regroupent le même objet de paramètre pour la résolution de l’écran du système de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0beb4-109">For example, both configurations would aggregate the same setting object for the computer system's monitor resolution.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0beb4-110">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="0beb4-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0beb4-111">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0beb4-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0beb4-112">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0beb4-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0beb4-113">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0beb4-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0beb4-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0beb4-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{F0B752E8-DB30-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_SettingContext
{
  CIM_Configuration REF Context;
  CIM_Setting       REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="0beb4-115">Membres</span><span class="sxs-lookup"><span data-stu-id="0beb4-115">Members</span></span>

<span data-ttu-id="0beb4-116">La classe **CIM \_ SettingContext** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0beb4-116">The **CIM\_SettingContext** class has these types of members:</span></span>

-   [<span data-ttu-id="0beb4-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0beb4-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0beb4-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0beb4-118">Properties</span></span>

<span data-ttu-id="0beb4-119">La classe **CIM \_ SettingContext** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0beb4-119">The **CIM\_SettingContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0beb4-120">**Contexte**</span><span class="sxs-lookup"><span data-stu-id="0beb4-120">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0beb4-121">Type de données **: \_ configuration CIM**</span><span class="sxs-lookup"><span data-stu-id="0beb4-121">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="0beb4-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0beb4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0beb4-123">Qualificateurs : [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0beb4-123">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0beb4-124">Référence à l’objet de configuration qui agrège le paramètre.</span><span class="sxs-lookup"><span data-stu-id="0beb4-124">Reference to the configuration object that aggregates the setting.</span></span>

</dd> <dt>

<span data-ttu-id="0beb4-125">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="0beb4-125">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0beb4-126">Type de données **: \_ paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="0beb4-126">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="0beb4-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0beb4-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0beb4-128">Référence à un paramètre agrégé.</span><span class="sxs-lookup"><span data-stu-id="0beb4-128">Reference to an aggregated setting.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0beb4-129">Notes</span><span class="sxs-lookup"><span data-stu-id="0beb4-129">Remarks</span></span>

<span data-ttu-id="0beb4-130">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="0beb4-130">WMI does not implement this class.</span></span>

<span data-ttu-id="0beb4-131">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="0beb4-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0beb4-132">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0beb4-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0beb4-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0beb4-133">Requirements</span></span>



| <span data-ttu-id="0beb4-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0beb4-134">Requirement</span></span> | <span data-ttu-id="0beb4-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="0beb4-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0beb4-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0beb4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0beb4-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0beb4-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0beb4-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0beb4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0beb4-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0beb4-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0beb4-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0beb4-140">Namespace</span></span><br/>                | <span data-ttu-id="0beb4-141">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0beb4-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0beb4-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0beb4-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0beb4-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0beb4-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0beb4-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0beb4-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0beb4-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0beb4-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

