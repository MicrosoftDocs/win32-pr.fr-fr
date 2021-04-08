---
description: La méthode Reset de la \_ classe CIM MediaAccessDevice demande une réinitialisation de l’unité logique.
ms.assetid: 89796284-3569-4ff0-873d-0c5ed58eaedc
ms.tgt_platform: multiple
title: Méthode Reset de la classe CIM_MediaAccessDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90dd391a32d36ea17bfbb20edd4e6394a85f38dd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953467"
---
# <a name="reset-method-of-the-cim_mediaaccessdevice-class"></a><span data-ttu-id="e71d3-103">Méthode Reset de la \_ classe CIM MediaAccessDevice</span><span class="sxs-lookup"><span data-stu-id="e71d3-103">Reset method of the CIM\_MediaAccessDevice class</span></span>

<span data-ttu-id="e71d3-104">La méthode **Reset** de la \_ classe CIM MediaAccessDevice demande une réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="e71d3-104">The **Reset** method of the CIM\_MediaAccessDevice class requests a reset of the logical device.</span></span> <span data-ttu-id="e71d3-105">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e71d3-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e71d3-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e71d3-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e71d3-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e71d3-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e71d3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e71d3-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="e71d3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e71d3-109">Parameters</span></span>

<span data-ttu-id="e71d3-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e71d3-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e71d3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e71d3-111">Return value</span></span>

<span data-ttu-id="e71d3-112">Retourne 0 (zéro) si la requête a été exécutée avec succès, 1 (un) si la demande n’est pas prise en charge, et une autre valeur si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e71d3-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="e71d3-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e71d3-113">Remarks</span></span>

<span data-ttu-id="e71d3-114">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="e71d3-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e71d3-115">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e71d3-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="e71d3-116">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="e71d3-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e71d3-117">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e71d3-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e71d3-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e71d3-118">Requirements</span></span>



| <span data-ttu-id="e71d3-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e71d3-119">Requirement</span></span> | <span data-ttu-id="e71d3-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e71d3-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e71d3-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e71d3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e71d3-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e71d3-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e71d3-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e71d3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e71d3-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e71d3-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e71d3-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e71d3-125">Namespace</span></span><br/>                | <span data-ttu-id="e71d3-126">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e71d3-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e71d3-127">MOF</span><span class="sxs-lookup"><span data-stu-id="e71d3-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e71d3-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e71d3-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e71d3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e71d3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e71d3-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e71d3-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e71d3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e71d3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e71d3-132">\_MEDIAACCESSDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="e71d3-132">CIM\_MediaAccessDevice</span></span>](reset-method-in-class-cim-mediaaccessdevice.md)
</dt> <dt>

[<span data-ttu-id="e71d3-133">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e71d3-133">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

 




