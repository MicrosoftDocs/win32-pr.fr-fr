---
description: La longévité de IPv4 a entraîné le codage en dur de nombreuses adresses IPv4 connues, telles que les adresses de bouclage (127. x. x. x), les constantes entières telles que le bouclage inaddr \_ , entre autres.
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: Utilisation d’adresses IPv4 codées en dur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8205840b1c79afcaf375b81f3223a1c780cc03d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318358"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a><span data-ttu-id="da339-103">Utilisation d’adresses IPv4 codées en dur</span><span class="sxs-lookup"><span data-stu-id="da339-103">Use of Hardcoded IPv4 Addresses</span></span>

<span data-ttu-id="da339-104">La longévité de IPv4 a entraîné le codage en dur de nombreuses adresses IPv4 connues, telles que les adresses de bouclage (127. x. x. x), les constantes entières telles que le bouclage inaddr \_ , entre autres.</span><span class="sxs-lookup"><span data-stu-id="da339-104">The longevity of IPv4 resulted in hard coding many well-known IPv4 addresses, such as loopback addresses (127.x.x.x), integer constants such as INADDR\_LOOPBACK, among others.</span></span> <span data-ttu-id="da339-105">La pratique consistant à coder en dur ces adresses présente des problèmes évidents lors de la modification d’une application existante pour prendre en charge IPv6 ou la création de nouveaux programmes indépendants de la version IP.</span><span class="sxs-lookup"><span data-stu-id="da339-105">The practice of hard coding these addresses presents obvious problems when modifying and existing application to support IPv6 or creating new IP version-independent programs.</span></span>

<span data-ttu-id="da339-106">Bonne pratique</span><span class="sxs-lookup"><span data-stu-id="da339-106">Best Practice</span></span>

-   <span data-ttu-id="da339-107">La meilleure approche consiste à éviter le codage en dur des adresses.</span><span class="sxs-lookup"><span data-stu-id="da339-107">The best approach is to avoid hardcoding any addresses.</span></span>

<span data-ttu-id="da339-108">Code pour éviter</span><span class="sxs-lookup"><span data-stu-id="da339-108">Code To Avoid</span></span>

-   <span data-ttu-id="da339-109">Évitez d’utiliser des adresses codées en dur dans le code.</span><span class="sxs-lookup"><span data-stu-id="da339-109">Avoid using hardcoded addresses in code.</span></span>

<span data-ttu-id="da339-110">**Pour modifier votre base de code existante de IPv4 en IPv4 et IPv6-interopérabilité**</span><span class="sxs-lookup"><span data-stu-id="da339-110">**To modify your existing code base from IPv4 to IPv4- and IPv6-interoperability**</span></span>

1.  <span data-ttu-id="da339-111">Acquérir l’utilitaire *Checkv4.exe* .</span><span class="sxs-lookup"><span data-stu-id="da339-111">Acquire the *Checkv4.exe* utility.</span></span> <span data-ttu-id="da339-112">L’utilitaire *Checkv4.exe* est installé dans le cadre du kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="da339-112">The *Checkv4.exe* utility is installed as part of the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later.</span></span> <span data-ttu-id="da339-113">Le SDK Windows est disponible via un abonnement MSDN et peut également être téléchargé à partir du site Web de Microsoft ( https://msdn.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="da339-113">The Windows SDK is available through an MSDN subscription and can also be downloaded from the Microsoft website (https://msdn.microsoft.com).</span></span>
2.  <span data-ttu-id="da339-114">Exécutez l’utilitaire *Checkv4.exe* sur votre code.</span><span class="sxs-lookup"><span data-stu-id="da339-114">Run the *Checkv4.exe* utility against your code.</span></span> <span data-ttu-id="da339-115">Découvrez comment exécuter l’utilitaire *Checkv4.exe* sur vos fichiers dans la section relative à l' [utilisation de l’utilitaire Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="da339-115">Learn about how to run the *Checkv4.exe* utility against your files in the section on [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>
3.  <span data-ttu-id="da339-116">L’utilitaire *Checkv4.exe* vous avertit de la présence de définitions courantes pour les adresses IPv4, telles que le bouclage inaddr \_ .</span><span class="sxs-lookup"><span data-stu-id="da339-116">The *Checkv4.exe* utility alerts you to the presence of common defines for IPv4 addresses, such as INADDR\_LOOPBACK.</span></span> <span data-ttu-id="da339-117">Modifiez tout code qui utilise des chaînes littérales avec du code qui est indépendant de la version de protocole.</span><span class="sxs-lookup"><span data-stu-id="da339-117">Modify any code that uses literal strings with code that is protocol-version agnostic.</span></span>
4.  <span data-ttu-id="da339-118">Recherchez dans votre base de code des chaînes littérales potentielles, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="da339-118">Search your code base for other potential literal strings, as appropriate.</span></span>

<span data-ttu-id="da339-119">L’utilitaire *Checkv4.exe* peut vous aider à trouver des chaînes littérales courantes, mais il peut y en avoir d’autres spécifiques à votre application.</span><span class="sxs-lookup"><span data-stu-id="da339-119">The *Checkv4.exe* utility can help you find common literal strings, but there may be others that are specific to your application.</span></span> <span data-ttu-id="da339-120">Vous devez effectuer des recherches et des tests approfondis pour vous assurer que votre code base a éliminé des problèmes potentiels associés à des chaînes littérales.</span><span class="sxs-lookup"><span data-stu-id="da339-120">You should perform thorough searching and testing to ensure your code base has eradicated potential problems associated with literal strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da339-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da339-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da339-122">Guide IPv6 pour les applications Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="da339-122">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="da339-123">Modification des structures de données pour IPv6 Winsock appications</span><span class="sxs-lookup"><span data-stu-id="da339-123">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="da339-124">Sockets à double pile pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="da339-124">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="da339-125">Appels de fonction pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="da339-125">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="da339-126">Problèmes d’interface utilisateur pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="da339-126">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="da339-127">Protocoles sous-jacents pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="da339-127">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 



