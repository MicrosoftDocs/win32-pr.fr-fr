---
description: 'Méthode Reset de la classe CIM_DiscreteSensor : la méthode Reset demande une réinitialisation de l’unité logique. Cette méthode est héritée de CIM \_ LogicalDevice.'
ms.assetid: 4ddbad2a-e586-434a-a33e-7d60dcb67b3a
ms.tgt_platform: multiple
title: Méthode Reset de la classe CIM_DiscreteSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiscreteSensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: aecda4b40a70c72679c3edff7b30f6ba548938cf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096907"
---
# <a name="reset-method-of-the-cim_discretesensor-class"></a><span data-ttu-id="df4d5-104">Méthode Reset de la \_ classe CIM DiscreteSensor</span><span class="sxs-lookup"><span data-stu-id="df4d5-104">Reset method of the CIM\_DiscreteSensor class</span></span>

<span data-ttu-id="df4d5-105">La méthode **Reset** demande une réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="df4d5-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="df4d5-106">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="df4d5-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="df4d5-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="df4d5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="df4d5-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="df4d5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="df4d5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df4d5-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="df4d5-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df4d5-110">Parameters</span></span>

<span data-ttu-id="df4d5-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="df4d5-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="df4d5-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="df4d5-112">Return value</span></span>

<span data-ttu-id="df4d5-113">Retourne 0 (zéro) si la requête a été exécutée avec succès, 1 (un) si la demande n’est pas prise en charge, et une autre valeur si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="df4d5-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="df4d5-114">Notes </span><span class="sxs-lookup"><span data-stu-id="df4d5-114">Remarks</span></span>

<span data-ttu-id="df4d5-115">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="df4d5-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="df4d5-116">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="df4d5-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="df4d5-117">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="df4d5-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="df4d5-118">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="df4d5-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="df4d5-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df4d5-119">Requirements</span></span>



| <span data-ttu-id="df4d5-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df4d5-120">Requirement</span></span> | <span data-ttu-id="df4d5-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="df4d5-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df4d5-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df4d5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="df4d5-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df4d5-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df4d5-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df4d5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="df4d5-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df4d5-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df4d5-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="df4d5-126">Namespace</span></span><br/>                | <span data-ttu-id="df4d5-127">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="df4d5-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="df4d5-128">MOF</span><span class="sxs-lookup"><span data-stu-id="df4d5-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df4d5-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df4d5-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="df4d5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="df4d5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df4d5-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df4d5-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df4d5-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df4d5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df4d5-133">\_DISCRETESENSOR CIM</span><span class="sxs-lookup"><span data-stu-id="df4d5-133">CIM\_DiscreteSensor</span></span>](reset-method-in-class-cim-discretesensor.md)
</dt> <dt>

[<span data-ttu-id="df4d5-134">**\_DISCRETESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="df4d5-134">**CIM\_DiscreteSensor**</span></span>](cim-discretesensor.md)
</dt> </dl>

 

 




