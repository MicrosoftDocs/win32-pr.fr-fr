---
description: La méthode EvictNode supprime un système informatique d’un cluster. Le nœud à supprimer est spécifié en tant que paramètre de la méthode.
ms.assetid: 4691d536-ade3-4a02-bc28-e31ebaf5d9e4
ms.tgt_platform: multiple
title: Méthode EvictNode de la classe CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.EvictNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d68ddc1adc0af335dcf2d4139cf7c1f0a381d986
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748140"
---
# <a name="evictnode-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="2e163-104">Méthode EvictNode de la \_ classe CIM ClusteringService</span><span class="sxs-lookup"><span data-stu-id="2e163-104">EvictNode method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="2e163-105">La méthode **EvictNode** supprime un système informatique d’un cluster.</span><span class="sxs-lookup"><span data-stu-id="2e163-105">The **EvictNode** method removes a computer system from a cluster.</span></span> <span data-ttu-id="2e163-106">Le nœud à supprimer est spécifié en tant que paramètre de la méthode.</span><span class="sxs-lookup"><span data-stu-id="2e163-106">The node to be evicted is specified as a parameter to the method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e163-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="2e163-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2e163-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2e163-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2e163-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="2e163-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2e163-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2e163-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e163-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e163-111">Syntax</span></span>


```mof
uint32 EvictNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a><span data-ttu-id="2e163-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e163-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e163-113">*CS* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e163-113">*CS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e163-114">Référence au système informatique à supprimer du cluster.</span><span class="sxs-lookup"><span data-stu-id="2e163-114">Reference to the computer system to remove from the cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e163-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e163-115">Return value</span></span>

<span data-ttu-id="2e163-116">Retourne 0 (zéro) si le système informatique est correctement expulsé, 1 (un) si la méthode n’est pas prise en charge, et tout autre nombre si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2e163-116">Returns 0 (zero) if the computer system is successfully evicted, 1 (one) if the method is not supported, and any other number if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e163-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2e163-117">Remarks</span></span>

<span data-ttu-id="2e163-118">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="2e163-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="2e163-119">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2e163-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="2e163-120">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="2e163-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2e163-121">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2e163-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e163-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e163-122">Requirements</span></span>



| <span data-ttu-id="2e163-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e163-123">Requirement</span></span> | <span data-ttu-id="2e163-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e163-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e163-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e163-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2e163-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e163-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e163-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e163-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2e163-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e163-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e163-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2e163-129">Namespace</span></span><br/>                | <span data-ttu-id="2e163-130">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2e163-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e163-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2e163-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e163-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e163-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e163-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2e163-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e163-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e163-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e163-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e163-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e163-136">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2e163-136">**CIM\_ClusteringService**</span></span>](evictnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="2e163-137">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2e163-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

