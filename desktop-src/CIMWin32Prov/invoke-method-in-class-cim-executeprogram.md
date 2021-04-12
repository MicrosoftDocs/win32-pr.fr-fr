---
description: La méthode Invoke de la \_ classe CIM ExecuteProgram prend une mesure particulière. Les détails de la façon dont la méthode effectue l’action sont spécifiques à l’implémentation. Cette méthode est héritée de l' \_ action CIM.
ms.assetid: 14a12fae-14a6-412a-a778-8dd34a5843d1
ms.tgt_platform: multiple
title: Méthode Invoke de la classe CIM_ExecuteProgram
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExecuteProgram.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bdf9a4edb78bb47c0354991d161339099e4dc49f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393035"
---
# <a name="invoke-method-of-the-cim_executeprogram-class"></a><span data-ttu-id="8f86a-105">Méthode Invoke de la \_ classe CIM ExecuteProgram</span><span class="sxs-lookup"><span data-stu-id="8f86a-105">Invoke method of the CIM\_ExecuteProgram class</span></span>

<span data-ttu-id="8f86a-106">La méthode **Invoke** de la classe [**CIM \_ ExecuteProgram**](cim-executeprogram.md) prend une mesure particulière.</span><span class="sxs-lookup"><span data-stu-id="8f86a-106">The **Invoke** method of the [**CIM\_ExecuteProgram**](cim-executeprogram.md) class takes a particular action.</span></span> <span data-ttu-id="8f86a-107">Les détails de la façon dont la méthode effectue l’action sont spécifiques à l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="8f86a-107">The details of how the method performs the action are implementation specific.</span></span> <span data-ttu-id="8f86a-108">Cette méthode est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="8f86a-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f86a-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="8f86a-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8f86a-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8f86a-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8f86a-111">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="8f86a-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8f86a-112">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8f86a-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f86a-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f86a-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="8f86a-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f86a-114">Parameters</span></span>

<span data-ttu-id="8f86a-115">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8f86a-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f86a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8f86a-116">Return value</span></span>

<span data-ttu-id="8f86a-117">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="8f86a-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f86a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="8f86a-118">Remarks</span></span>

<span data-ttu-id="8f86a-119">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="8f86a-119">WMI does not implement this class.</span></span>

<span data-ttu-id="8f86a-120">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="8f86a-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8f86a-121">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="8f86a-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f86a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f86a-122">Requirements</span></span>



| <span data-ttu-id="8f86a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f86a-123">Requirement</span></span> | <span data-ttu-id="8f86a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f86a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f86a-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f86a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8f86a-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f86a-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f86a-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f86a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8f86a-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f86a-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f86a-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8f86a-129">Namespace</span></span><br/>                | <span data-ttu-id="8f86a-130">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8f86a-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f86a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="8f86a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f86a-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f86a-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f86a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8f86a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f86a-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f86a-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f86a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f86a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f86a-136">\_EXECUTEPROGRAM CIM</span><span class="sxs-lookup"><span data-stu-id="8f86a-136">CIM\_ExecuteProgram</span></span>](invoke-method-in-class-cim-executeprogram.md)
</dt> <dt>

[<span data-ttu-id="8f86a-137">**\_EXECUTEPROGRAM CIM**</span><span class="sxs-lookup"><span data-stu-id="8f86a-137">**CIM\_ExecuteProgram**</span></span>](cim-executeprogram.md)
</dt> </dl>

 

