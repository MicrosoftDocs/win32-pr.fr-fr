---
description: L' \_ option de socket de niveau de protection IPv6 permet aux \_ développeurs de placer des restrictions d’accès sur les sockets IPv6.
ms.assetid: bfb934b3-1e86-431f-a21c-880048d32d35
title: IPV6_PROTECTION_LEVEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2a8dd70bb1fb5b21f74f8939f11da0d9e2a3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536329"
---
# <a name="ipv6_protection_level"></a><span data-ttu-id="8a79d-103">\_Niveau de protection IPv6 \_</span><span class="sxs-lookup"><span data-stu-id="8a79d-103">IPV6\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="8a79d-104">L' \_ option de socket de niveau de protection IPv6 permet aux \_ développeurs de placer des restrictions d’accès sur les sockets IPv6.</span><span class="sxs-lookup"><span data-stu-id="8a79d-104">The IPV6\_PROTECTION\_LEVEL socket option enables developers to place access restrictions on IPv6 sockets.</span></span> <span data-ttu-id="8a79d-105">Ces restrictions permettent à une application qui s'exécute sur un réseau local privé de se renforcer facilement et efficacement contre les attaques externes.</span><span class="sxs-lookup"><span data-stu-id="8a79d-105">Such restrictions enable an application running on a private LAN to simply and robustly harden itself against external attacks.</span></span> <span data-ttu-id="8a79d-106">L' \_ \_ option de socket de niveau de protection IPv6 élargit ou limite l’étendue d’un socket d’écoute, en permettant l’accès illimité des utilisateurs publics et privés, le cas échéant, ou en limitant l’accès au même site, selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="8a79d-106">The IPV6\_PROTECTION\_LEVEL socket option widens or narrows the scope of a listening socket, enabling unrestricted access from public and private users when appropriate, or restricting access only to the same site, as required.</span></span>

<span data-ttu-id="8a79d-107">Le \_ niveau de protection IPv6 \_ a actuellement trois niveaux de protection définis.</span><span class="sxs-lookup"><span data-stu-id="8a79d-107">IPV6\_PROTECTION\_LEVEL currently has three defined protection levels.</span></span>



| <span data-ttu-id="8a79d-108">Niveau de protection</span><span class="sxs-lookup"><span data-stu-id="8a79d-108">Protection level</span></span>                                                                                                                                 | <span data-ttu-id="8a79d-109">Description</span><span class="sxs-lookup"><span data-stu-id="8a79d-109">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a79d-110"><span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>niveau de PROTECTION non \_ \_ restreint</span><span class="sxs-lookup"><span data-stu-id="8a79d-110"><span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>PROTECTION\_LEVEL\_UNRESTRICTED</span></span><br/>       | <span data-ttu-id="8a79d-111">Utilisé par les applications conçues pour fonctionner sur Internet, y compris les applications tirant parti des capacités de traversée NAT IPv6 intégrées à Windows (Teredo, par exemple).</span><span class="sxs-lookup"><span data-stu-id="8a79d-111">Used by applications designed to operate across the Internet, including applications taking advantage of IPv6 NAT traversal capabilities built into Windows (Teredo, for example).</span></span> <span data-ttu-id="8a79d-112">Ces applications peuvent contourner les pare-feux IPv4 ; elles doivent donc être renforcées contre les attaques Internet dirigées sur le port ouvert.</span><span class="sxs-lookup"><span data-stu-id="8a79d-112">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span><br/> |
| <span data-ttu-id="8a79d-113"><span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>niveau de PROTECTION \_ \_ EDGERESTRICTED</span><span class="sxs-lookup"><span data-stu-id="8a79d-113"><span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>PROTECTION\_LEVEL\_EDGERESTRICTED</span></span><br/> | <span data-ttu-id="8a79d-114">Utilisé par les applications conçues pour fonctionner sur Internet.</span><span class="sxs-lookup"><span data-stu-id="8a79d-114">Used by applications designed to operate across the Internet.</span></span> <span data-ttu-id="8a79d-115">Ce paramètre n’autorise pas la traversée NAT à l’aide de l’implémentation de Windows Teredo.</span><span class="sxs-lookup"><span data-stu-id="8a79d-115">This setting does not allow NAT traversal using the Windows Teredo implementation.</span></span> <span data-ttu-id="8a79d-116">Ces applications peuvent contourner les pare-feux IPv4 ; elles doivent donc être renforcées contre les attaques Internet dirigées sur le port ouvert.</span><span class="sxs-lookup"><span data-stu-id="8a79d-116">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span><br/>                                   |
| <span data-ttu-id="8a79d-117"><span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>niveau de PROTECTION \_ \_ restreint</span><span class="sxs-lookup"><span data-stu-id="8a79d-117"><span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>PROTECTION\_LEVEL\_RESTRICTED</span></span><br/>             | <span data-ttu-id="8a79d-118">Utilisé par les applications intranet qui n’implémentent pas les scénarios Internet.</span><span class="sxs-lookup"><span data-stu-id="8a79d-118">Used by intranet applications that do not implement Internet scenarios.</span></span> <span data-ttu-id="8a79d-119">Ces applications ne sont généralement pas testées ou renforcées contre les attaques Internet.</span><span class="sxs-lookup"><span data-stu-id="8a79d-119">These applications are generally not tested or hardened against Internet-style attacks.</span></span><br/> <span data-ttu-id="8a79d-120">Ce paramètre limitera uniquement le trafic reçu aux liens locaux.</span><span class="sxs-lookup"><span data-stu-id="8a79d-120">This setting will limit the received traffic to link-local only.</span></span><br/>                                                                             |



 

