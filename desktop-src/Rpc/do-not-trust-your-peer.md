---
title: Ne pas faire confiance à votre homologue
description: '\ 0034 ; ne faites pas confiance à votre homologue \ 0034 ; est une règle de sécurité de base, mais elle est souvent négligée.'
ms.assetid: 776c1c99-feb1-415c-9a18-e9bf581bc3ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c5c7ba3760e14a66fb4765000c7a6698599b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672842"
---
# <a name="do-not-trust-your-peer"></a><span data-ttu-id="ad110-103">Ne pas faire confiance à votre homologue</span><span class="sxs-lookup"><span data-stu-id="ad110-103">Do Not Trust Your Peer</span></span>

<span data-ttu-id="ad110-104">« Ne pas approuver votre homologue » est une règle de sécurité de base, mais elle est souvent négligée.</span><span class="sxs-lookup"><span data-stu-id="ad110-104">"Do not trust your peer" is a basic security rule, but it is often overlooked.</span></span> <span data-ttu-id="ad110-105">Ne partez pas du principe que l’autre partie d’une communication se comporte correctement et ne supposez pas que votre homologue transmettra les données attendues.</span><span class="sxs-lookup"><span data-stu-id="ad110-105">Do not assume the other party in a communication will behave properly, and do not assume your peer will pass the data you expect.</span></span> <span data-ttu-id="ad110-106">MIDL et RPC effectuent des vérifications en votre nom, mais pas toutes les vérifications.</span><span class="sxs-lookup"><span data-stu-id="ad110-106">MIDL and RPC perform some checks on your behalf, but not all checks.</span></span>

<span data-ttu-id="ad110-107">Savoir quel aspect des paramètres sont vérifiés par MIDL ou RPC, et quels aspects vous devez vérifier vous-même.</span><span class="sxs-lookup"><span data-stu-id="ad110-107">Know which aspect of the parameters are verified by MIDL or RPC, and which aspects you must verify yourself.</span></span> <span data-ttu-id="ad110-108">Par exemple, pour les handles de contexte in/out, RPC vérifie que le handle de contexte n’est pas une valeur non null valide.</span><span class="sxs-lookup"><span data-stu-id="ad110-108">For example, for in/out context handles, RPC verifies the context handle is not an invalid non-null value.</span></span> <span data-ttu-id="ad110-109">Elle autorise les valeurs NULL et les valeurs valides, mais de nombreux développeurs ne savent pas que les valeurs NULL sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="ad110-109">It allows null values and valid values, but many developers are not aware that null values are let through.</span></span> <span data-ttu-id="ad110-110">Il s’agit d’un point à vérifier.</span><span class="sxs-lookup"><span data-stu-id="ad110-110">This is something to check for.</span></span>

<span data-ttu-id="ad110-111">Même si vous faites généralement confiance à votre homologue, veillez à ne pas introduire de nouveaux chemins d’accès par lesquels un ordinateur compromis ou un compte principal peut attaquer d’autres ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="ad110-111">Even if you generally trust your peer, be sure not to introduce new paths by which a compromised machine or principal account can attack other machines.</span></span> <span data-ttu-id="ad110-112">Imaginez qu’un utilisateur choisit son mot de passe anniversaire et qu’il est deviné par un pirate.</span><span class="sxs-lookup"><span data-stu-id="ad110-112">Imagine that a user chooses his birthday as his password, and it is guessed by an attacker.</span></span> <span data-ttu-id="ad110-113">Même après l’authentification des demandes de l’utilisateur et l’accès à ses données est autorisé, assurez-vous qu’il n’existe pas de vulnérabilités exploitables, telles que des dépassements de pile qui peuvent permettre à une personne malveillante de prendre le contrôle de votre serveur et d’étendre la violation de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="ad110-113">Even after requests from the user are authenticated and access to his data is allowed, make sure exploitable vulnerabilities do not exist, such stack overruns that may allow an attacker to take control of your server and extend the security breach.</span></span>

 

 




