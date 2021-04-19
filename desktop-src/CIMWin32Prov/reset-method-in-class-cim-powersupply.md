---
description: La méthode Reset de la \_ classe d’alimentation CIM demande une réinitialisation de l’unité logique.
ms.assetid: 55fa8408-215b-4e24-a92a-96f44f28c589
ms.tgt_platform: multiple
title: Méthode Reset de la classe CIM_PowerSupply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PowerSupply.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c1bb483c35c56f8d50a16ff50f5b44e1b9ac52db
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513951"
---
# <a name="reset-method-of-the-cim_powersupply-class"></a><span data-ttu-id="9a0d8-103">Méthode Reset de la \_ classe d’alimentation CIM</span><span class="sxs-lookup"><span data-stu-id="9a0d8-103">Reset method of the CIM\_PowerSupply class</span></span>

<span data-ttu-id="9a0d8-104">La méthode **Reset** de la \_ classe d’alimentation CIM demande une réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-104">The **Reset** method of the CIM\_PowerSupply class requests a reset of the logical device.</span></span> <span data-ttu-id="9a0d8-105">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9a0d8-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a0d8-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9a0d8-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9a0d8-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9a0d8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a0d8-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="9a0d8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a0d8-109">Parameters</span></span>

<span data-ttu-id="9a0d8-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a0d8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9a0d8-111">Return value</span></span>

<span data-ttu-id="9a0d8-112">Retourne 0 (zéro) si la requête a été exécutée avec succès, 1 (zéro) si la demande n’est pas prise en charge, et une autre valeur si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-112">Returns 0 (zero) if the request was successfully executed, 1 (zero) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a0d8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9a0d8-113">Remarks</span></span>

<span data-ttu-id="9a0d8-114">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9a0d8-115">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9a0d8-116">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9a0d8-117">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9a0d8-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a0d8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a0d8-118">Requirements</span></span>



| <span data-ttu-id="9a0d8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a0d8-119">Requirement</span></span> | <span data-ttu-id="9a0d8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a0d8-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a0d8-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a0d8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9a0d8-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a0d8-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a0d8-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a0d8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9a0d8-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a0d8-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a0d8-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9a0d8-125">Namespace</span></span><br/>                | <span data-ttu-id="9a0d8-126">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9a0d8-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9a0d8-127">MOF</span><span class="sxs-lookup"><span data-stu-id="9a0d8-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a0d8-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a0d8-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a0d8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9a0d8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a0d8-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a0d8-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a0d8-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a0d8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a0d8-132">\_Alimentation CIM</span><span class="sxs-lookup"><span data-stu-id="9a0d8-132">CIM\_PowerSupply</span></span>](reset-method-in-class-cim-powersupply.md)
</dt> <dt>

[<span data-ttu-id="9a0d8-133">**\_Alimentation CIM**</span><span class="sxs-lookup"><span data-stu-id="9a0d8-133">**CIM\_PowerSupply**</span></span>](cim-powersupply.md)
</dt> </dl>

 

 




