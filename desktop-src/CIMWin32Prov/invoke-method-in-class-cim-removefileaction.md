---
description: La méthode Invoke de la \_ classe CIM RemoveFileAction prend une mesure particulière. Les détails de la méthode d’exécution de l’action sont spécifiques à l’implémentation. Cette méthode est héritée de l' \_ action CIM.
ms.assetid: 7fc33654-a51b-41cf-a5b4-ef08fd6e40ac
ms.tgt_platform: multiple
title: Méthode Invoke de la classe CIM_RemoveFileAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoveFileAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a371ad1f7b1da874b6a049b04d5f50ec694cf181
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515151"
---
# <a name="invoke-method-of-the-cim_removefileaction-class"></a><span data-ttu-id="c5df3-105">Méthode Invoke de la \_ classe CIM RemoveFileAction</span><span class="sxs-lookup"><span data-stu-id="c5df3-105">Invoke method of the CIM\_RemoveFileAction class</span></span>

<span data-ttu-id="c5df3-106">La méthode **Invoke** de la classe [**CIM \_ RemoveFileAction**](cim-removefileaction.md) prend une mesure particulière.</span><span class="sxs-lookup"><span data-stu-id="c5df3-106">The **Invoke** method of the [**CIM\_RemoveFileAction**](cim-removefileaction.md) class takes a particular action.</span></span> <span data-ttu-id="c5df3-107">Les détails de la méthode d’exécution de l’action sont spécifiques à l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="c5df3-107">The details of how the method performs the action is implementation specific.</span></span> <span data-ttu-id="c5df3-108">Cette méthode est héritée de l' [**\_ action CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="c5df3-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5df3-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="c5df3-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c5df3-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c5df3-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c5df3-111">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c5df3-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c5df3-112">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c5df3-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5df3-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5df3-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="c5df3-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5df3-114">Parameters</span></span>

<span data-ttu-id="c5df3-115">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c5df3-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c5df3-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5df3-116">Return value</span></span>

<span data-ttu-id="c5df3-117">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="c5df3-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5df3-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c5df3-118">Remarks</span></span>

<span data-ttu-id="c5df3-119">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="c5df3-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c5df3-120">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c5df3-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c5df3-121">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="c5df3-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c5df3-122">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="c5df3-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5df3-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5df3-123">Requirements</span></span>



| <span data-ttu-id="c5df3-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5df3-124">Requirement</span></span> | <span data-ttu-id="c5df3-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5df3-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5df3-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5df3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c5df3-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5df3-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c5df3-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5df3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c5df3-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5df3-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5df3-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c5df3-130">Namespace</span></span><br/>                | <span data-ttu-id="c5df3-131">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="c5df3-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c5df3-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c5df3-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5df3-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5df3-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5df3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c5df3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5df3-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5df3-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5df3-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5df3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5df3-137">\_REMOVEFILEACTION CIM</span><span class="sxs-lookup"><span data-stu-id="c5df3-137">CIM\_RemoveFileAction</span></span>](invoke-method-in-class-cim-removefileaction.md)
</dt> <dt>

[<span data-ttu-id="c5df3-138">**\_REMOVEFILEACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="c5df3-138">**CIM\_RemoveFileAction**</span></span>](cim-removefileaction.md)
</dt> </dl>

 

