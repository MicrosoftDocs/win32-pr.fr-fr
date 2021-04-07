---
description: L' \_ objet de configuration CIM permet de regrouper des jeux de paramètres (définis dans les \_ objets de paramètre CIM) et des dépendances pour un ou plusieurs éléments système gérés.
ms.assetid: f597fe78-be50-4d31-b1eb-d219acaf1751
ms.tgt_platform: multiple
title: Classe CIM_Configuration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Configuration
- CIM_Configuration.Caption
- CIM_Configuration.Description
- CIM_Configuration.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c069f5c7186d08f01b54fe02c0568dbb4ff43d26
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748604"
---
# <a name="cim_configuration-class"></a><span data-ttu-id="1fe55-103">\_Classe de configuration CIM</span><span class="sxs-lookup"><span data-stu-id="1fe55-103">CIM\_Configuration class</span></span>

<span data-ttu-id="1fe55-104">L’objet de **\_ configuration CIM** permet de regrouper des jeux de paramètres (définis dans les objets de [**\_ paramètre CIM**](cim-setting.md) ) et des dépendances pour un ou plusieurs éléments système gérés.</span><span class="sxs-lookup"><span data-stu-id="1fe55-104">The **CIM\_Configuration** object allows the grouping of parameter sets (defined in [**CIM\_Setting**](cim-setting.md) objects) and dependencies for one or more managed system elements.</span></span> <span data-ttu-id="1fe55-105">Cet objet représente un certain comportement ou un état fonctionnel souhaité pour les éléments système gérés.</span><span class="sxs-lookup"><span data-stu-id="1fe55-105">This object represents a certain behavior, or a desired functional state for the managed system elements.</span></span> <span data-ttu-id="1fe55-106">L’état fonctionnel souhaité est généralement piloté par des exigences externes, telles que l’heure ou l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="1fe55-106">The desired functional state is typically driven by external requirements, such as time or location.</span></span> <span data-ttu-id="1fe55-107">Par exemple, pour se connecter à un système de messagerie à partir de chez vous, il existe une dépendance sur un modem. en revanche, il existe une dépendance sur une carte réseau au travail.</span><span class="sxs-lookup"><span data-stu-id="1fe55-107">For example, to connect to a mail system from home, a dependency on a modem exists; whereas, a dependency on a network adapter exists at work.</span></span> <span data-ttu-id="1fe55-108">Les paramètres des appareils logiques pertinents (dans cet exemple, modem POTS et carte réseau) peuvent être définis et regroupés par **\_ configuration CIM**.</span><span class="sxs-lookup"><span data-stu-id="1fe55-108">Settings for the pertinent logical devices (in this example, POTS modem and network adapter) can be defined and aggregated by **CIM\_Configuration**.</span></span> <span data-ttu-id="1fe55-109">Par conséquent, deux configurations de « connexion à un message » peuvent être définies en regroupant les dépendances pertinentes et les objets de [**\_ paramètre CIM**](cim-setting.md) .</span><span class="sxs-lookup"><span data-stu-id="1fe55-109">Therefore, two "Connect to Mail" configurations can be defined by grouping the relevant dependencies and [**CIM\_Setting**](cim-setting.md) objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1fe55-110">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="1fe55-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1fe55-111">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1fe55-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1fe55-112">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1fe55-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1fe55-113">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="1fe55-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fe55-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fe55-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{4C51D7AE-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_Configuration
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="1fe55-115">Membres</span><span class="sxs-lookup"><span data-stu-id="1fe55-115">Members</span></span>

<span data-ttu-id="1fe55-116">La classe de **\_ configuration CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1fe55-116">The **CIM\_Configuration** class has these types of members:</span></span>

-   [<span data-ttu-id="1fe55-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1fe55-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1fe55-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1fe55-118">Properties</span></span>

<span data-ttu-id="1fe55-119">La classe de **\_ configuration CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1fe55-119">The **CIM\_Configuration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1fe55-120">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1fe55-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe55-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1fe55-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fe55-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1fe55-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fe55-123">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1fe55-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1fe55-124">Description textuelle courte de l’objet de **\_ configuration CIM** .</span><span class="sxs-lookup"><span data-stu-id="1fe55-124">Short textual description of the **CIM\_Configuration** object.</span></span>

</dd> <dt>

<span data-ttu-id="1fe55-125">**Description**</span><span class="sxs-lookup"><span data-stu-id="1fe55-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe55-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1fe55-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fe55-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1fe55-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe55-128">Description textuelle de l’objet de **\_ configuration CIM** .</span><span class="sxs-lookup"><span data-stu-id="1fe55-128">Textual description of the **CIM\_Configuration** object.</span></span>

</dd> <dt>

<span data-ttu-id="1fe55-129">**Nom**</span><span class="sxs-lookup"><span data-stu-id="1fe55-129">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe55-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1fe55-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fe55-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1fe55-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fe55-132">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1fe55-132">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1fe55-133">Étiquette par laquelle l’objet de **\_ configuration CIM** est connu.</span><span class="sxs-lookup"><span data-stu-id="1fe55-133">Label by which the **CIM\_Configuration** object is known.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fe55-134">Notes</span><span class="sxs-lookup"><span data-stu-id="1fe55-134">Remarks</span></span>

<span data-ttu-id="1fe55-135">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="1fe55-135">WMI does not implement this class.</span></span>

<span data-ttu-id="1fe55-136">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="1fe55-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1fe55-137">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="1fe55-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fe55-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fe55-138">Requirements</span></span>



| <span data-ttu-id="1fe55-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fe55-139">Requirement</span></span> | <span data-ttu-id="1fe55-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fe55-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe55-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fe55-141">Minimum supported client</span></span><br/> | <span data-ttu-id="1fe55-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fe55-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1fe55-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fe55-143">Minimum supported server</span></span><br/> | <span data-ttu-id="1fe55-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fe55-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1fe55-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1fe55-145">Namespace</span></span><br/>                | <span data-ttu-id="1fe55-146">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1fe55-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1fe55-147">MOF</span><span class="sxs-lookup"><span data-stu-id="1fe55-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fe55-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fe55-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fe55-149">DLL</span><span class="sxs-lookup"><span data-stu-id="1fe55-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fe55-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fe55-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

