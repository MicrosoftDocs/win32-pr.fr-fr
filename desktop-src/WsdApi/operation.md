---
description: Spécifie une opération pour laquelle du code doit être généré.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: Operation, élément
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c0e4562241f5f437554d0af28dc8bca482512ea
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994315"
---
# <a name="operation-element"></a><span data-ttu-id="17f44-103">Operation, élément</span><span class="sxs-lookup"><span data-stu-id="17f44-103">operation element</span></span>

<span data-ttu-id="17f44-104">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="17f44-104">Specifies an operation for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="17f44-105">Usage</span><span class="sxs-lookup"><span data-stu-id="17f44-105">Usage</span></span>

``` syntax
<operation/>
```

## <a name="attributes"></a><span data-ttu-id="17f44-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="17f44-106">Attributes</span></span>

<span data-ttu-id="17f44-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="17f44-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="17f44-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="17f44-108">Child elements</span></span>

<span data-ttu-id="17f44-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="17f44-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="17f44-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="17f44-110">Parent elements</span></span>



| <span data-ttu-id="17f44-111">Élément</span><span class="sxs-lookup"><span data-stu-id="17f44-111">Element</span></span>                                                                                                 | <span data-ttu-id="17f44-112">Description</span><span class="sxs-lookup"><span data-stu-id="17f44-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17f44-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="17f44-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="17f44-114">Génère des déclarations d’implémentation pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="17f44-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="17f44-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="17f44-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="17f44-116">Génère des déclarations IDL pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="17f44-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="17f44-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="17f44-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="17f44-118">Génère des définitions de structure C pour les types de messages.</span><span class="sxs-lookup"><span data-stu-id="17f44-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="17f44-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="17f44-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="17f44-120">Génère des déclarations de constante C pour les tables de schéma XML pour les types de messages.</span><span class="sxs-lookup"><span data-stu-id="17f44-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="17f44-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="17f44-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="17f44-122">Génère des constantes C pour les tables de schéma XML pour les types de messages.</span><span class="sxs-lookup"><span data-stu-id="17f44-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="17f44-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="17f44-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="17f44-124">Génère des déclarations de constante C pour les types de port.</span><span class="sxs-lookup"><span data-stu-id="17f44-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="17f44-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="17f44-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="17f44-126">Génère des constantes C pour les types de ports.</span><span class="sxs-lookup"><span data-stu-id="17f44-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="17f44-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="17f44-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="17f44-128">Génère des implémentations pour les fonctions proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="17f44-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="17f44-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="17f44-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="17f44-130">Génère des déclarations pour les fonctions stub pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="17f44-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="17f44-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="17f44-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="17f44-132">Génère des implémentations pour les fonctions stub pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="17f44-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="17f44-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="17f44-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="17f44-134">Génère des déclarations d’implémentation pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.</span><span class="sxs-lookup"><span data-stu-id="17f44-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="17f44-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="17f44-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="17f44-136">Génère des déclarations IDL pour les fonctions de proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.</span><span class="sxs-lookup"><span data-stu-id="17f44-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="17f44-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="17f44-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="17f44-138">Génère des implémentations pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.</span><span class="sxs-lookup"><span data-stu-id="17f44-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="17f44-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="17f44-139">Remarks</span></span>

<span data-ttu-id="17f44-140">Il est possible de spécifier un nombre quelconque d’opérations.</span><span class="sxs-lookup"><span data-stu-id="17f44-140">Any number of operations may be specified.</span></span> <span data-ttu-id="17f44-141">Si aucune opération n’est spécifiée, du code est généré pour toutes les opérations dans tous les types de port appropriés.</span><span class="sxs-lookup"><span data-stu-id="17f44-141">If no operations are specified, code is generated for all operations in all the relevant port types.</span></span> <span data-ttu-id="17f44-142">L’utilisation de l’élément **operation** limite les méthodes générées à celles contenues dans l’opération.</span><span class="sxs-lookup"><span data-stu-id="17f44-142">Using the **operation** element will limit the methods generated to those contained in the operation.</span></span>

<span data-ttu-id="17f44-143">Par exemple, une imprimante prend en charge ces opérations entre autres :</span><span class="sxs-lookup"><span data-stu-id="17f44-143">For example, a printer supports these operations among others:</span></span>

-   <span data-ttu-id="17f44-144">**PrintJobByPost**</span><span class="sxs-lookup"><span data-stu-id="17f44-144">**PrintJobByPost**</span></span>
-   <span data-ttu-id="17f44-145">**PrintJobByReference**</span><span class="sxs-lookup"><span data-stu-id="17f44-145">**PrintJobByReference**</span></span>
-   <span data-ttu-id="17f44-146">**CancelJob**</span><span class="sxs-lookup"><span data-stu-id="17f44-146">**CancelJob**</span></span>
-   <span data-ttu-id="17f44-147">**GetJobElements**</span><span class="sxs-lookup"><span data-stu-id="17f44-147">**GetJobElements**</span></span>
-   <span data-ttu-id="17f44-148">**GetActiveJobs**</span><span class="sxs-lookup"><span data-stu-id="17f44-148">**GetActiveJobs**</span></span>
-   <span data-ttu-id="17f44-149">**GetJobHistory**</span><span class="sxs-lookup"><span data-stu-id="17f44-149">**GetJobHistory**</span></span>
-   <span data-ttu-id="17f44-150">**SubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="17f44-150">**SubscribeToPrinterConfigChange**</span></span>
-   <span data-ttu-id="17f44-151">**UnsubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="17f44-151">**UnsubscribeToPrinterConfigChange**</span></span>

<span data-ttu-id="17f44-152">Toutefois, pour inclure uniquement les méthodes liées aux opérations **PrintJobByPost** et **GetJobElements** , le script de génération de code utilisera les éléments [**idlFunctionDeclarations**](idlfunctiondeclarations.md) comme suit :</span><span class="sxs-lookup"><span data-stu-id="17f44-152">However, to include only the methods related to the **PrintJobByPost** and **GetJobElements** operations, the code generation script would use the [**idlFunctionDeclarations**](idlfunctiondeclarations.md) elements as follows:</span></span>

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

<span data-ttu-id="17f44-153">Cela génère des déclarations de fonction idl pour toutes les méthodes associées aux deux opérations (par exemple, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** et **EndGetJobElements**).</span><span class="sxs-lookup"><span data-stu-id="17f44-153">This generates idl function declarations for all methods associated with the two operations (for example, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** and **EndGetJobElements**).</span></span>

## <a name="element-information"></a><span data-ttu-id="17f44-154">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="17f44-154">Element information</span></span>



| <span data-ttu-id="17f44-155">Étiquette</span><span class="sxs-lookup"><span data-stu-id="17f44-155">Label</span></span> | <span data-ttu-id="17f44-156">Value</span><span class="sxs-lookup"><span data-stu-id="17f44-156">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="17f44-157">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17f44-157">Minimum supported system</span></span><br/> | <span data-ttu-id="17f44-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17f44-158">Windows Vista</span></span> |
| <span data-ttu-id="17f44-159">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="17f44-159">Can be empty</span></span>                        | <span data-ttu-id="17f44-160">Oui</span><span class="sxs-lookup"><span data-stu-id="17f44-160">Yes</span></span>           |



 

 




