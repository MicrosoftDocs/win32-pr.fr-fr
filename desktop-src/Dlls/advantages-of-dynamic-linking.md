---
description: La liaison dynamique présente les avantages suivants par rapport à la liaison statique.
ms.assetid: adfd941d-1a36-4dd8-af1f-b105466e0668
title: Avantages de la liaison dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1764e25a051522600bd6b485b75f414f8a280e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519942"
---
# <a name="advantages-of-dynamic-linking"></a><span data-ttu-id="6ce07-103">Avantages de la liaison dynamique</span><span class="sxs-lookup"><span data-stu-id="6ce07-103">Advantages of Dynamic Linking</span></span>

<span data-ttu-id="6ce07-104">La liaison dynamique présente les avantages suivants par rapport à la liaison statique :</span><span class="sxs-lookup"><span data-stu-id="6ce07-104">Dynamic linking has the following advantages over static linking:</span></span>

-   <span data-ttu-id="6ce07-105">Plusieurs processus qui chargent la même DLL à la même adresse de base partagent une seule copie de la DLL dans la mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="6ce07-105">Multiple processes that load the same DLL at the same base address share a single copy of the DLL in physical memory.</span></span> <span data-ttu-id="6ce07-106">Cela permet d’économiser la mémoire système et de réduire l’échange.</span><span class="sxs-lookup"><span data-stu-id="6ce07-106">Doing this saves system memory and reduces swapping.</span></span>
-   <span data-ttu-id="6ce07-107">Lorsque les fonctions d’une DLL changent, les applications qui les utilisent n’ont pas besoin d’être recompilées ou reliées tant que les arguments de fonction, les conventions d’appel et les valeurs de retour ne sont pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="6ce07-107">When the functions in a DLL change, the applications that use them do not need to be recompiled or relinked as long as the function arguments, calling conventions, and return values do not change.</span></span> <span data-ttu-id="6ce07-108">En revanche, le code objet lié statiquement exige que l’application soit reliée lorsque les fonctions changent.</span><span class="sxs-lookup"><span data-stu-id="6ce07-108">In contrast, statically linked object code requires that the application be relinked when the functions change.</span></span>
-   <span data-ttu-id="6ce07-109">Une DLL peut fournir un support après le marché.</span><span class="sxs-lookup"><span data-stu-id="6ce07-109">A DLL can provide after-market support.</span></span> <span data-ttu-id="6ce07-110">Par exemple, une DLL de pilote d’affichage peut être modifiée pour prendre en charge un affichage qui n’était pas disponible lors de la livraison initiale de l’application.</span><span class="sxs-lookup"><span data-stu-id="6ce07-110">For example, a display driver DLL can be modified to support a display that was not available when the application was initially shipped.</span></span>
-   <span data-ttu-id="6ce07-111">Les programmes écrits dans différents langages de programmation peuvent appeler la même fonction DLL tant que les programmes suivent la même convention d’appel que celle utilisée par la fonction.</span><span class="sxs-lookup"><span data-stu-id="6ce07-111">Programs written in different programming languages can call the same DLL function as long as the programs follow the same calling convention that the function uses.</span></span> <span data-ttu-id="6ce07-112">La Convention d’appel (par exemple, C, Pascal ou appel standard) contrôle l’ordre dans lequel la fonction appelante doit envoyer les arguments sur la pile, si la fonction ou la fonction appelante est responsable du nettoyage de la pile et si des arguments sont passés dans les registres.</span><span class="sxs-lookup"><span data-stu-id="6ce07-112">The calling convention (such as C, Pascal, or standard call) controls the order in which the calling function must push the arguments onto the stack, whether the function or the calling function is responsible for cleaning up the stack, and whether any arguments are passed in registers.</span></span> <span data-ttu-id="6ce07-113">Pour plus d’informations, consultez la documentation fournie avec votre compilateur.</span><span class="sxs-lookup"><span data-stu-id="6ce07-113">For more information, see the documentation included with your compiler.</span></span>

<span data-ttu-id="6ce07-114">Un inconvénient potentiel de l’utilisation des dll est que l’application n’est pas autonome ; Cela dépend de l’existence d’un module DLL distinct.</span><span class="sxs-lookup"><span data-stu-id="6ce07-114">A potential disadvantage to using DLLs is that the application is not self-contained; it depends on the existence of a separate DLL module.</span></span> <span data-ttu-id="6ce07-115">Le système met fin aux processus à l’aide de la liaison dynamique au moment du chargement s’ils requièrent une DLL qui est introuvable lors du démarrage du processus et envoie un message d’erreur à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6ce07-115">The system terminates processes using load-time dynamic linking if they require a DLL that is not found at process startup and gives an error message to the user.</span></span> <span data-ttu-id="6ce07-116">Le système ne met pas fin à un processus à l’aide de la liaison dynamique au moment de l’exécution dans ce cas, mais les fonctions exportées par la DLL manquante ne sont pas disponibles pour le programme.</span><span class="sxs-lookup"><span data-stu-id="6ce07-116">The system does not terminate a process using run-time dynamic linking in this situation, but functions exported by the missing DLL are not available to the program.</span></span>

 

 



