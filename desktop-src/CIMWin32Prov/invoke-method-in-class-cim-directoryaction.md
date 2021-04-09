---
description: La méthode Invoke de la \_ classe CIM DirectoryAction prend une mesure particulière. Les détails sur la façon dont la méthode exécute l’action sont spécifiques à l’implémentation. Cette méthode est héritée de l' \_ action CIM.
ms.assetid: e919dfdb-a52d-4bcb-abff-e1273c406226
ms.tgt_platform: multiple
title: Méthode Invoke de la classe CIM_DirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f30184fe46cd8e8b9a595545ccba9a7d738af18e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860934"
---
# <a name="invoke-method-of-the-cim_directoryaction-class"></a><span data-ttu-id="ddb5f-105">Méthode Invoke de la \_ classe CIM DirectoryAction</span><span class="sxs-lookup"><span data-stu-id="ddb5f-105">Invoke method of the CIM\_DirectoryAction class</span></span>

<span data-ttu-id="ddb5f-106">La méthode **Invoke** de la classe [**CIM \_ DirectoryAction**](cim-directoryaction.md) prend une mesure particulière.</span><span class="sxs-lookup"><span data-stu-id="ddb5f-106">The **Invoke** method of the [**CIM\_DirectoryAction**](cim-directoryaction.md) class takes a particular action.</span></span> <span data-ttu-id="ddb5f-107">Les détails sur la façon dont la méthode exécute l’action sont spécifiques à l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="ddb5f-107">Details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="ddb5f-108">Cette méthode est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="ddb5f-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ddb5f-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="ddb5f-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ddb5f-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ddb5f-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ddb5f-111">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ddb5f-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ddb5f-112">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ddb5f-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ddb5f-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddb5f-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="ddb5f-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddb5f-114">Parameters</span></span>

<span data-ttu-id="ddb5f-115">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ddb5f-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ddb5f-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ddb5f-116">Return value</span></span>

<span data-ttu-id="ddb5f-117">Retourne la valeur 0 (zéro) en cas de réussite, 1 (un) si la méthode n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="ddb5f-117">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddb5f-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ddb5f-118">Remarks</span></span>

<span data-ttu-id="ddb5f-119">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="ddb5f-119">WMI does not implement this class.</span></span>

<span data-ttu-id="ddb5f-120">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="ddb5f-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ddb5f-121">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ddb5f-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddb5f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddb5f-122">Requirements</span></span>



| <span data-ttu-id="ddb5f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddb5f-123">Requirement</span></span> | <span data-ttu-id="ddb5f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddb5f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb5f-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddb5f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ddb5f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddb5f-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ddb5f-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddb5f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ddb5f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddb5f-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ddb5f-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ddb5f-129">Namespace</span></span><br/>                | <span data-ttu-id="ddb5f-130">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ddb5f-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ddb5f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ddb5f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddb5f-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ddb5f-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ddb5f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ddb5f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddb5f-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddb5f-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddb5f-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddb5f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb5f-136">\_DIRECTORYACTION CIM</span><span class="sxs-lookup"><span data-stu-id="ddb5f-136">CIM\_DirectoryAction</span></span>](invoke-method-in-class-cim-directoryaction.md)
</dt> <dt>

[<span data-ttu-id="ddb5f-137">**\_DIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="ddb5f-137">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> </dl>

 

