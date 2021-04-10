---
description: La méthode Reset de la \_ classe CIM CacheMemory demande une réinitialisation de l’unité logique.
ms.assetid: 499426e9-a10f-4d34-a9af-721c2f59d551
ms.tgt_platform: multiple
title: Méthode Reset de la classe CIM_CacheMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CacheMemory.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 58c73f392ab6e380c29374aa8116918e788e1ddd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861221"
---
# <a name="reset-method-of-the-cim_cachememory-class"></a><span data-ttu-id="e74f2-103">Méthode Reset de la \_ classe CIM CacheMemory</span><span class="sxs-lookup"><span data-stu-id="e74f2-103">Reset method of the CIM\_CacheMemory class</span></span>

<span data-ttu-id="e74f2-104">La méthode **Reset** de la \_ classe CIM CacheMemory demande une réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="e74f2-104">The **Reset** method of the CIM\_CacheMemory class requests a reset of the logical device.</span></span> <span data-ttu-id="e74f2-105">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e74f2-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e74f2-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e74f2-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e74f2-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e74f2-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e74f2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e74f2-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="e74f2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e74f2-109">Parameters</span></span>

<span data-ttu-id="e74f2-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e74f2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e74f2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e74f2-111">Return value</span></span>

<span data-ttu-id="e74f2-112">Retourne 0 (zéro) si la requête a été exécutée avec succès, 1 (un) si la demande n’est pas prise en charge, et une autre valeur si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e74f2-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="e74f2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e74f2-113">Remarks</span></span>

<span data-ttu-id="e74f2-114">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="e74f2-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e74f2-115">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e74f2-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="e74f2-116">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="e74f2-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e74f2-117">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e74f2-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e74f2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e74f2-118">Requirements</span></span>



| <span data-ttu-id="e74f2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e74f2-119">Requirement</span></span> | <span data-ttu-id="e74f2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e74f2-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e74f2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e74f2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e74f2-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e74f2-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e74f2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e74f2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e74f2-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e74f2-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e74f2-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e74f2-125">Namespace</span></span><br/>                | <span data-ttu-id="e74f2-126">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e74f2-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e74f2-127">MOF</span><span class="sxs-lookup"><span data-stu-id="e74f2-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e74f2-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e74f2-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e74f2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e74f2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e74f2-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e74f2-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e74f2-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e74f2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e74f2-132">\_CACHEMEMORY CIM</span><span class="sxs-lookup"><span data-stu-id="e74f2-132">CIM\_CacheMemory</span></span>](reset-method-in-class-cim-cachememory.md)
</dt> <dt>

[<span data-ttu-id="e74f2-133">**\_CACHEMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="e74f2-133">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> </dl>

 

 




