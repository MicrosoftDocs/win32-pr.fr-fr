---
description: Lorsque vous utilisez des fournisseurs de services de chiffrement, gardez à l’esprit les conventions suivantes.
ms.assetid: 70053b89-4d39-4a86-985a-0e8f05fbc9c0
title: 'Utilisation des fournisseurs de services de chiffrement : processus généraux'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f067ef0e3cd837b1b347daac3e3da21543047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516063"
---
# <a name="using-csps-general-processes"></a><span data-ttu-id="790ed-103">Utilisation des fournisseurs de services de chiffrement : processus généraux</span><span class="sxs-lookup"><span data-stu-id="790ed-103">Using CSPs: General Processes</span></span>

<span data-ttu-id="790ed-104">Lorsque vous utilisez des [*fournisseurs de services de chiffrement*](../secgloss/c-gly.md) , gardez à l’esprit les conventions suivantes.</span><span class="sxs-lookup"><span data-stu-id="790ed-104">When using [*cryptographic service providers*](../secgloss/c-gly.md) CSPs, keep the following conventions in mind.</span></span>

## <a name="private-key-caching"></a><span data-ttu-id="790ed-105">Mise en cache des clés privées</span><span class="sxs-lookup"><span data-stu-id="790ed-105">Private Key Caching</span></span>

<span data-ttu-id="790ed-106">Un CSP peut mettre en cache certaines [*clés privées*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="790ed-106">A CSP can cache some [*private keys*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="790ed-107">Il est possible de contrôler cette mise en cache de clé privée sur une base globale, mais pas propre à l’application.</span><span class="sxs-lookup"><span data-stu-id="790ed-107">It is possible to control this private key caching on a global, but not an application-specific, basis.</span></span> <span data-ttu-id="790ed-108">La mise en cache des modifications s’effectue en modifiant certains paramètres du Registre.</span><span class="sxs-lookup"><span data-stu-id="790ed-108">Caching changes are made by modifying certain registry settings.</span></span> <span data-ttu-id="790ed-109">Pour plus d’informations, consultez [**constantes de mise en cache de clés privées**](private-key-caching-constants.md).</span><span class="sxs-lookup"><span data-stu-id="790ed-109">For more information, see [**Private Key Caching Constants**](private-key-caching-constants.md).</span></span>

## <a name="example-code-conventions"></a><span data-ttu-id="790ed-110">Exemples de conventions de code</span><span class="sxs-lookup"><span data-stu-id="790ed-110">Example Code Conventions</span></span>

<span data-ttu-id="790ed-111">Pour fournir un code plus concis et plus lisible, certains principes de bonnes pratiques de programmation ne sont pas toujours suivis dans les exemples.</span><span class="sxs-lookup"><span data-stu-id="790ed-111">To provide more concise, more readable code, some principles of good programming practice are not always followed in the examples.</span></span> <span data-ttu-id="790ed-112">En particulier :</span><span class="sxs-lookup"><span data-stu-id="790ed-112">In particular:</span></span>

-   <span data-ttu-id="790ed-113">Seules les réponses d’erreur limitées sont affichées.</span><span class="sxs-lookup"><span data-stu-id="790ed-113">Only limited error responses are shown.</span></span> <span data-ttu-id="790ed-114">Les programmes correctement écrits et complets vérifient les codes d’erreur renvoyés et effectuent les actions appropriées lorsqu’une erreur est rencontrée.</span><span class="sxs-lookup"><span data-stu-id="790ed-114">Well-written, complete programs check returned error codes and perform appropriate actions when an error is encountered.</span></span>
-   <span data-ttu-id="790ed-115">Seule la gestion de la mémoire et des ressources est limitée.</span><span class="sxs-lookup"><span data-stu-id="790ed-115">Only limited memory and resource management is done.</span></span> <span data-ttu-id="790ed-116">Les programmes bien écrits et complets détruisent l’ensemble des clés et des [*hachages*](../secgloss/h-gly.md), libèrent toute la mémoire allouée, ferment tous les fichiers et libèrent tous les descripteurs.</span><span class="sxs-lookup"><span data-stu-id="790ed-116">Well-written, complete programs destroy all keys and [*hashes*](../secgloss/h-gly.md), free all allocated memory, close all files, and release all handles.</span></span> <span data-ttu-id="790ed-117">Ces exemples fournissent uniquement des démonstrations limitées de l’utilisation des fonctions qui effectuent ces tâches.</span><span class="sxs-lookup"><span data-stu-id="790ed-117">These examples provide only limited demonstrations of the use of functions that perform these tasks.</span></span> <span data-ttu-id="790ed-118">Ces exemples n’effectuent aucune tâche de gestion de la mémoire ou des ressources en cas d’arrêt du programme en raison d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="790ed-118">These examples perform no memory or resource management tasks in the case of program termination due to errors.</span></span>

<span data-ttu-id="790ed-119">Les rubriques suivantes présentent des informations générales sur les exemples de procédures, ainsi que des exemples de code.</span><span class="sxs-lookup"><span data-stu-id="790ed-119">The following topics present general information about procedure examples as well as sample code.</span></span>

-   [<span data-ttu-id="790ed-120">Récupération de données de longueur inconnue</span><span class="sxs-lookup"><span data-stu-id="790ed-120">Retrieving Data of Unknown Length</span></span>](retrieving-data-of-unknown-length.md)
-   [<span data-ttu-id="790ed-121">Énumération des protocoles pris en charge</span><span class="sxs-lookup"><span data-stu-id="790ed-121">Enumerating Supported Protocols</span></span>](enumerating-supported-protocols.md)

 

 
