---
description: La méthode Reset de la classe CIM CIM \_ demande une réinitialisation de l’unité logique.
ms.assetid: 48097e0d-7986-46b9-884d-7534f3848dd7
ms.tgt_platform: multiple
title: Méthode Reset de la classe CIM_TapeDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e5fd76d038e743ba5148f4c82555d50f0a5dde5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861622"
---
# <a name="reset-method-of-the-cim_tapedrive-class"></a><span data-ttu-id="db23e-103">Méthode Reset de la classe CIM CIM \_</span><span class="sxs-lookup"><span data-stu-id="db23e-103">Reset method of the CIM\_TapeDrive class</span></span>

<span data-ttu-id="db23e-104">La méthode **Reset** de la classe CIM CIM \_ demande une réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="db23e-104">The **Reset** method of the CIM\_TapeDrive class requests a reset of the logical device.</span></span> <span data-ttu-id="db23e-105">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db23e-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="db23e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db23e-106">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="db23e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db23e-107">Parameters</span></span>

<span data-ttu-id="db23e-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="db23e-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db23e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db23e-109">Return value</span></span>

<span data-ttu-id="db23e-110">Retourne 0 (zéro) si la requête a été exécutée avec succès, 1 (un) si la demande n’est pas prise en charge, et une autre valeur si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="db23e-110">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="db23e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="db23e-111">Remarks</span></span>

<span data-ttu-id="db23e-112">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="db23e-112">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="db23e-113">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="db23e-113">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="db23e-114">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="db23e-114">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="db23e-115">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="db23e-115">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="db23e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db23e-116">Requirements</span></span>



| <span data-ttu-id="db23e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db23e-117">Requirement</span></span> | <span data-ttu-id="db23e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="db23e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db23e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db23e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="db23e-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db23e-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="db23e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db23e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="db23e-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db23e-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="db23e-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="db23e-123">Namespace</span></span><br/>                | <span data-ttu-id="db23e-124">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="db23e-124">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="db23e-125">MOF</span><span class="sxs-lookup"><span data-stu-id="db23e-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db23e-126"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db23e-126"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="db23e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="db23e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db23e-128"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db23e-128"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db23e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db23e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db23e-130">CIM \_ CIM</span><span class="sxs-lookup"><span data-stu-id="db23e-130">CIM\_TapeDrive</span></span>](reset-method-in-class-cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="db23e-131">**CIM \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="db23e-131">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> </dl>

 

 




