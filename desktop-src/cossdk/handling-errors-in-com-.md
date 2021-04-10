---
description: La partie la plus problématique de l’écriture des composants est le traitement des erreurs possibles.
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: Gestion des erreurs dans COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1979fc49ff8f14bb83b194be7e1787feaf7d86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111678"
---
# <a name="handling-errors-in-com"></a><span data-ttu-id="91f03-103">Gestion des erreurs dans COM+</span><span class="sxs-lookup"><span data-stu-id="91f03-103">Handling Errors in COM+</span></span>

<span data-ttu-id="91f03-104">La partie la plus problématique de l’écriture des composants est le traitement des erreurs possibles.</span><span class="sxs-lookup"><span data-stu-id="91f03-104">The most problematic part of writing components is dealing with possible errors.</span></span> <span data-ttu-id="91f03-105">Essayer de déterminer ce qui peut être incorrect et ce qu’il convient de faire peut être difficile dans les meilleures conditions.</span><span class="sxs-lookup"><span data-stu-id="91f03-105">Trying to determine what can go wrong and what to do about it can be challenging under the best conditions.</span></span> <span data-ttu-id="91f03-106">Les erreurs courantes que votre composant peut vérifier et gérer sont les échecs de connexion réseau, les erreurs de sécurité et les échecs associés à des objets inaccessibles.</span><span class="sxs-lookup"><span data-stu-id="91f03-106">Common errors that your component might check for and handle are failed network connections, security errors, and failures associated with unreachable objects.</span></span>

<span data-ttu-id="91f03-107">En outre, vous pouvez développer vos propres codes d’erreur pour signaler des erreurs spécifiques à l’interface, par exemple lorsqu’une règle d’entreprise a été violée.</span><span class="sxs-lookup"><span data-stu-id="91f03-107">Additionally, you can develop your own error codes to report interface-specific errors such as when a business rule has been violated.</span></span>

