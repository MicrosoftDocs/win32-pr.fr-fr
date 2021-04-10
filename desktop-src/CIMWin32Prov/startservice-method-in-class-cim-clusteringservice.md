---
description: La méthode StartService met le service dans un état Démarré.
ms.assetid: 2efd2a06-a03c-4f4c-b2fa-889f84faac0f
ms.tgt_platform: multiple
title: Méthode StartService de la classe CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8abdeffa234461952f99013524042dcbba6e682
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201004"
---
# <a name="startservice-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="e937c-103">Méthode StartService de la \_ classe CIM ClusteringService</span><span class="sxs-lookup"><span data-stu-id="e937c-103">StartService method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="e937c-104">La méthode **StartService** met le service dans un état Démarré.</span><span class="sxs-lookup"><span data-stu-id="e937c-104">The **StartService** method puts the service in a started state.</span></span> <span data-ttu-id="e937c-105">Dans une sous-classe, l’ensemble des codes de retour possibles peut être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="e937c-105">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="e937c-106">Les chaînes dans lesquelles le contenu **ValueMap** est traduit peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="e937c-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="e937c-107">Cette méthode est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="e937c-107">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e937c-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e937c-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e937c-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e937c-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e937c-110">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="e937c-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e937c-111">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e937c-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e937c-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e937c-112">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="e937c-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e937c-113">Parameters</span></span>

<span data-ttu-id="e937c-114">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e937c-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e937c-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e937c-115">Return value</span></span>

<span data-ttu-id="e937c-116">Retourne la valeur 0 (zéro) si le service a été démarré avec succès, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="e937c-116">Returns a value of 0 (zero) if the service was successfully started, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e937c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e937c-117">Remarks</span></span>

<span data-ttu-id="e937c-118">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="e937c-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e937c-119">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e937c-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="e937c-120">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="e937c-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e937c-121">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e937c-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e937c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e937c-122">Requirements</span></span>



| <span data-ttu-id="e937c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e937c-123">Requirement</span></span> | <span data-ttu-id="e937c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e937c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e937c-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e937c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e937c-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e937c-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e937c-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e937c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e937c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e937c-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e937c-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e937c-129">Namespace</span></span><br/>                | <span data-ttu-id="e937c-130">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e937c-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e937c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e937c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e937c-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e937c-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e937c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e937c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e937c-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e937c-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e937c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e937c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e937c-136">\_CLUSTERINGSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="e937c-136">CIM\_ClusteringService</span></span>](startservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="e937c-137">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e937c-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

