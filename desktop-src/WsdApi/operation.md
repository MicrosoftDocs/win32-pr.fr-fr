---
description: Spécifie une opération pour laquelle du code doit être généré.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: Operation, élément
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdd8324553e046000f467c103afd6ac0464cbc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034302"
---
# <a name="operation-element"></a><span data-ttu-id="b5d7f-103">Operation, élément</span><span class="sxs-lookup"><span data-stu-id="b5d7f-103">operation element</span></span>

<span data-ttu-id="b5d7f-104">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-104">Specifies an operation for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="b5d7f-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="b5d7f-105">Usage</span></span>

``` syntax
<operation/>
```

## <a name="attributes"></a><span data-ttu-id="b5d7f-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="b5d7f-106">Attributes</span></span>

<span data-ttu-id="b5d7f-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b5d7f-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b5d7f-108">Child elements</span></span>

<span data-ttu-id="b5d7f-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b5d7f-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b5d7f-110">Parent elements</span></span>



| <span data-ttu-id="b5d7f-111">Élément</span><span class="sxs-lookup"><span data-stu-id="b5d7f-111">Element</span></span>                                                                                                 | <span data-ttu-id="b5d7f-112">Description</span><span class="sxs-lookup"><span data-stu-id="b5d7f-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5d7f-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="b5d7f-114">Génère des déclarations d’implémentation pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="b5d7f-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="b5d7f-116">Génère des déclarations IDL pour les fonctions de proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="b5d7f-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="b5d7f-118">Génère des définitions de structure C pour les types de messages.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="b5d7f-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="b5d7f-120">Génère des déclarations de constante C pour les tables de schéma XML pour les types de messages.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="b5d7f-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="b5d7f-122">Génère des constantes C pour les tables de schéma XML pour les types de messages.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="b5d7f-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="b5d7f-124">Génère des déclarations de constante C pour les types de port.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="b5d7f-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="b5d7f-126">Génère des constantes C pour les types de ports.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="b5d7f-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="b5d7f-128">Génère des implémentations pour les fonctions proxy pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="b5d7f-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="b5d7f-130">Génère des déclarations pour les fonctions stub pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="b5d7f-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="b5d7f-132">Génère des implémentations pour les fonctions stub pour les opérations de type de port.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="b5d7f-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="b5d7f-134">Génère des déclarations d’implémentation pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="b5d7f-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="b5d7f-136">Génère des déclarations IDL pour les fonctions de proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="b5d7f-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="b5d7f-138">Génère des implémentations pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="b5d7f-139">Notes</span><span class="sxs-lookup"><span data-stu-id="b5d7f-139">Remarks</span></span>

<span data-ttu-id="b5d7f-140">Il est possible de spécifier un nombre quelconque d’opérations.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-140">Any number of operations may be specified.</span></span> <span data-ttu-id="b5d7f-141">Si aucune opération n’est spécifiée, du code est généré pour toutes les opérations dans tous les types de port appropriés.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-141">If no operations are specified, code is generated for all operations in all the relevant port types.</span></span> <span data-ttu-id="b5d7f-142">L’utilisation de l’élément **operation** limite les méthodes générées à celles contenues dans l’opération.</span><span class="sxs-lookup"><span data-stu-id="b5d7f-142">Using the **operation** element will limit the methods generated to those contained in the operation.</span></span>

<span data-ttu-id="b5d7f-143">Par exemple, une imprimante prend en charge ces opérations entre autres :</span><span class="sxs-lookup"><span data-stu-id="b5d7f-143">For example, a printer supports these operations among others:</span></span>

-   <span data-ttu-id="b5d7f-144">**PrintJobByPost**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-144">**PrintJobByPost**</span></span>
-   <span data-ttu-id="b5d7f-145">**PrintJobByReference**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-145">**PrintJobByReference**</span></span>
-   <span data-ttu-id="b5d7f-146">**CancelJob**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-146">**CancelJob**</span></span>
-   <span data-ttu-id="b5d7f-147">**GetJobElements**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-147">**GetJobElements**</span></span>
-   <span data-ttu-id="b5d7f-148">**GetActiveJobs**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-148">**GetActiveJobs**</span></span>
-   <span data-ttu-id="b5d7f-149">**GetJobHistory**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-149">**GetJobHistory**</span></span>
-   <span data-ttu-id="b5d7f-150">**SubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-150">**SubscribeToPrinterConfigChange**</span></span>
-   <span data-ttu-id="b5d7f-151">**UnsubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="b5d7f-151">**UnsubscribeToPrinterConfigChange**</span></span>

<span data-ttu-id="b5d7f-152">Toutefois, pour inclure uniquement les méthodes liées aux opérations **PrintJobByPost** et **GetJobElements** , le script de génération de code utilisera les éléments [**idlFunctionDeclarations**](idlfunctiondeclarations.md) comme suit :</span><span class="sxs-lookup"><span data-stu-id="b5d7f-152">However, to include only the methods related to the **PrintJobByPost** and **GetJobElements** operations, the code generation script would use the [**idlFunctionDeclarations**](idlfunctiondeclarations.md) elements as follows:</span></span>

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

<span data-ttu-id="b5d7f-153">Cela génère des déclarations de fonction idl pour toutes les méthodes associées aux deux opérations (par exemple, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** et **EndGetJobElements**).</span><span class="sxs-lookup"><span data-stu-id="b5d7f-153">This generates idl function declarations for all methods associated with the two operations (for example, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** and **EndGetJobElements**).</span></span>

## <a name="element-information"></a><span data-ttu-id="b5d7f-154">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b5d7f-154">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b5d7f-155">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5d7f-155">Minimum supported system</span></span><br/> | <span data-ttu-id="b5d7f-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5d7f-156">Windows Vista</span></span> |
| <span data-ttu-id="b5d7f-157">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="b5d7f-157">Can be empty</span></span>                        | <span data-ttu-id="b5d7f-158">Oui</span><span class="sxs-lookup"><span data-stu-id="b5d7f-158">Yes</span></span>           |



 

 




