---
title: Choix d’un niveau d’authentification
description: Lors du choix d’un niveau d’authentification, utilisez les instructions suivantes.
ms.assetid: 6efb4162-5884-4bcb-86da-4809f89f0c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba73b2541497ff70204151e57f0483ac7965ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462162"
---
# <a name="choosing-an-authentication-level"></a><span data-ttu-id="68131-103">Choix d’un niveau d’authentification</span><span class="sxs-lookup"><span data-stu-id="68131-103">Choosing an Authentication Level</span></span>

<span data-ttu-id="68131-104">Lors du choix d’un niveau d’authentification, utilisez les instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="68131-104">When choosing an authentication level, use the following guideline.</span></span> <span data-ttu-id="68131-105">S’il n’est pas important que les données envoyées puissent être interceptées et modifiées, et que les données reçues puissent être interceptées ou modifiées, utilisez \_ le niveau d’authentification RPC C « \_ \_ aucun » \_ , qui est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="68131-105">If it does not matter whether the data being sent can be intercepted and modified, and the data received can be intercepted or modified, use RPC\_C\_AUTHN\_LEVEL\_NONE, which is the default.</span></span> <span data-ttu-id="68131-106">Si les données ne doivent pas être modifiées et que les données privées ne sont pas envoyées ou reçues, \_ Utilisez \_ \_ \_ l’intégrité PKT du niveau d’authentification RPC C \_ .</span><span class="sxs-lookup"><span data-stu-id="68131-106">If the data should not be modified, and private data is not being sent or received, use RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY.</span></span> <span data-ttu-id="68131-107">Dans tous les autres cas, utilisez \_ la \_ confidentialité du niveau d’authentification RPC C \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="68131-107">In all other cases, use RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY.</span></span>

<span data-ttu-id="68131-108">N’utilisez pas le \_ niveau d’authentification RPC c \_ \_ par défaut, le niveau d' \_ \_ authentification RPC c \_ \_ Connect, l’appel de niveau d’authentification \_ RPC \_ c ou le \_ niveau d' \_ authentification par \_ \_ authentification c RPC \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="68131-108">Do not use RPC\_C\_AUTHN\_LEVEL\_DEFAULT, RPC\_C\_AUTHN\_LEVEL\_CONNECT, RPC\_C\_AUTHN\_LEVEL\_CALL or RPC\_C\_AUTHN\_LEVEL\_PKT.</span></span> <span data-ttu-id="68131-109">Une personne malveillante sophistiquée peut arrêter ces niveaux d’authentification et les rendre inefficaces.</span><span class="sxs-lookup"><span data-stu-id="68131-109">A sophisticated attacker can break these authentication levels and render them ineffective.</span></span> <span data-ttu-id="68131-110">Chacun de ces niveaux rend légèrement plus difficile pour une personne malveillante d’intercepter et de modifier des données, et d’emprunter l’identité, mais la sécurité n’est pas vraiment obtenue.</span><span class="sxs-lookup"><span data-stu-id="68131-110">Each of these levels does make it slightly more difficult for an attacker to intercept and modify data, and to impersonate, but security is not really achieved.</span></span> <span data-ttu-id="68131-111">Étant donné que le niveau de sophistication d’une personne malveillante est rarement connu, il ne s’agit pas de choix judicieux.</span><span class="sxs-lookup"><span data-stu-id="68131-111">Since the sophistication level of an attacker is rarely known, these are not wise choices.</span></span>

 

 




