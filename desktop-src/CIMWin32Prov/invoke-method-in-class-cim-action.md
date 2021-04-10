---
description: La méthode Invoke de la \_ classe d’action CIM prend une mesure particulière. Les détails de la méthode d’exécution de l’action sont spécifiques à l’implémentation.
ms.assetid: 4f0be560-bd78-4c7f-b6e3-ca86837a84f9
ms.tgt_platform: multiple
title: Méthode Invoke de la classe CIM_Action
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Action.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e02e414fb05e0dd4ea97c3e3a4d87659fed4c963
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860941"
---
# <a name="invoke-method-of-the-cim_action-class"></a><span data-ttu-id="1d8d5-104">Méthode Invoke de la \_ classe d’action CIM</span><span class="sxs-lookup"><span data-stu-id="1d8d5-104">Invoke method of the CIM\_Action class</span></span>

<span data-ttu-id="1d8d5-105">La méthode **Invoke** de la classe d' [**\_ action CIM**](cim-action.md) prend une mesure particulière.</span><span class="sxs-lookup"><span data-stu-id="1d8d5-105">The **Invoke** method of the [**CIM\_Action**](cim-action.md) class takes a particular action.</span></span> <span data-ttu-id="1d8d5-106">Les détails de la méthode d’exécution de l’action sont spécifiques à l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="1d8d5-106">The details of how the method performs the action is implementation-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d8d5-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="1d8d5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1d8d5-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1d8d5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1d8d5-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1d8d5-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1d8d5-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1d8d5-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d8d5-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d8d5-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="1d8d5-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d8d5-112">Parameters</span></span>

<span data-ttu-id="1d8d5-113">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1d8d5-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d8d5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d8d5-114">Return value</span></span>

<span data-ttu-id="1d8d5-115">Retourne la valeur 0 (zéro) en cas de réussite, 1 (un) si la méthode n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="1d8d5-115">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d8d5-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1d8d5-116">Remarks</span></span>

<span data-ttu-id="1d8d5-117">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="1d8d5-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1d8d5-118">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1d8d5-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1d8d5-119">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="1d8d5-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1d8d5-120">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="1d8d5-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d8d5-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d8d5-121">Requirements</span></span>



| <span data-ttu-id="1d8d5-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d8d5-122">Requirement</span></span> | <span data-ttu-id="1d8d5-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d8d5-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d8d5-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d8d5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1d8d5-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d8d5-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d8d5-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d8d5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1d8d5-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d8d5-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d8d5-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1d8d5-128">Namespace</span></span><br/>                | <span data-ttu-id="1d8d5-129">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1d8d5-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d8d5-130">MOF</span><span class="sxs-lookup"><span data-stu-id="1d8d5-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d8d5-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d8d5-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d8d5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1d8d5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d8d5-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d8d5-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d8d5-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d8d5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d8d5-135">\_Action CIM</span><span class="sxs-lookup"><span data-stu-id="1d8d5-135">CIM\_Action</span></span>](invoke-method-in-class-cim-action.md)
</dt> <dt>

[<span data-ttu-id="1d8d5-136">**\_Action CIM**</span><span class="sxs-lookup"><span data-stu-id="1d8d5-136">**CIM\_Action**</span></span>](cim-action.md)
</dt> <dt>

[<span data-ttu-id="1d8d5-137">Classes CIM</span><span class="sxs-lookup"><span data-stu-id="1d8d5-137">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

