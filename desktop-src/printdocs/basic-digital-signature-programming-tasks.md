---
description: Cette section décrit comment effectuer des tâches de programmation de base avec l’API de signature numérique XPS.
ms.assetid: a25a8d33-000a-4774-8beb-56d3bb39d5ae
title: Tâches courantes de programmation des signatures numériques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 346b29c7768f4c4e972284afa697f97bb1da5f69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485801"
---
# <a name="common-digital-signature-programming-tasks"></a><span data-ttu-id="1e0d6-103">Tâches courantes de programmation des signatures numériques</span><span class="sxs-lookup"><span data-stu-id="1e0d6-103">Common Digital Signature Programming Tasks</span></span>

<span data-ttu-id="1e0d6-104">Cette section décrit comment effectuer des tâches de programmation de base avec l’API de signature numérique XPS.</span><span class="sxs-lookup"><span data-stu-id="1e0d6-104">This section describes how to perform basic programming tasks with the XPS Digital Signature API.</span></span>

<span data-ttu-id="1e0d6-105">Tâches</span><span class="sxs-lookup"><span data-stu-id="1e0d6-105">Tasks</span></span>

-   [<span data-ttu-id="1e0d6-106">Initialiser le gestionnaire de signatures</span><span class="sxs-lookup"><span data-stu-id="1e0d6-106">Initialize the Signature Manager</span></span>](initialize-the-signature-manager.md)
-   [<span data-ttu-id="1e0d6-107">Signer un document</span><span class="sxs-lookup"><span data-stu-id="1e0d6-107">Sign a Document</span></span>](sign-a-document.md)
-   [<span data-ttu-id="1e0d6-108">Ajouter une demande de signature à un document XPS</span><span class="sxs-lookup"><span data-stu-id="1e0d6-108">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
-   [<span data-ttu-id="1e0d6-109">Vérifier les signatures de document</span><span class="sxs-lookup"><span data-stu-id="1e0d6-109">Verify Document Signatures</span></span>](verify-document-signatures.md)

## <a name="disclaimer"></a><span data-ttu-id="1e0d6-110">Clause d'exclusion de responsabilité</span><span class="sxs-lookup"><span data-stu-id="1e0d6-110">Disclaimer</span></span>

<span data-ttu-id="1e0d6-111">Les exemples de code ne sont pas destinés à être des programmes complets et fonctionnels.</span><span class="sxs-lookup"><span data-stu-id="1e0d6-111">Code examples are not intended to be complete and working programs.</span></span> <span data-ttu-id="1e0d6-112">Les exemples de code qui sont référencés sur cette page, par exemple, n’effectuent pas la vérification des paramètres, la vérification des erreurs, la gestion complète de la mémoire ou des ressources ou la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="1e0d6-112">The code examples that are referenced on this page, for example, do not perform parameter checking, error checking, complete memory or resource management, or error handling.</span></span> <span data-ttu-id="1e0d6-113">Utilisez ces exemples comme point de départ, puis ajoutez le code nécessaire pour créer une application fiable.</span><span class="sxs-lookup"><span data-stu-id="1e0d6-113">Use these examples as a starting point, then add the necessary code to create a robust application.</span></span> <span data-ttu-id="1e0d6-114">Pour plus d’informations sur les valeurs de retour **HRESULT** et les stratégies de gestion des erreurs, consultez [gestion des erreurs dans com](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="1e0d6-114">For more information about **HRESULT** return values and error handling strategies, see [Error Handling in COM](../com/error-handling-in-com.md).</span></span>

<span data-ttu-id="1e0d6-115">Par souci de clarté, ces exemples de code utilisent des scénarios de document et de signature XPS très simples, qui peuvent ne pas être suffisamment complexes pour répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="1e0d6-115">For clarity, these code examples use very simple XPS document and signature scenarios, which might not be sufficiently complex to meet your needs.</span></span>

 

 
