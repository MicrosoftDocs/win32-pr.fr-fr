---
description: Microsoft a implémenté un tableau d’extensions pour le format de fichier de configuration automatique du navigateur afin d’ajouter la prise en charge IPv6 dans les fonctions d’assistance WPAD WinINet et WinHTTP.
ms.assetid: 40116a01-b18f-432a-8542-b56b3f55c692
title: Extensions IPv6 du format de fichier de configuration automatique du navigateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b57fce93caaf7790136ee9ac7db04017d9ac11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523376"
---
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a><span data-ttu-id="1b599-103">Extensions IPv6 du format de fichier de configuration automatique du navigateur</span><span class="sxs-lookup"><span data-stu-id="1b599-103">IPv6 Extensions to Navigator Auto-Config File Format</span></span>

<span data-ttu-id="1b599-104">Microsoft a implémenté un tableau d’extensions pour le format de fichier de configuration automatique du navigateur afin d’ajouter la prise en charge IPv6 dans les fonctions d’assistance WPAD WinINet et WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="1b599-104">Microsoft has implemented an array of extensions to the Navigator Auto-Config File Format in order to add IPv6 support in the WinINet and WinHTTP WPAD helper functions.</span></span>

<span data-ttu-id="1b599-105">L’explosion d’Internet à la fin des années 1990 a provoqué un manque inattendu d’adresses IPv4, le pool étant épuisé quotidiennement.</span><span class="sxs-lookup"><span data-stu-id="1b599-105">The explosion of the Internet in the late 1990’s has caused an unexpected scarcity of IPv4 addresses, with the pool depleting on a daily basis.</span></span> <span data-ttu-id="1b599-106">IPv6 fournit une solution à ce problème et, bien qu’il ne soit pas largement déployé, son utilisation sera de plus en plus répandue à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="1b599-106">IPv6 provides a solution to this problem and although it is currently not widely deployed, its use will definitely become more prevalent in the future.</span></span> <span data-ttu-id="1b599-107">[WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) est un protocole qui permet aux clients Web de détecter automatiquement la configuration de proxy appropriée pour le trafic sortant.</span><span class="sxs-lookup"><span data-stu-id="1b599-107">[WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) is a protocol that allows web clients to automatically detect what the correct proxy configuration should be for their outgoing traffic.</span></span> <span data-ttu-id="1b599-108">Cette fonctionnalité est très utile pour les déploiements d’entreprise, car elle permet aux administrateurs informatiques de configurer des scripts complexes capables d’acheminer le trafic de tous les clients vers des proxies spécifiques en fonction du serveur cible auquel les clients tentent de se connecter.</span><span class="sxs-lookup"><span data-stu-id="1b599-108">This is very useful for corporate deployments because it allows IT administrators to setup complex scripts that can route traffic for all clients to specific proxies based on the target server the clients are attempting to connect to.</span></span> <span data-ttu-id="1b599-109">WinINet et WinHTTP prennent en charge les fonctions d’assistance WPAD, telles que définies par la [spécification de format de fichier de configuration automatique du proxy du navigateur (PAC)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), qui est devenue une norme de facto.</span><span class="sxs-lookup"><span data-stu-id="1b599-109">WinINet and WinHTTP support WPAD helper functions as defined by the [Navigator Proxy Auto-Config (PAC) File Format specification](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), which has become a defacto standard.</span></span> <span data-ttu-id="1b599-110">Malheureusement, cette spécification a été écrite en 1996 et ne définit pas les comportements de fonction lorsqu’un script WPAD est déployé sur un réseau compatible IPv6.</span><span class="sxs-lookup"><span data-stu-id="1b599-110">Unfortunately this specification was written in 1996 and does not define what the function behaviors should be when a WPAD script is deployed in an IPv6 capable network.</span></span>

<span data-ttu-id="1b599-111">Étant donné que le protocole IPv6 est la vague du futur, tous les composants Windows prennent désormais en charge les réseaux à double pile (IPv4 et IPv6) et IPv6 uniquement.</span><span class="sxs-lookup"><span data-stu-id="1b599-111">Since IPv6 is the wave of the future, all Windows components now support dual stack (IPv4 and IPv6) and IPv6 only networks.</span></span> <span data-ttu-id="1b599-112">Pour prendre en charge IPv6 sans affecter le déploiement existant, Microsoft a ajouté 6 nouvelles fonctions de classe d’assistance en tant qu’extension de la spécification de format de fichier de configuration automatique du proxy du navigateur (PAC) et a également ajouté une nouvelle fonction compatible IPv6 appelée **FindProxyForURLEx** que les administrateurs peuvent implémenter dans le script WPAD.</span><span class="sxs-lookup"><span data-stu-id="1b599-112">In order to support IPv6 without affecting existing deployment, Microsoft added 6 new helper class functions as an extension to the Navigator Proxy Auto-Config (PAC) File Format specification and also added a new IPv6 capable function called **FindProxyForURLEx** that administrators can implement in the WPAD script.</span></span>

<dl> <dt>

[<span data-ttu-id="1b599-113">Définitions d’API d’assistance du proxy compatibles IPv6</span><span class="sxs-lookup"><span data-stu-id="1b599-113">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[<span data-ttu-id="1b599-114">Différences entre les fonctions d’assistance WPAD IPv6-Aware et les fonctions d’assistance WPAD héritées</span><span class="sxs-lookup"><span data-stu-id="1b599-114">Differences Between IPv6-Aware WPAD Helper Functions and Legacy WPAD Helper Functions</span></span>](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
<span data-ttu-id="1b599-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1b599-115"></dt> <dd></dd> </dl></span></span>

> [!Note]  
> <span data-ttu-id="1b599-116">Cette fonctionnalité nécessite Windows Internet Explorer 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1b599-116">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