<span data-ttu-id="8a79d-121">L’exemple de code suivant fournit les valeurs définies pour chaque :</span><span class="sxs-lookup"><span data-stu-id="8a79d-121">The following code example provides the defined values for each:</span></span>

``` syntax
#define PROTECTION_LEVEL_UNRESTRICTED   10  /* for peer-to-peer apps */
#define PROTECTION_LEVEL_EDGERESTRICTED 20  /* Same as unrestricted, except for Teredo  */
#define PROTECTION_LEVEL_RESTRICTED     30  /* for Intranet apps     */
```

<span data-ttu-id="8a79d-122">Ces valeurs s’excluent mutuellement et ne peuvent pas être combinées dans un seul appel de fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) .</span><span class="sxs-lookup"><span data-stu-id="8a79d-122">These values are mutually exclusive, and cannot be combined in a single [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function call.</span></span> <span data-ttu-id="8a79d-123">Les autres valeurs de cette option de socket sont réservées.</span><span class="sxs-lookup"><span data-stu-id="8a79d-123">Other values for this socket option are reserved.</span></span> <span data-ttu-id="8a79d-124">Ces niveaux de protection s’appliquent uniquement aux connexions entrantes.</span><span class="sxs-lookup"><span data-stu-id="8a79d-124">These protection levels apply only to incoming connections.</span></span> <span data-ttu-id="8a79d-125">La définition de cette option de socket n’a aucun effet sur les paquets sortants ou les connexions.</span><span class="sxs-lookup"><span data-stu-id="8a79d-125">Setting this socket option has no effect on outbound packets or connections.</span></span>

<span data-ttu-id="8a79d-126">Sur Windows 7 et Windows Server 2008 R2, la valeur par défaut du \_ niveau de protection IPv6 n’est pas spécifiée et le niveau de protection \_ **\_ \_ par défaut** est défini sur-1, une valeur non autorisée pour le \_ niveau de protection IPv6 \_ .</span><span class="sxs-lookup"><span data-stu-id="8a79d-126">On Windows 7 and Windows Server 2008 R2, the default value for IPV6\_PROTECTION\_LEVEL is unspecified and **PROTECTION\_LEVEL\_DEFAULT** is defined to -1, an illegal value for IPV6\_PROTECTION\_LEVEL.</span></span>

<span data-ttu-id="8a79d-127">Sur Windows Vista et Windows Server 2008, la valeur par défaut du niveau de protection IPV6 \_ \_ est **niveau de protection non \_ \_ restreint** et le **niveau de protection \_ \_ par défaut** est défini sur-1, une valeur non autorisée pour le \_ niveau de protection IPv6 \_ .</span><span class="sxs-lookup"><span data-stu-id="8a79d-127">On Windows Vista and Windows Server 2008, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED** and **PROTECTION\_LEVEL\_DEFAULT** is defined to -1, an illegal value for IPV6\_PROTECTION\_LEVEL.</span></span>

<span data-ttu-id="8a79d-128">Sur Windows Server 2003 et Windows XP, la valeur par défaut pour le niveau de protection IPV6 \_ \_ est niveau de protection **\_ \_ EDGERESTRICTED** et niveau de protection **\_ \_ par défaut** est défini pour le **niveau de protection \_ \_ EDGERESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="8a79d-128">On Windows Server 2003 and Windows XP, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_EDGERESTRICTED** and **PROTECTION\_LEVEL\_DEFAULT** is defined to be **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>

> [!Note]  
> <span data-ttu-id="8a79d-129">L' \_ option de socket de niveau de protection IPv6 \_ doit être définie avant que le socket ne soit lié.</span><span class="sxs-lookup"><span data-stu-id="8a79d-129">The IPV6\_PROTECTION\_LEVEL socket option should be set before the socket is bound.</span></span> <span data-ttu-id="8a79d-130">Dans le cas contraire, les paquets reçus entre les appels [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) et [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) sont conformes au **niveau de protection \_ \_ EDGERESTRICTED** et peuvent être remis à l’application.</span><span class="sxs-lookup"><span data-stu-id="8a79d-130">Otherwise, packets received between [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) and [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) calls will conform to **PROTECTION\_LEVEL\_EDGERESTRICTED**, and may be delivered to the application.</span></span>

 

<span data-ttu-id="8a79d-131">Le tableau suivant décrit l’effet de l’application de chaque niveau de protection à un socket d’écoute.</span><span class="sxs-lookup"><span data-stu-id="8a79d-131">The following table describes the effect of applying each protection level to a listening socket.</span></span>

<span data-ttu-id="8a79d-132">Niveau de protection</span><span class="sxs-lookup"><span data-stu-id="8a79d-132">Protection level</span></span>

<span data-ttu-id="8a79d-133">Trafic entrant autorisé</span><span class="sxs-lookup"><span data-stu-id="8a79d-133">Incoming traffic permitted</span></span>

<span data-ttu-id="8a79d-134">Même site</span><span class="sxs-lookup"><span data-stu-id="8a79d-134">Same site</span></span>

<span data-ttu-id="8a79d-135">Externe</span><span class="sxs-lookup"><span data-stu-id="8a79d-135">External</span></span>

<span data-ttu-id="8a79d-136">Parcours NAT (Teredo)</span><span class="sxs-lookup"><span data-stu-id="8a79d-136">NAT traversal (Teredo)</span></span>

<span data-ttu-id="8a79d-137">niveau de PROTECTION \_ \_ restreint</span><span class="sxs-lookup"><span data-stu-id="8a79d-137">PROTECTION\_LEVEL\_RESTRICTED</span></span>

<span data-ttu-id="8a79d-138">Oui</span><span class="sxs-lookup"><span data-stu-id="8a79d-138">Yes</span></span>

<span data-ttu-id="8a79d-139">Non</span><span class="sxs-lookup"><span data-stu-id="8a79d-139">No</span></span>

<span data-ttu-id="8a79d-140">Non</span><span class="sxs-lookup"><span data-stu-id="8a79d-140">No</span></span>

<span data-ttu-id="8a79d-141">niveau de PROTECTION \_ \_ EDGERESTRICTED</span><span class="sxs-lookup"><span data-stu-id="8a79d-141">PROTECTION\_LEVEL\_EDGERESTRICTED</span></span>

<span data-ttu-id="8a79d-142">Oui</span><span class="sxs-lookup"><span data-stu-id="8a79d-142">Yes</span></span>

<span data-ttu-id="8a79d-143">Oui</span><span class="sxs-lookup"><span data-stu-id="8a79d-143">Yes</span></span>

<span data-ttu-id="8a79d-144">Non</span><span class="sxs-lookup"><span data-stu-id="8a79d-144">No</span></span>

<span data-ttu-id="8a79d-145">niveau de PROTECTION non \_ \_ restreint</span><span class="sxs-lookup"><span data-stu-id="8a79d-145">PROTECTION\_LEVEL\_UNRESTRICTED</span></span>

<span data-ttu-id="8a79d-146">Oui</span><span class="sxs-lookup"><span data-stu-id="8a79d-146">Yes</span></span>

<span data-ttu-id="8a79d-147">Oui</span><span class="sxs-lookup"><span data-stu-id="8a79d-147">Yes</span></span>

<span data-ttu-id="8a79d-148">Oui</span><span class="sxs-lookup"><span data-stu-id="8a79d-148">Yes</span></span>



 

<span data-ttu-id="8a79d-149">Dans le tableau ci-dessus, la même colonne de **site** est une combinaison des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8a79d-149">In the table above, the **Same site** column is a combination of the following:</span></span>

-   <span data-ttu-id="8a79d-150">Lier des adresses locales</span><span class="sxs-lookup"><span data-stu-id="8a79d-150">Link local addresses</span></span>
-   <span data-ttu-id="8a79d-151">Adresses locales du site</span><span class="sxs-lookup"><span data-stu-id="8a79d-151">Site Local addresses</span></span>
-   <span data-ttu-id="8a79d-152">Adresses globales connues pour appartenir au même site (correspondant à la table de préfixe de site)</span><span class="sxs-lookup"><span data-stu-id="8a79d-152">Global addresses known to belong to the same site (matching the site prefix table)</span></span>

<span data-ttu-id="8a79d-153">Sur Windows 7 et Windows Server 2008 R2, la valeur par défaut du \_ niveau de protection IPv6 \_ n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8a79d-153">On Windows 7 and Windows Server 2008 R2, the default value for IPV6\_PROTECTION\_LEVEL is unspecified.</span></span> <span data-ttu-id="8a79d-154">Si aucun logiciel de pare-feu prenant en charge la traversée latérale n’est installé sur l’ordinateur local (le pare-feu Windows est désactivé ou un autre pare-feu est installé, qui ignore le trafic Teredo), vous recevrez le trafic Teredo uniquement si vous définissez l' \_ \_ option de socket niveau de protection IPv6 sur **niveau de protection non \_ \_ restreint**.</span><span class="sxs-lookup"><span data-stu-id="8a79d-154">If there is no edge-traversal aware firewall software installed on the local computer (Windows firewall is disabled or some other firewall is installed that ignores Teredo traffic), you will receive Teredo traffic only if you set the IPV6\_PROTECTION\_LEVEL socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="8a79d-155">Toutefois, le pare-feu Windows ou toute stratégie de pare-feu prenant en charge la traversée latérale peut ignorer cette option en fonction des paramètres de stratégie du pare-feu.</span><span class="sxs-lookup"><span data-stu-id="8a79d-155">However, Windows firewall or any edge-traversal aware firewall policy may ignore this option based on policy settings for the firewall.</span></span> <span data-ttu-id="8a79d-156">En définissant cette option de socket sur **niveau de protection \_ \_ sans restriction**, l’application communique son intention explicite de recevoir le trafic traversé par le pare-feu hôte installé sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8a79d-156">By setting this socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**, the application is communicating its explicit intent to receive edge traversed traffic by the host firewall installed on the local machine.</span></span> <span data-ttu-id="8a79d-157">Par conséquent, si un pare-feu hôte prenant en charge la traversée latérale est installé, il aura la décision finale d’accepter un paquet.</span><span class="sxs-lookup"><span data-stu-id="8a79d-157">So if there is an edge-traversal aware host firewall installed, it will have the final decision on accepting a packet.</span></span> <span data-ttu-id="8a79d-158">Par défaut, sans option de socket définie :</span><span class="sxs-lookup"><span data-stu-id="8a79d-158">By default, without any socket option set:</span></span>

-   <span data-ttu-id="8a79d-159">o si le pare-feu Windows est activé (ou qu’un autre pare-feu d’hôte prenant en charge la traversée latérale est installé) sur l’ordinateur local, tout ce qu’il impose est observé.</span><span class="sxs-lookup"><span data-stu-id="8a79d-159">o If Windows firewall is enabled (or another edge-traversal aware host firewall is installed) on the local computer, whatever it enforces will be observed.</span></span> <span data-ttu-id="8a79d-160">Le pare-feu d’hôte prenant en charge la traversée latérale standard bloquera le trafic Teredo par défaut.</span><span class="sxs-lookup"><span data-stu-id="8a79d-160">Typical edge-traversal aware host firewall will block Teredo traffic by default.</span></span> <span data-ttu-id="8a79d-161">Par conséquent, les applications observent la valeur par défaut comme s’il s’agissait d’un **niveau de protection \_ \_ EDGERESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="8a79d-161">Therefore applications will observe the default as if it was **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>
-   <span data-ttu-id="8a79d-162">o si le pare-feu Windows n’est pas activé et qu’aucun autre pare-feu d’hôte prenant en charge la traversée latérale n’est installé sur le système local, le niveau de protection par défaut est **\_ \_ EDGERESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="8a79d-162">o If Windows firewall is not enabled and no other edge-traversal aware host firewall is installed on the local system, the default will be **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>

<span data-ttu-id="8a79d-163">Sur Windows Vista et Windows Server 2008, la valeur par défaut du niveau de protection IPV6 \_ \_ est **niveau de protection non \_ \_ restreint**.</span><span class="sxs-lookup"><span data-stu-id="8a79d-163">On Windows Vista and Windows Server 2008, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="8a79d-164">Mais la valeur effective varie selon que le pare-feu Windows est activé ou non.</span><span class="sxs-lookup"><span data-stu-id="8a79d-164">But the effective value depends on whether Windows firewall is enabled.</span></span> <span data-ttu-id="8a79d-165">Le pare-feu Windows prend en charge la traversée latérale (prise en charge de Teredo), quelle que soit la valeur définie pour le \_ niveau de protection IPv6 \_ et ignore si le niveau de protection IPv6 est sans \_ \_ **\_ \_ restriction**.</span><span class="sxs-lookup"><span data-stu-id="8a79d-165">The Windows firewall is edge-traversal aware (Teredo aware), no matter what value is set for the IPV6\_PROTECTION\_LEVEL and ignores if IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="8a79d-166">La valeur effective dépend de la stratégie de pare-feu.</span><span class="sxs-lookup"><span data-stu-id="8a79d-166">So the effective value depends on the firewall policy.</span></span> <span data-ttu-id="8a79d-167">Lorsque le pare-feu Windows est désactivé et qu’aucun autre pare-feu prenant en charge la traversée latérale n’est installé sur l’ordinateur local, la valeur par défaut du niveau de protection IPV6 \_ \_ est **niveau de protection non \_ \_ restreint**.</span><span class="sxs-lookup"><span data-stu-id="8a79d-167">When Windows firewall is disabled and no other edge-traversal aware firewall is installed on the local computer, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span>

<span data-ttu-id="8a79d-168">Sur Windows Server 2003 et Windows XP, la valeur par défaut pour le \_ niveau de protection IPv6 \_ est niveau de **protection \_ \_ EDGERESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="8a79d-168">On Windows Server 2003 and Windows XP, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span> <span data-ttu-id="8a79d-169">À moins que vous n’ayez défini l' \_ \_ option de socket de niveau de protection IPv6 sur **niveau de protection non \_ \_ restreint**, vous ne recevrez pas de trafic Teredo.</span><span class="sxs-lookup"><span data-stu-id="8a79d-169">Unless you have set the IPV6\_PROTECTION\_LEVEL socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**, you would not receive any Teredo traffic.</span></span>

<span data-ttu-id="8a79d-170">Selon le \_ niveau de protection IPv6 \_ , une application qui nécessite un trafic non sollicité provenant d’Internet peut ne pas être capable de recevoir du trafic non sollicité.</span><span class="sxs-lookup"><span data-stu-id="8a79d-170">Depending on the IPV6\_PROTECTION\_LEVEL, an application that requires unsolicited traffic from the Internet may not be capable of receiving unsolicited traffic.</span></span> <span data-ttu-id="8a79d-171">Toutefois, ces exigences ne sont pas nécessaires pour recevoir le trafic sollicité sur l’interface Windows Teredo.</span><span class="sxs-lookup"><span data-stu-id="8a79d-171">However, these requirements are not necessary for receiving solicited traffic over the Windows Teredo interface.</span></span> <span data-ttu-id="8a79d-172">Pour plus d’informations sur l’interaction avec Teredo, consultez [réception du trafic sollicité sur Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).</span><span class="sxs-lookup"><span data-stu-id="8a79d-172">For more details on the interaction with Teredo, see [Receiving Solicited Traffic Over Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).</span></span>

<span data-ttu-id="8a79d-173">Lorsque des paquets entrants ou des connexions sont refusés en raison du niveau de protection défini, le rejet est géré comme si aucune application n’était à l’écoute sur ce Socket.</span><span class="sxs-lookup"><span data-stu-id="8a79d-173">When incoming packets or connections are refused due to the set protection level, rejection is handled as if no application was listening on that socket.</span></span>

> [!Note]
>
> <span data-ttu-id="8a79d-174">L' \_ \_ option de socket de niveau de protection IPv6 ne place pas nécessairement les restrictions d’accès sur les sockets IPv6 ou ne restreint pas la traversée NAT à l’aide d’une autre méthode que Windows Teredo, ou même en utilisant une autre implémentation de Teredo par un autre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8a79d-174">The IPV6\_PROTECTION\_LEVEL socket option does not necessarily place access restrictions on IPv6 sockets or restrict NAT traversal using some method other than Windows Teredo or even using another implementation of Teredo by another vendor.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8a79d-175">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8a79d-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a79d-176">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="8a79d-176">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="8a79d-177">Réception du trafic sollicité sur Teredo</span><span class="sxs-lookup"><span data-stu-id="8a79d-177">Receiving Solicited Traffic Over Teredo</span></span>](../teredo/receiving-solicited-traffic-over-teredo.md)
</dt> <dt>

[<span data-ttu-id="8a79d-178">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="8a79d-178">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 
