---
description: Demande la réinitialisation de l’unité logique. Cette méthode est héritée de CIM \_ LogicalDevice.
ms.assetid: 2ad40b35-608f-4918-ac66-e3dc53ebe0bb
ms.tgt_platform: multiple
title: Méthode Reset de la classe Win32_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskPartition.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb316a72b801a696b5c5f76376036af75a8beb54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111223"
---
# <a name="reset-method-of-the-win32_diskpartition-class"></a><span data-ttu-id="d52ba-104">Méthode Reset de la \_ classe DiskPartition Win32</span><span class="sxs-lookup"><span data-stu-id="d52ba-104">Reset method of the Win32\_DiskPartition class</span></span>

<span data-ttu-id="d52ba-105">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d52ba-105">Requests a reset of the logical device.</span></span> <span data-ttu-id="d52ba-106">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d52ba-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d52ba-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d52ba-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d52ba-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d52ba-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d52ba-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d52ba-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="d52ba-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d52ba-110">Parameters</span></span>

<span data-ttu-id="d52ba-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d52ba-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d52ba-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d52ba-112">Return value</span></span>

<span data-ttu-id="d52ba-113">Retourne 0 (zéro) si la requête a été exécutée avec succès, 1 (un) si la demande n’est pas prise en charge, et une autre valeur si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d52ba-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="d52ba-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d52ba-114">Remarks</span></span>

<span data-ttu-id="d52ba-115">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="d52ba-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d52ba-116">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d52ba-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d52ba-117">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d52ba-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d52ba-118">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d52ba-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d52ba-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d52ba-119">Requirements</span></span>



| <span data-ttu-id="d52ba-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d52ba-120">Requirement</span></span> | <span data-ttu-id="d52ba-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d52ba-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d52ba-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d52ba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d52ba-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d52ba-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d52ba-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d52ba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d52ba-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d52ba-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d52ba-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d52ba-126">Namespace</span></span><br/>                | <span data-ttu-id="d52ba-127">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d52ba-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d52ba-128">MOF</span><span class="sxs-lookup"><span data-stu-id="d52ba-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d52ba-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d52ba-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d52ba-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d52ba-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d52ba-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d52ba-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d52ba-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d52ba-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d52ba-133">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="d52ba-133">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dt>

[<span data-ttu-id="d52ba-134">**\_DiskPartition Win32**</span><span class="sxs-lookup"><span data-stu-id="d52ba-134">**Win32\_DiskPartition**</span></span>](win32-diskpartition.md)
</dt> </dl>

 

 




