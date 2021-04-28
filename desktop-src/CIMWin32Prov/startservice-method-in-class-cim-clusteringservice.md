---
description: Méthode StartService de la classe CIM_ClusteringService-la méthode StartService met le service dans un état Démarré.
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
ms.openlocfilehash: dcd18af37da9302256776cfee844fd83f989c9b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086187"
---
# <a name="startservice-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="fff48-103">Méthode StartService de la \_ classe CIM ClusteringService</span><span class="sxs-lookup"><span data-stu-id="fff48-103">StartService method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="fff48-104">La méthode **StartService** met le service dans un état Démarré.</span><span class="sxs-lookup"><span data-stu-id="fff48-104">The **StartService** method puts the service in a started state.</span></span> <span data-ttu-id="fff48-105">Dans une sous-classe, l’ensemble des codes de retour possibles peut être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="fff48-105">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="fff48-106">Les chaînes dans lesquelles le contenu **ValueMap** est traduit peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="fff48-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="fff48-107">Cette méthode est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="fff48-107">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fff48-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="fff48-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fff48-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fff48-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fff48-110">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="fff48-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fff48-111">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fff48-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fff48-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fff48-112">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="fff48-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fff48-113">Parameters</span></span>

<span data-ttu-id="fff48-114">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="fff48-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fff48-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fff48-115">Return value</span></span>

<span data-ttu-id="fff48-116">Retourne la valeur 0 (zéro) si le service a été démarré avec succès, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="fff48-116">Returns a value of 0 (zero) if the service was successfully started, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="fff48-117">Notes </span><span class="sxs-lookup"><span data-stu-id="fff48-117">Remarks</span></span>

<span data-ttu-id="fff48-118">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="fff48-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="fff48-119">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="fff48-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="fff48-120">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="fff48-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fff48-121">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="fff48-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fff48-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fff48-122">Requirements</span></span>



| <span data-ttu-id="fff48-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fff48-123">Requirement</span></span> | <span data-ttu-id="fff48-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="fff48-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fff48-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fff48-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fff48-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fff48-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fff48-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fff48-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fff48-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fff48-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fff48-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fff48-129">Namespace</span></span><br/>                | <span data-ttu-id="fff48-130">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="fff48-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fff48-131">MOF</span><span class="sxs-lookup"><span data-stu-id="fff48-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fff48-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fff48-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fff48-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fff48-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fff48-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fff48-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fff48-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fff48-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fff48-136">\_CLUSTERINGSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="fff48-136">CIM\_ClusteringService</span></span>](startservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="fff48-137">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fff48-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

