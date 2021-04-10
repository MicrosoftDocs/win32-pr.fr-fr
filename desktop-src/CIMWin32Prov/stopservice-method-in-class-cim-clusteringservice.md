---
description: Arrête le service représenté par l’objet dérivé de CIM \_ ClusteringService.
ms.assetid: b8dbaeeb-819b-469b-9f5e-d658e88d1a6e
ms.tgt_platform: multiple
title: Méthode StopService de la classe CIM_ClusteringService (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3a55f7b0a9527092e51156d55c7513ee59c4861
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861189"
---
# <a name="stopservice-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="3b12b-103">Méthode StopService de la \_ classe CIM ClusteringService</span><span class="sxs-lookup"><span data-stu-id="3b12b-103">StopService method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="3b12b-104">La méthode **StopService** arrête le service représenté par l’objet dérivé de [**CIM \_ ClusteringService**](cim-clusteringservice.md).</span><span class="sxs-lookup"><span data-stu-id="3b12b-104">The **StopService** method stops the service represented by the object derived from [**CIM\_ClusteringService**](cim-clusteringservice.md).</span></span> <span data-ttu-id="3b12b-105">Cette méthode est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="3b12b-105">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b12b-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="3b12b-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3b12b-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3b12b-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3b12b-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3b12b-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3b12b-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3b12b-109">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b12b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b12b-110">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="3b12b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b12b-111">Parameters</span></span>

<span data-ttu-id="3b12b-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3b12b-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3b12b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b12b-113">Return value</span></span>

<span data-ttu-id="3b12b-114">Retourne la valeur 0 (zéro) si le service a été arrêté avec succès, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="3b12b-114">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b12b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3b12b-115">Remarks</span></span>

<span data-ttu-id="3b12b-116">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="3b12b-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3b12b-117">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3b12b-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3b12b-118">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="3b12b-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3b12b-119">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="3b12b-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b12b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b12b-120">Requirements</span></span>



| <span data-ttu-id="3b12b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b12b-121">Requirement</span></span> | <span data-ttu-id="3b12b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b12b-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b12b-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b12b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3b12b-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b12b-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b12b-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b12b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3b12b-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b12b-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b12b-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3b12b-127">Namespace</span></span><br/>                | <span data-ttu-id="3b12b-128">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3b12b-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3b12b-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b12b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b12b-130"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b12b-130"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="3b12b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3b12b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b12b-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b12b-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b12b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3b12b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b12b-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b12b-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b12b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b12b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b12b-136">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3b12b-136">**CIM\_ClusteringService**</span></span>](stopservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="3b12b-137">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3b12b-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

