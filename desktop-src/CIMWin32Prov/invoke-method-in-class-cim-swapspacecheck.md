---
description: La méthode Invoke de la \_ classe CIM SwapSpaceCheck évalue une vérification particulière. Les détails de la façon dont la méthode évalue un contrôle particulier dans un contexte CIM sont décrits par les sous-classes de vérification CIM non abstraites \_ . Cette méthode est héritée de la \_ vérification CIM.
ms.assetid: eee84cf1-dbd6-4557-b9ff-eb19c8042db8
ms.tgt_platform: multiple
title: Méthode Invoke de la classe CIM_SwapSpaceCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwapSpaceCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b23d9aa0f9563f68804eaff1ac969679f220dce2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200945"
---
# <a name="invoke-method-of-the-cim_swapspacecheck-class"></a><span data-ttu-id="55b42-105">Méthode Invoke de la \_ classe CIM SwapSpaceCheck</span><span class="sxs-lookup"><span data-stu-id="55b42-105">Invoke method of the CIM\_SwapSpaceCheck class</span></span>

<span data-ttu-id="55b42-106">La méthode **Invoke** de la classe [**CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md) évalue une vérification particulière.</span><span class="sxs-lookup"><span data-stu-id="55b42-106">The **Invoke** method of the [**CIM\_SwapSpaceCheck**](cim-swapspacecheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="55b42-107">Les détails de la façon dont la méthode évalue un contrôle particulier dans un contexte CIM sont décrits par les sous-classes de [**\_ vérification CIM**](cim-check.md) non abstraites.</span><span class="sxs-lookup"><span data-stu-id="55b42-107">The details of how the method evaluates a particular check in a CIM context are described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="55b42-108">Cette méthode est héritée de la **\_ vérification CIM**.</span><span class="sxs-lookup"><span data-stu-id="55b42-108">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55b42-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="55b42-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="55b42-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="55b42-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="55b42-111">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="55b42-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="55b42-112">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="55b42-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="55b42-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55b42-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="55b42-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55b42-114">Parameters</span></span>

<span data-ttu-id="55b42-115">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="55b42-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="55b42-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="55b42-116">Return value</span></span>

<span data-ttu-id="55b42-117">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="55b42-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="55b42-118">Notes</span><span class="sxs-lookup"><span data-stu-id="55b42-118">Remarks</span></span>

<span data-ttu-id="55b42-119">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="55b42-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="55b42-120">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="55b42-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="55b42-121">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="55b42-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="55b42-122">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="55b42-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="55b42-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55b42-123">Requirements</span></span>



| <span data-ttu-id="55b42-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55b42-124">Requirement</span></span> | <span data-ttu-id="55b42-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="55b42-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55b42-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55b42-126">Minimum supported client</span></span><br/> | <span data-ttu-id="55b42-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55b42-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55b42-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55b42-128">Minimum supported server</span></span><br/> | <span data-ttu-id="55b42-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55b42-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55b42-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="55b42-130">Namespace</span></span><br/>                | <span data-ttu-id="55b42-131">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="55b42-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55b42-132">MOF</span><span class="sxs-lookup"><span data-stu-id="55b42-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55b42-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55b42-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55b42-134">DLL</span><span class="sxs-lookup"><span data-stu-id="55b42-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55b42-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55b42-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55b42-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55b42-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b42-137">\_SWAPSPACECHECK CIM</span><span class="sxs-lookup"><span data-stu-id="55b42-137">CIM\_SwapSpaceCheck</span></span>](invoke-method-in-class-cim-swapspacecheck.md)
</dt> <dt>

[<span data-ttu-id="55b42-138">**\_SWAPSPACECHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="55b42-138">**CIM\_SwapSpaceCheck**</span></span>](cim-swapspacecheck.md)
</dt> </dl>

 

