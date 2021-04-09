---
title: Choix du type de descripteurs de liaison à utiliser
description: Choix du type de descripteurs de liaison à utiliser
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dd07716b3618766b3ea8aa07fb766f154285207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028924"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a><span data-ttu-id="0cfa8-103">Choix du type de descripteurs de liaison à utiliser</span><span class="sxs-lookup"><span data-stu-id="0cfa8-103">Choosing the Type of Binding Handles to Use</span></span>

<span data-ttu-id="0cfa8-104">**Bonne pratique :** Si vous savez quel serveur l’application doit utiliser, utilisez des handles explicites.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-104">**Best practice:** If you know which server the application will use, use explicit handles.</span></span> <span data-ttu-id="0cfa8-105">Si vous ne le faites pas, utilisez des handles explicites à chaque fois, ou utilisez des handles génériques avec des routines de **\_ liaison** et de **\_ séparation** .</span><span class="sxs-lookup"><span data-stu-id="0cfa8-105">If you don't, use explicit handles construct every time, or use generic handles with **\_bind** and **\_unbind** routines.</span></span>

<span data-ttu-id="0cfa8-106">N’utilisez pas de handles implicites ou de handles auto.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-106">Do not use implicit handles or auto handles.</span></span> <span data-ttu-id="0cfa8-107">Les handles implicites ne sont pas thread-safe, et même si la sécurité des threads peut paraître inutile, cela peut devenir nécessaire ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-107">Implicit handles are not thread safe, and even though thread safety may seem unnecessary, it could become necessary later.</span></span> <span data-ttu-id="0cfa8-108">Les handles automatiques présentent une surcharge importante et nécessitent beaucoup de programme d’installation pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-108">Auto handles have large overhead and require a lot of setup to work properly.</span></span> <span data-ttu-id="0cfa8-109">Leurs fonctionnalités de recherche ont été remplacées par les services Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-109">Their search capabilities have been superseded by Active Directory services.</span></span>

<span data-ttu-id="0cfa8-110">Les handles explicites sont très efficaces et de nombreuses fonctionnalités attrayantes sont disponibles uniquement pour les handles explicites.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-110">Explicit handles are highly efficient, and many attractive capabilities are available only for explicit handles.</span></span> <span data-ttu-id="0cfa8-111">Par exemple, si plusieurs appels RPC vont vers le même serveur, vous pouvez construire le descripteur de liaison une fois et effectuer tous les appels avec lui.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-111">For example, if several RPC calls will be going to the same server, you can construct the binding handle once and make all calls with it.</span></span> <span data-ttu-id="0cfa8-112">Cette approche est bien plus efficace que toute autre méthode.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-112">This approach is much more efficient than any other method.</span></span> <span data-ttu-id="0cfa8-113">Si le serveur vers lequel l’appel est placé est inconnu, construisez un handle de liaison explicite pour chaque appel ou utilisez des handles de liaison génériques.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-113">If the server to which the call will go is unknown, construct an explicit binding handle for every call, or use generic binding handles.</span></span>

<span data-ttu-id="0cfa8-114">Dans Microsoft™ Windows XP, le temps d’exécution RPC est très efficace lors de la réutilisation et de la mise en cache des appels. par conséquent, si le *n*+ premier appel finit sur le même serveur que le *n* ième appel, RPC réutilise les ressources allouées pour le *n* ième appel, en contournant la nécessité de mettre en cache des handles de liaison pour améliorer les performances</span><span class="sxs-lookup"><span data-stu-id="0cfa8-114">In Microsoft™ Windows XP, the RPC run time is quite efficient in re-using and caching calls, so if the *n*+1st call ends up on the same server as the *n* th call, RPC re-uses the resources allocated for the *n* th call, circumventing the need to cache binding handles to improve performance.</span></span>

 

 




