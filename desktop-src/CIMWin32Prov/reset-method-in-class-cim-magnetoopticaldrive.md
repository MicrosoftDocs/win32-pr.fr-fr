---
description: La méthode Reset de la \_ classe CIM MagnetoOpticalDrive demande une réinitialisation de l’unité logique.
ms.assetid: a2a9d58a-2c20-4edc-8700-eebc7e5826f9
ms.tgt_platform: multiple
title: Méthode Reset de la classe CIM_MagnetoOpticalDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MagnetoOpticalDrive.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 81d9830ddf684699d7339bbd436f87a3b6dd91b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950643"
---
# <a name="reset-method-of-the-cim_magnetoopticaldrive-class"></a><span data-ttu-id="36d74-103">Méthode Reset de la \_ classe CIM MagnetoOpticalDrive</span><span class="sxs-lookup"><span data-stu-id="36d74-103">Reset method of the CIM\_MagnetoOpticalDrive class</span></span>

<span data-ttu-id="36d74-104">La méthode **Reset** de la \_ classe CIM MagnetoOpticalDrive demande une réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="36d74-104">The **Reset** method of the CIM\_MagnetoOpticalDrive class requests a reset of the logical device.</span></span> <span data-ttu-id="36d74-105">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="36d74-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36d74-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="36d74-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="36d74-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="36d74-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="36d74-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36d74-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="36d74-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36d74-109">Parameters</span></span>

<span data-ttu-id="36d74-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="36d74-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="36d74-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36d74-111">Return value</span></span>

<span data-ttu-id="36d74-112">Retourne 0 (zéro) si la requête a été exécutée avec succès, 1 (un) si la demande n’est pas prise en charge, et une autre valeur si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="36d74-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="36d74-113">Notes</span><span class="sxs-lookup"><span data-stu-id="36d74-113">Remarks</span></span>

<span data-ttu-id="36d74-114">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="36d74-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="36d74-115">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="36d74-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="36d74-116">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="36d74-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="36d74-117">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="36d74-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="36d74-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36d74-118">Requirements</span></span>



| <span data-ttu-id="36d74-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36d74-119">Requirement</span></span> | <span data-ttu-id="36d74-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="36d74-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36d74-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36d74-121">Minimum supported client</span></span><br/> | <span data-ttu-id="36d74-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36d74-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="36d74-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36d74-123">Minimum supported server</span></span><br/> | <span data-ttu-id="36d74-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36d74-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="36d74-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="36d74-125">Namespace</span></span><br/>                | <span data-ttu-id="36d74-126">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="36d74-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="36d74-127">MOF</span><span class="sxs-lookup"><span data-stu-id="36d74-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36d74-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36d74-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="36d74-129">DLL</span><span class="sxs-lookup"><span data-stu-id="36d74-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36d74-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36d74-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36d74-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36d74-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d74-132">\_MAGNETOOPTICALDRIVE CIM</span><span class="sxs-lookup"><span data-stu-id="36d74-132">CIM\_MagnetoOpticalDrive</span></span>](reset-method-in-class-cim-magnetoopticaldrive.md)
</dt> <dt>

[<span data-ttu-id="36d74-133">**\_MAGNETOOPTICALDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="36d74-133">**CIM\_MagnetoOpticalDrive**</span></span>](cim-magnetoopticaldrive.md)
</dt> </dl>

 

 




