---
description: La méthode Reset demande une réinitialisation de l’unité logique. Cette méthode est héritée de CIM \_ LogicalDevice.
ms.assetid: 874f8eb4-784a-41ab-9c58-9e48486a7f71
ms.tgt_platform: multiple
title: Méthode Reset de la classe CIM_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskPartition.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 236a8c018b584fbc2d5ef1d13b0429d946b868fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200895"
---
# <a name="reset-method-of-the-cim_diskpartition-class"></a><span data-ttu-id="3c5ad-104">Méthode Reset de la \_ classe CIM DiskPartition</span><span class="sxs-lookup"><span data-stu-id="3c5ad-104">Reset method of the CIM\_DiskPartition class</span></span>

<span data-ttu-id="3c5ad-105">La méthode **Reset** demande une réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="3c5ad-106">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3c5ad-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c5ad-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3c5ad-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3c5ad-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3c5ad-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c5ad-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="3c5ad-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c5ad-110">Parameters</span></span>

<span data-ttu-id="3c5ad-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c5ad-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c5ad-112">Return value</span></span>

<span data-ttu-id="3c5ad-113">Retourne 0 (zéro) si la requête a été exécutée avec succès, 1 (un) si la demande n’est pas prise en charge, et une autre valeur si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c5ad-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3c5ad-114">Remarks</span></span>

<span data-ttu-id="3c5ad-115">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3c5ad-116">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3c5ad-117">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3c5ad-118">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="3c5ad-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c5ad-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c5ad-119">Requirements</span></span>



| <span data-ttu-id="3c5ad-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c5ad-120">Requirement</span></span> | <span data-ttu-id="3c5ad-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c5ad-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c5ad-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c5ad-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3c5ad-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c5ad-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c5ad-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c5ad-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3c5ad-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c5ad-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c5ad-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c5ad-126">Namespace</span></span><br/>                | <span data-ttu-id="3c5ad-127">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3c5ad-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3c5ad-128">MOF</span><span class="sxs-lookup"><span data-stu-id="3c5ad-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c5ad-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c5ad-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c5ad-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3c5ad-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c5ad-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c5ad-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c5ad-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c5ad-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c5ad-133">\_DISKPARTITION CIM</span><span class="sxs-lookup"><span data-stu-id="3c5ad-133">CIM\_DiskPartition</span></span>](reset-method-in-class-cim-diskpartition.md)
</dt> <dt>

[<span data-ttu-id="3c5ad-134">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="3c5ad-134">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> </dl>

 

 




