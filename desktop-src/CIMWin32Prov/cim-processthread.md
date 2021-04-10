---
description: La \_ classe CIM ProcessThread représente un lien entre un processus et les threads qui s’exécutent dans le contexte du processus.
ms.assetid: e71543c5-d9b3-4f98-93a6-08f977a26305
ms.tgt_platform: multiple
title: Classe CIM_ProcessThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessThread
- CIM_ProcessThread.PartComponent
- CIM_ProcessThread.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: afc29d1576355eda1f9e3dfd7ed55d2cca399d5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200919"
---
# <a name="cim_processthread-class"></a><span data-ttu-id="41466-103">\_Classe CIM ProcessThread</span><span class="sxs-lookup"><span data-stu-id="41466-103">CIM\_ProcessThread class</span></span>

<span data-ttu-id="41466-104">La classe **CIM \_ ProcessThread** représente un lien entre un processus et les threads qui s’exécutent dans le contexte du processus.</span><span class="sxs-lookup"><span data-stu-id="41466-104">The **CIM\_ProcessThread** class represents a link between a process and the threads running in the context of the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41466-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="41466-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="41466-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="41466-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="41466-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="41466-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="41466-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="41466-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="41466-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41466-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{B7E6042C-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ProcessThread : CIM_Component
{
  CIM_Thread  REF PartComponent;
  CIM_Process REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="41466-110">Membres</span><span class="sxs-lookup"><span data-stu-id="41466-110">Members</span></span>

<span data-ttu-id="41466-111">La classe **CIM \_ ProcessThread** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="41466-111">The **CIM\_ProcessThread** class has these types of members:</span></span>

-   [<span data-ttu-id="41466-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="41466-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41466-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="41466-113">Properties</span></span>

<span data-ttu-id="41466-114">La classe **CIM \_ ProcessThread** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="41466-114">The **CIM\_ProcessThread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41466-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="41466-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41466-116">Type de données **: \_ processus CIM**</span><span class="sxs-lookup"><span data-stu-id="41466-116">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="41466-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="41466-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41466-118">Qualificateurs : [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="41466-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="41466-119">[**\_ Processus CIM**](cim-process.md) qui décrit le processus.</span><span class="sxs-lookup"><span data-stu-id="41466-119">A [**CIM\_Process**](cim-process.md) that describes the process.</span></span>

</dd> <dt>

<span data-ttu-id="41466-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="41466-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41466-121">Type de données **: \_ thread CIM**</span><span class="sxs-lookup"><span data-stu-id="41466-121">Data type: **CIM\_Thread**</span></span>
</dt> <dt>

<span data-ttu-id="41466-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="41466-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41466-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="41466-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="41466-124">[**\_ Thread CIM**](cim-thread.md) qui décrit le thread qui s’exécute dans le contexte du processus.</span><span class="sxs-lookup"><span data-stu-id="41466-124">A [**CIM\_Thread**](cim-thread.md) that describes the thread running in the context of the process.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41466-125">Notes</span><span class="sxs-lookup"><span data-stu-id="41466-125">Remarks</span></span>

<span data-ttu-id="41466-126">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="41466-126">WMI does not implement this class.</span></span>

<span data-ttu-id="41466-127">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="41466-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="41466-128">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="41466-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="41466-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41466-129">Requirements</span></span>



| <span data-ttu-id="41466-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41466-130">Requirement</span></span> | <span data-ttu-id="41466-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="41466-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41466-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41466-132">Minimum supported client</span></span><br/> | <span data-ttu-id="41466-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41466-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41466-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41466-134">Minimum supported server</span></span><br/> | <span data-ttu-id="41466-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41466-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41466-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="41466-136">Namespace</span></span><br/>                | <span data-ttu-id="41466-137">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="41466-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="41466-138">MOF</span><span class="sxs-lookup"><span data-stu-id="41466-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41466-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41466-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="41466-140">DLL</span><span class="sxs-lookup"><span data-stu-id="41466-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41466-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41466-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41466-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41466-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41466-143">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="41466-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