<span data-ttu-id="91f03-108">Dans le cadre du modèle de programmation COM+, un objet peut (et souvent) appeler des méthodes d’interface sur d’autres objets pour effectuer le travail.</span><span class="sxs-lookup"><span data-stu-id="91f03-108">In keeping with the COM+ programming model, an object can (and often does) call interface methods on other objects to perform work.</span></span> <span data-ttu-id="91f03-109">Étant donné que les programmeurs peuvent écrire des composants dans différents langages de programmation, COM+ exige que tous les mécanismes de gestion des erreurs soient indépendants du langage, par exemple : les collections HRESULT et [**errorInfo**](errorinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="91f03-109">Because programmers can write components in different programming languages, COM+ requires that all error-handling mechanisms be language-neutral, for example: HRESULTs and [**ErrorInfo**](errorinfo.md) collections.</span></span>

<span data-ttu-id="91f03-110">Cette section comprend des rubriques, décrites dans le tableau suivant, qui traitent des techniques de gestion des erreurs dans les applications COM+, des fonctionnalités de COM+ qui affectent le comportement d’échec et des suggestions pour le diagnostic des erreurs COM+.</span><span class="sxs-lookup"><span data-stu-id="91f03-110">This section includes topics, described in the following table, that discuss techniques for handling errors in COM+ applications, features in COM+ that affect failure behavior, and suggestions for diagnosing COM+ errors.</span></span>



| <span data-ttu-id="91f03-111">Rubrique</span><span class="sxs-lookup"><span data-stu-id="91f03-111">Topic</span></span>                                                                                           | <span data-ttu-id="91f03-112">Description</span><span class="sxs-lookup"><span data-stu-id="91f03-112">Description</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91f03-113">Stratégies de gestion des erreurs dans COM+</span><span class="sxs-lookup"><span data-stu-id="91f03-113">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)<br/> | <span data-ttu-id="91f03-114">Répertorie et décrit les recommandations de base pour la gestion des erreurs dans COM+, y compris quand utiliser les collections HRESULTs et [**errorInfo**](errorinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="91f03-114">Lists and describes basic guidelines for handling errors in COM+, including when to use HRESULTs and [**ErrorInfo**](errorinfo.md) collections.</span></span><br/> |
| [<span data-ttu-id="91f03-115">Modification des valeurs de retour par COM+</span><span class="sxs-lookup"><span data-stu-id="91f03-115">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)<br/>               | <span data-ttu-id="91f03-116">Identifie la condition unique dans laquelle COM+ convertit un HRESULT standard en code d’erreur COM+ avant de le renvoyer à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="91f03-116">Identifies the single condition in which COM+ converts a standard HRESULT to a COM+ error code before passing it back to the caller.</span></span><br/>             |
| [<span data-ttu-id="91f03-117">Isolation des erreurs et stratégie FailFast</span><span class="sxs-lookup"><span data-stu-id="91f03-117">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)<br/>       | <span data-ttu-id="91f03-118">Montre comment l’isolation des erreurs et la stratégie FailFast affectent le comportement de COM+.</span><span class="sxs-lookup"><span data-stu-id="91f03-118">Shows how fault isolation and the failfast policy affect COM+ behavior.</span></span><br/>                                                                          |
| [<span data-ttu-id="91f03-119">Recherche de la source d’une erreur</span><span class="sxs-lookup"><span data-stu-id="91f03-119">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)<br/>                 | <span data-ttu-id="91f03-120">Décrit comment vous pouvez diagnostiquer la source et obtenir une description des erreurs d’application.</span><span class="sxs-lookup"><span data-stu-id="91f03-120">Describes how you can diagnose the source and obtain a description of application errors.</span></span> <br/>                                                       |
| [<span data-ttu-id="91f03-121">Interprétation des codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="91f03-121">Interpreting Error Codes</span></span>](interpreting-error-codes.md)<br/>                             | <span data-ttu-id="91f03-122">Identifie le mécanisme de gestion des erreurs prédominant pour Microsoft Visual C++, le langage Java et Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="91f03-122">Identifies the predominant error-handling mechanism for Microsoft Visual C++, the Java language, and Microsoft Visual Basic.</span></span> <br/>                    |
| [<span data-ttu-id="91f03-123">Dépannage</span><span class="sxs-lookup"><span data-stu-id="91f03-123">Troubleshooting</span></span>](troubleshooting.md)<br/>                                               | <span data-ttu-id="91f03-124">Fournit une assistance supplémentaire pour diagnostiquer les erreurs.</span><span class="sxs-lookup"><span data-stu-id="91f03-124">Provides additional assistance in diagnosing errors.</span></span><br/>                                                                                             |
| [<span data-ttu-id="91f03-125">Contacter le support technique</span><span class="sxs-lookup"><span data-stu-id="91f03-125">Contacting Support</span></span>](contacting-support.md)<br/>                                         | <span data-ttu-id="91f03-126">Identifie les informations importantes de résolution des problèmes que vous devez fournir lorsque vous contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="91f03-126">Identifies important problem-solving information you should provide when contacting support.</span></span><br/>                                                     |



 

<span data-ttu-id="91f03-127">Pour plus d’informations sur la gestion des erreurs associées à différents services COM+, consultez les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="91f03-127">For detailed information on handling errors associated with various COM+ services, see the following sections:</span></span>

-   [<span data-ttu-id="91f03-128">Accélération des transactions en avertissant l’objet racine</span><span class="sxs-lookup"><span data-stu-id="91f03-128">Speeding Transactions by Notifying the Root Object</span></span>](speeding-transactions-by-notifying-the-root-object.md)
-   <span data-ttu-id="91f03-129">[Gestion des erreurs](handling-errors-in-queued-components.md) (pour les composants en file d’attente)</span><span class="sxs-lookup"><span data-stu-id="91f03-129">[Handling Errors](handling-errors-in-queued-components.md) (for queued components)</span></span>

## <a name="related-topics"></a><span data-ttu-id="91f03-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="91f03-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91f03-131">Débogage des applications COM+</span><span class="sxs-lookup"><span data-stu-id="91f03-131">Debugging COM+ Applications</span></span>](debugging-com--applications.md)
</dt> </dl>

 

 




