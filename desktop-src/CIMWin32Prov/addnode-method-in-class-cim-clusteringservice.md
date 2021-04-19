---
description: Met un nouveau système d’ordinateur dans un cluster.
ms.assetid: 26d9428e-99de-4dcb-96ed-d773f28e015a
ms.tgt_platform: multiple
title: AddNode, méthode de la classe CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.AddNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1769ebb876fd2ae99c800a61b80d339a850ab232
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515781"
---
# <a name="addnode-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="1b7cc-103">AddNode, méthode de la \_ classe CIM ClusteringService</span><span class="sxs-lookup"><span data-stu-id="1b7cc-103">AddNode method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="1b7cc-104">La méthode **AddNode** permet de placer un nouveau système d’ordinateur dans un cluster.</span><span class="sxs-lookup"><span data-stu-id="1b7cc-104">The **AddNode** method brings a new computer system into a cluster.</span></span> <span data-ttu-id="1b7cc-105">Le nœud à ajouter est spécifié en tant que paramètre de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1b7cc-105">The node to be added is specified as a parameter to the method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b7cc-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="1b7cc-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1b7cc-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1b7cc-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1b7cc-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1b7cc-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1b7cc-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1b7cc-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b7cc-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b7cc-110">Syntax</span></span>


```mof
uint32 AddNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a><span data-ttu-id="1b7cc-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b7cc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b7cc-112">*CS* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1b7cc-112">*CS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7cc-113">Référence au système de l’ordinateur à ajouter au cluster.</span><span class="sxs-lookup"><span data-stu-id="1b7cc-113">Reference to the computer system to add to the cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b7cc-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1b7cc-114">Return value</span></span>

<span data-ttu-id="1b7cc-115">Retourne la valeur 0 (zéro) en cas de réussite, 1 (un) si l’opération n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="1b7cc-115">Returns a value of 0 (zero) on success, 1 (one) if the operation is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b7cc-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1b7cc-116">Remarks</span></span>

<span data-ttu-id="1b7cc-117">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="1b7cc-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1b7cc-118">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1b7cc-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1b7cc-119">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="1b7cc-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1b7cc-120">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="1b7cc-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b7cc-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b7cc-121">Requirements</span></span>



| <span data-ttu-id="1b7cc-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b7cc-122">Requirement</span></span> | <span data-ttu-id="1b7cc-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b7cc-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b7cc-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b7cc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1b7cc-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b7cc-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b7cc-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b7cc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1b7cc-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b7cc-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b7cc-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1b7cc-128">Namespace</span></span><br/>                | <span data-ttu-id="1b7cc-129">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1b7cc-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1b7cc-130">MOF</span><span class="sxs-lookup"><span data-stu-id="1b7cc-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b7cc-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b7cc-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b7cc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1b7cc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b7cc-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b7cc-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b7cc-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b7cc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b7cc-135">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1b7cc-135">**CIM\_ClusteringService**</span></span>](addnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="1b7cc-136">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1b7cc-136">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

