---
title: Marshaling d’interface
description: Marshaling d’interface
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5112b67e643fb95e1025fd4ed297043f81f576e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106512756"
---
# <a name="interface-marshaling"></a><span data-ttu-id="ac26d-103">Marshaling d’interface</span><span class="sxs-lookup"><span data-stu-id="ac26d-103">Interface Marshaling</span></span>

<span data-ttu-id="ac26d-104">À moins que vous ne sachiez au-delà que votre interface ne sera jamais utilisée dans les limites de cloisonnement, de thread ou de processus, vous devez décider comment assurer la prise en charge du marshaling pour vos interfaces.</span><span class="sxs-lookup"><span data-stu-id="ac26d-104">Unless you know beyond all doubt that your interface will never be used across apartment, thread, or process boundaries, you need to decide how to provide marshaling support for your interfaces.</span></span> <span data-ttu-id="ac26d-105">Il existe trois façons de fournir une prise en charge du marshaling :</span><span class="sxs-lookup"><span data-stu-id="ac26d-105">There are three ways to provide marshaling support:</span></span>

-   <span data-ttu-id="ac26d-106">Écrivez votre propre code proxy/stub qui appelle le canal COM, qui à son tour appelle les bibliothèques Runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="ac26d-106">Write your own proxy/stub code that calls the COM channel, which in turn calls the RPC run-time libraries.</span></span> <span data-ttu-id="ac26d-107">En théorie, il est possible de le faire, mais dans la pratique, il est presque impossible de le faire sans beaucoup d’efforts.</span><span class="sxs-lookup"><span data-stu-id="ac26d-107">Theoretically, it is possible to do this, but in practice it is almost impossible to do without a significant amount of effort.</span></span>
-   <span data-ttu-id="ac26d-108">Décrivez vos interfaces dans un fichier IDL (Interface Definition Language) et utilisez le compilateur MIDL pour générer une DLL proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="ac26d-108">Describe your interfaces in an interface definition language (IDL) file and use the MIDL compiler to generate a proxy/stub DLL.</span></span> <span data-ttu-id="ac26d-109">Cette méthode fournit les meilleures performances et la plus grande flexibilité en termes de types de données acceptables.</span><span class="sxs-lookup"><span data-stu-id="ac26d-109">This method provides the best performance and the most flexibility in terms of acceptable data types.</span></span> <span data-ttu-id="ac26d-110">À l’aide de stubs proxy générés par MIDL, vous pouvez contrôler non seulement la gestion de la mémoire, mais également le marshaling et le démarshaling de types de données complexes sur différentes plateformes.</span><span class="sxs-lookup"><span data-stu-id="ac26d-110">Using MIDL-generated proxy stubs, you can control not only memory management but even the marshaling and unmarshaling of complex data types across different platforms.</span></span>
-   <span data-ttu-id="ac26d-111">Utilisez MIDL pour générer une bibliothèque de types que le système utilise pour assurer la prise en charge du marshaling au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ac26d-111">Use MIDL to generate a type library that the system uses to provide marshaling support at run time.</span></span> <span data-ttu-id="ac26d-112">Il s’agit du moyen le plus simple d’implémenter la prise en charge du marshaling.</span><span class="sxs-lookup"><span data-stu-id="ac26d-112">This is the easiest way to implement marshaling support.</span></span> <span data-ttu-id="ac26d-113">Il vous suffit de générer une bibliothèque de types et de l’inscrire.</span><span class="sxs-lookup"><span data-stu-id="ac26d-113">All you have to do is generate a type library and register it.</span></span> <span data-ttu-id="ac26d-114">Vos interfaces doivent être compatibles avec Automation ( [**oleautomation**](/windows/desktop/Midl/oleautomation) ou [**Dual**](/windows/desktop/Midl/dual)), ce qui impose des restrictions sur les types de données que vous pouvez utiliser comme paramètres de méthode.</span><span class="sxs-lookup"><span data-stu-id="ac26d-114">Your interfaces must be Automation-compatible (either [**oleautomation**](/windows/desktop/Midl/oleautomation) or [**dual**](/windows/desktop/Midl/dual)), which places some restrictions on the kinds of data types you can use as method parameters.</span></span> <span data-ttu-id="ac26d-115">Toutefois, dans la plupart des cas, l’avantage d’avoir vos interfaces accessibles aux programmes écrits dans d’autres langages, tels que Microsoft Visual Basic et Java, compense les limitations relatives aux types de données.</span><span class="sxs-lookup"><span data-stu-id="ac26d-115">However, in most cases, the advantage of having your interfaces accessible to programs written in other languages, such as Microsoft Visual Basic and Java, outweighs the limitations on data types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac26d-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ac26d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac26d-117">Communication entre les objets</span><span class="sxs-lookup"><span data-stu-id="ac26d-117">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> </dl>

 

 