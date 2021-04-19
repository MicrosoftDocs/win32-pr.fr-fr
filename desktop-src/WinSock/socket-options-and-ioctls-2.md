---
description: Certaines options de socket pour Windows Sockets 2 sont résumées dans le tableau suivant.
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: Options de socket et IOCTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472d37bd8d2d97eead66d7c9d2319e57fc5dafde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524354"
---
# <a name="socket-options-and-ioctls"></a><span data-ttu-id="50729-103">Options de socket et IOCTL</span><span class="sxs-lookup"><span data-stu-id="50729-103">Socket Options and IOCTLs</span></span>

<span data-ttu-id="50729-104">Certaines options de socket pour Windows Sockets 2 sont résumées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="50729-104">Some of the socket options for Windows Sockets 2 are summarized in the following table.</span></span> <span data-ttu-id="50729-105">Des informations plus détaillées sont fournies dans la section 4 sous [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) et/ou [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="50729-105">More detailed information is provided in section 4 under [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) and/or [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)).</span></span> <span data-ttu-id="50729-106">Il existe d’autres nouvelles options de socket spécifiques au protocole qui se trouvent dans l’annexe Protocol-Specific.</span><span class="sxs-lookup"><span data-stu-id="50729-106">There are other new protocol-specific socket options which can be found in the Protocol-Specific Annex.</span></span> <span data-ttu-id="50729-107">La liste complète des [**options de socket**](socket-options.md) pour Windows Sockets est disponible dans les informations de référence sur Winsock.</span><span class="sxs-lookup"><span data-stu-id="50729-107">A complete list of [**Socket Options**](socket-options.md) for Windows Sockets are available in the Winsock reference.</span></span>

<span data-ttu-id="50729-108">Pour obtenir un résumé de certains des IOCTL Winsock, consultez [Résumé des OpCodes IOCTL de socket](summary-of-socket-ioctl-opcodes-2.md).</span><span class="sxs-lookup"><span data-stu-id="50729-108">For a a summary of some of the Winsock Ioctls, see [Summary of Socket Ioctl Opcodes](summary-of-socket-ioctl-opcodes-2.md).</span></span> <span data-ttu-id="50729-109">Une liste complète des [**IOCTL Winsock**](winsock-ioctls.md) est disponible dans les informations de référence sur Winsock.</span><span class="sxs-lookup"><span data-stu-id="50729-109">A complete list of [**Winsock IOCTLs**](winsock-ioctls.md) are available in the Winsock reference.</span></span>

## <a name="summary-of-common-socket-options"></a><span data-ttu-id="50729-110">Résumé des options de socket courantes</span><span class="sxs-lookup"><span data-stu-id="50729-110">Summary of Common Socket Options</span></span>

<span data-ttu-id="50729-111">Un fournisseur de services Winsock doit reconnaître toutes ces options et (pour [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) retourner des valeurs plausibles pour chaque.</span><span class="sxs-lookup"><span data-stu-id="50729-111">A Winsock service provider must recognize all of these options, and (for [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) return plausible values for each.</span></span> <span data-ttu-id="50729-112">La valeur par défaut de chaque option est indiquée dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="50729-112">The default value for each option is shown in the following table.</span></span>

<span data-ttu-id="50729-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="50729-113">Value</span></span>

<span data-ttu-id="50729-114">Type</span><span class="sxs-lookup"><span data-stu-id="50729-114">Type</span></span>

<span data-ttu-id="50729-115">Signification</span><span class="sxs-lookup"><span data-stu-id="50729-115">Meaning</span></span>

<span data-ttu-id="50729-116">Default</span><span class="sxs-lookup"><span data-stu-id="50729-116">Default</span></span>

<span data-ttu-id="50729-117">Remarque</span><span class="sxs-lookup"><span data-stu-id="50729-117">Note</span></span>

<span data-ttu-id="50729-118"><span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>\_ACCEPTCONN</span><span class="sxs-lookup"><span data-stu-id="50729-118"><span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>SO\_ACCEPTCONN</span></span>

<span data-ttu-id="50729-119">BOOL</span><span class="sxs-lookup"><span data-stu-id="50729-119">BOOL</span></span>

<span data-ttu-id="50729-120">Le socket est à l’écoute.</span><span class="sxs-lookup"><span data-stu-id="50729-120">Socket is listening.</span></span>

<span data-ttu-id="50729-121">FALSe, sauf si un [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="50729-121">FALSE unless a [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) has been performed.</span></span>

<span data-ttu-id="50729-122"><span id="SO_BROADCAST"></span><span id="so_broadcast"></span>\_diffusion</span><span class="sxs-lookup"><span data-stu-id="50729-122"><span id="SO_BROADCAST"></span><span id="so_broadcast"></span>SO\_BROADCAST</span></span>

<span data-ttu-id="50729-123">BOOL</span><span class="sxs-lookup"><span data-stu-id="50729-123">BOOL</span></span>

<span data-ttu-id="50729-124">Le socket est configuré pour la transmission et la réception des messages de diffusion.</span><span class="sxs-lookup"><span data-stu-id="50729-124">Socket is configured for the transmission and receipt of broadcast messages.</span></span>

<span data-ttu-id="50729-125">FALSE</span><span class="sxs-lookup"><span data-stu-id="50729-125">FALSE</span></span>

<span data-ttu-id="50729-126"><span id="SO_DEBUG"></span><span id="so_debug"></span>\_Déboguer</span><span class="sxs-lookup"><span data-stu-id="50729-126"><span id="SO_DEBUG"></span><span id="so_debug"></span>SO\_DEBUG</span></span>

<span data-ttu-id="50729-127">BOOL</span><span class="sxs-lookup"><span data-stu-id="50729-127">BOOL</span></span>

<span data-ttu-id="50729-128">Le débogage est activé.</span><span class="sxs-lookup"><span data-stu-id="50729-128">Debugging is enabled.</span></span>

<span data-ttu-id="50729-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="50729-129">FALSE</span></span>

<span data-ttu-id="50729-130">cliqu</span><span class="sxs-lookup"><span data-stu-id="50729-130">(i)</span></span>

<span data-ttu-id="50729-131"><span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>\_DONTLINGER</span><span class="sxs-lookup"><span data-stu-id="50729-131"><span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>SO\_DONTLINGER</span></span>

<span data-ttu-id="50729-132">BOOL</span><span class="sxs-lookup"><span data-stu-id="50729-132">BOOL</span></span>

<span data-ttu-id="50729-133">Si la valeur est true, l’option si oui \_ est désactivée.</span><span class="sxs-lookup"><span data-stu-id="50729-133">If true, the SO\_LINGER option is disabled.</span></span>

<span data-ttu-id="50729-134">TRUE</span><span class="sxs-lookup"><span data-stu-id="50729-134">TRUE</span></span>

<span data-ttu-id="50729-135"><span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>\_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="50729-135"><span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>SO\_DONTROUTE</span></span>

<span data-ttu-id="50729-136">BOOL</span><span class="sxs-lookup"><span data-stu-id="50729-136">BOOL</span></span>

<span data-ttu-id="50729-137">Le routage est désactivé.</span><span class="sxs-lookup"><span data-stu-id="50729-137">Routing is disabled.</span></span> <span data-ttu-id="50729-138">Réussit mais est ignoré sur \_ les sockets d’inet AF ; échoue sur \_ les sockets de l’aide de [WSAENOPROTOOPT](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="50729-138">Succeeds but is ignored on AF\_INET sockets; fails on AF\_INET6 sockets with [WSAENOPROTOOPT](windows-sockets-error-codes-2.md).</span></span> <span data-ttu-id="50729-139">Non pris en charge sur les sockets ATM (génère une erreur).</span><span class="sxs-lookup"><span data-stu-id="50729-139">Not supported on ATM sockets (results in an error).</span></span>

<span data-ttu-id="50729-140">FALSE</span><span class="sxs-lookup"><span data-stu-id="50729-140">FALSE</span></span>

<span data-ttu-id="50729-141">cliqu</span><span class="sxs-lookup"><span data-stu-id="50729-141">(i)</span></span>

<span data-ttu-id="50729-142"><span id="SO_ERROR"></span><span id="so_error"></span>\_erreur</span><span class="sxs-lookup"><span data-stu-id="50729-142"><span id="SO_ERROR"></span><span id="so_error"></span>SO\_ERROR</span></span>

<span data-ttu-id="50729-143">int</span><span class="sxs-lookup"><span data-stu-id="50729-143">int</span></span>

<span data-ttu-id="50729-144">Récupère l’état d’erreur et l’efface.</span><span class="sxs-lookup"><span data-stu-id="50729-144">Retrieves error status and clear.</span></span>

<span data-ttu-id="50729-145">0</span><span class="sxs-lookup"><span data-stu-id="50729-145">0</span></span>

<span data-ttu-id="50729-146"><span id="SO_GROUP_ID"></span><span id="so_group_id"></span>\_ID de groupe \_</span><span class="sxs-lookup"><span data-stu-id="50729-146"><span id="SO_GROUP_ID"></span><span id="so_group_id"></span>SO\_GROUP\_ID</span></span>

<span data-ttu-id="50729-147">GROUP</span><span class="sxs-lookup"><span data-stu-id="50729-147">GROUP</span></span>

<span data-ttu-id="50729-148">Réservé.</span><span class="sxs-lookup"><span data-stu-id="50729-148">Reserved.</span></span>

<span data-ttu-id="50729-149">NULL</span><span class="sxs-lookup"><span data-stu-id="50729-149">NULL</span></span>

<span data-ttu-id="50729-150">Récupérer uniquement</span><span class="sxs-lookup"><span data-stu-id="50729-150">Get only</span></span>

<span data-ttu-id="50729-151"><span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>\_priorité de groupe \_</span><span class="sxs-lookup"><span data-stu-id="50729-151"><span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>SO\_GROUP\_PRIORITY</span></span>

<span data-ttu-id="50729-152">int</span><span class="sxs-lookup"><span data-stu-id="50729-152">int</span></span>

<span data-ttu-id="50729-153">Réservé.</span><span class="sxs-lookup"><span data-stu-id="50729-153">Reserved.</span></span>

<span data-ttu-id="50729-154">0</span><span class="sxs-lookup"><span data-stu-id="50729-154">0</span></span>

[<span data-ttu-id="50729-155">**\_KeepAlive**</span><span class="sxs-lookup"><span data-stu-id="50729-155">**SO\_KEEPALIVE**</span></span>](so-keepalive.md)

<span data-ttu-id="50729-156">BOOL</span><span class="sxs-lookup"><span data-stu-id="50729-156">BOOL</span></span>

<span data-ttu-id="50729-157">Les KeepAlive sont envoyées.</span><span class="sxs-lookup"><span data-stu-id="50729-157">Keepalives are being sent.</span></span> <span data-ttu-id="50729-158">Non pris en charge sur les sockets ATM (génère une erreur).</span><span class="sxs-lookup"><span data-stu-id="50729-158">Not supported on ATM sockets (results in an error).</span></span>

<span data-ttu-id="50729-159">FALSE</span><span class="sxs-lookup"><span data-stu-id="50729-159">FALSE</span></span>

<span data-ttu-id="50729-160">cliqu</span><span class="sxs-lookup"><span data-stu-id="50729-160">(i)</span></span>

<span data-ttu-id="50729-161"><span id="SO_LINGER"></span><span id="so_linger"></span>DONC \_</span><span class="sxs-lookup"><span data-stu-id="50729-161"><span id="SO_LINGER"></span><span id="so_linger"></span>SO\_LINGER</span></span>

<span data-ttu-id="50729-162">Lingo de structure</span><span class="sxs-lookup"><span data-stu-id="50729-162">Structure linger</span></span>

<span data-ttu-id="50729-163">Retourne les options de Lingo actuelles.</span><span class="sxs-lookup"><span data-stu-id="50729-163">Returns the current linger options.</span></span>

<span data-ttu-id="50729-164">l \_ microphone est 0</span><span class="sxs-lookup"><span data-stu-id="50729-164">l\_onoff is 0</span></span>

<span data-ttu-id="50729-165"><span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>\_taille maximale des \_ messages \_</span><span class="sxs-lookup"><span data-stu-id="50729-165"><span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>SO\_MAX\_MSG\_SIZE</span></span>

<span data-ttu-id="50729-166">int</span><span class="sxs-lookup"><span data-stu-id="50729-166">int</span></span>

<span data-ttu-id="50729-167">Taille maximale sortante d’un message pour les types de sockets de message.</span><span class="sxs-lookup"><span data-stu-id="50729-167">Maximum outbound size of a message for message socket types.</span></span> <span data-ttu-id="50729-168">Il n’existe aucune provision pour déterminer la taille maximale du message entrant.</span><span class="sxs-lookup"><span data-stu-id="50729-168">There is no provision to determine the maximum inbound message size.</span></span> <span data-ttu-id="50729-169">N’a aucune signification pour les sockets orientés flux.</span><span class="sxs-lookup"><span data-stu-id="50729-169">Has no meaning for stream-oriented sockets.</span></span>

<span data-ttu-id="50729-170">Dépend de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="50729-170">Implementation dependent</span></span>

<span data-ttu-id="50729-171">Récupérer uniquement</span><span class="sxs-lookup"><span data-stu-id="50729-171">Get only</span></span>

<span data-ttu-id="50729-172"><span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>\_OOBINLINE</span><span class="sxs-lookup"><span data-stu-id="50729-172"><span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>SO\_OOBINLINE</span></span>

<span data-ttu-id="50729-173">BOOL</span><span class="sxs-lookup"><span data-stu-id="50729-173">BOOL</span></span>

<span data-ttu-id="50729-174">Les données OOB sont reçues dans le flux de données normal.</span><span class="sxs-lookup"><span data-stu-id="50729-174">OOB data is being received in the normal data stream.</span></span>

<span data-ttu-id="50729-175">FALSE</span><span class="sxs-lookup"><span data-stu-id="50729-175">FALSE</span></span>

<span data-ttu-id="50729-176"><span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>\_INFOW de protocole \_</span><span class="sxs-lookup"><span data-stu-id="50729-176"><span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>SO\_PROTOCOL\_INFOW</span></span>

<span data-ttu-id="50729-177">[ **\_ informations sur** la structure WSAPROTOCOL](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)</span><span class="sxs-lookup"><span data-stu-id="50729-177">structure [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)</span></span>

<span data-ttu-id="50729-178">Description des informations de protocole pour le protocole qui est lié à ce Socket.</span><span class="sxs-lookup"><span data-stu-id="50729-178">Description of protocol information for the protocol that is bound to this socket.</span></span>

<span data-ttu-id="50729-179">Dépendant du protocole</span><span class="sxs-lookup"><span data-stu-id="50729-179">Protocol dependent</span></span>

<span data-ttu-id="50729-180">Récupérer uniquement</span><span class="sxs-lookup"><span data-stu-id="50729-180">Get only</span></span>

<span data-ttu-id="50729-181"><span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>\_RCVBUF</span><span class="sxs-lookup"><span data-stu-id="50729-181"><span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>SO\_RCVBUF</span></span>

<span data-ttu-id="50729-182">int</span><span class="sxs-lookup"><span data-stu-id="50729-182">int</span></span>

<span data-ttu-id="50729-183">Espace de la mémoire tampon par socket total réservé aux réceptions.</span><span class="sxs-lookup"><span data-stu-id="50729-183">The total per-socket buffer space reserved for receives.</span></span> <span data-ttu-id="50729-184">Cela n’est pas lié à \_ \_ \_ la taille de message maximale et ne correspond pas nécessairement à la taille de la fenêtre de réception TCP.</span><span class="sxs-lookup"><span data-stu-id="50729-184">This is unrelated to SO\_MAX\_MSG\_SIZE and does not necessarily correspond to the size of the TCP receive window.</span></span>

<span data-ttu-id="50729-185">Dépend de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="50729-185">Implementation dependent</span></span>

<span data-ttu-id="50729-186">cliqu</span><span class="sxs-lookup"><span data-stu-id="50729-186">(i)</span></span>

<span data-ttu-id="50729-187"><span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>\_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="50729-187"><span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>SO\_REUSEADDR</span></span>

<span data-ttu-id="50729-188">BOOL</span><span class="sxs-lookup"><span data-stu-id="50729-188">BOOL</span></span>

<span data-ttu-id="50729-189">L’adresse à laquelle ce Socket est lié peut être utilisée par d’autres.</span><span class="sxs-lookup"><span data-stu-id="50729-189">The address to which this socket is bound can be used by others.</span></span> <span data-ttu-id="50729-190">Non applicable sur les sockets ATM.</span><span class="sxs-lookup"><span data-stu-id="50729-190">Not applicable on ATM sockets.</span></span>

<span data-ttu-id="50729-191">FALSE</span><span class="sxs-lookup"><span data-stu-id="50729-191">FALSE</span></span>

<span data-ttu-id="50729-192"><span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>\_SNDBUF</span><span class="sxs-lookup"><span data-stu-id="50729-192"><span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>SO\_SNDBUF</span></span>

<span data-ttu-id="50729-193">int</span><span class="sxs-lookup"><span data-stu-id="50729-193">int</span></span>

<span data-ttu-id="50729-194">Espace de mémoire tampon par socket total réservé aux envois.</span><span class="sxs-lookup"><span data-stu-id="50729-194">The total per-socket buffer space reserved for sends.</span></span> <span data-ttu-id="50729-195">Cela n’est pas lié à \_ \_ \_ la taille de message maximale et ne correspond pas nécessairement à la taille d’une fenêtre d’envoi TCP.</span><span class="sxs-lookup"><span data-stu-id="50729-195">This is unrelated to SO\_MAX\_MSG\_SIZE and does not necessarily correspond to the size of a TCP send window.</span></span>

<span data-ttu-id="50729-196">Dépend de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="50729-196">Implementation dependent</span></span>

<span data-ttu-id="50729-197">cliqu</span><span class="sxs-lookup"><span data-stu-id="50729-197">(i)</span></span>

<span data-ttu-id="50729-198"><span id="SO_TYPE"></span><span id="so_type"></span>\_type</span><span class="sxs-lookup"><span data-stu-id="50729-198"><span id="SO_TYPE"></span><span id="so_type"></span>SO\_TYPE</span></span>

<span data-ttu-id="50729-199">int</span><span class="sxs-lookup"><span data-stu-id="50729-199">int</span></span>

<span data-ttu-id="50729-200">Type du socket (par exemple, flux de chaussette \_ ).</span><span class="sxs-lookup"><span data-stu-id="50729-200">The type of the socket (for example, SOCK\_STREAM).</span></span>

<span data-ttu-id="50729-201">Tel qu’il a été créé via le Socket.</span><span class="sxs-lookup"><span data-stu-id="50729-201">As created through socket.</span></span>

<span data-ttu-id="50729-202"><span id="PVD_CONFIG"></span><span id="pvd_config"></span>configuration de PVD \_</span><span class="sxs-lookup"><span data-stu-id="50729-202"><span id="PVD_CONFIG"></span><span id="pvd_config"></span>PVD\_CONFIG</span></span>

<span data-ttu-id="50729-203">caractère FAR \*</span><span class="sxs-lookup"><span data-stu-id="50729-203">char FAR \*</span></span>

<span data-ttu-id="50729-204">Objet de structure de données opaque contenant les informations de configuration du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="50729-204">An opaque data structure object containing configuration information of the service provider.</span></span>

<span data-ttu-id="50729-205">Dépend de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="50729-205">Implementation dependent</span></span>

<span data-ttu-id="50729-206"><span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP- \_ délai</span><span class="sxs-lookup"><span data-stu-id="50729-206"><span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP\_NODELAY</span></span>

<span data-ttu-id="50729-207">BOOL</span><span class="sxs-lookup"><span data-stu-id="50729-207">BOOL</span></span>

<span data-ttu-id="50729-208">Désactive l'algorithme Nagle pour la fusion des envois.</span><span class="sxs-lookup"><span data-stu-id="50729-208">Disables the Nagle algorithm for send coalescing.</span></span>

<span data-ttu-id="50729-209">Dépend de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="50729-209">Implementation dependent</span></span>

<span data-ttu-id="50729-210">(i) un fournisseur de services peut ignorer cette option en mode silencieux sur [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) et retourner une valeur constante pour [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), ou il peut accepter une valeur pour **WSPSetSockOpt** et retourner la valeur correspondante dans **WSPGetSockOpt** sans utiliser la valeur de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="50729-210">(i) A service provider may silently ignore this option on [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) and return a constant value for [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), or it may accept a value for **WSPSetSockOpt** and return the corresponding value in **WSPGetSockOpt** without using the value in any way.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="50729-211">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50729-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50729-212">**Options de socket**</span><span class="sxs-lookup"><span data-stu-id="50729-212">**Socket Options**</span></span>](socket-options.md)
</dt> <dt>

[<span data-ttu-id="50729-213">**Options de socket de socket SOL \_**</span><span class="sxs-lookup"><span data-stu-id="50729-213">**SOL\_SOCKET Socket Options**</span></span>](sol-socket-socket-options.md)
</dt> <dt>

[<span data-ttu-id="50729-214">**\_Options de socket TCP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="50729-214">**IPPROTO\_TCP Socket Options**</span></span>](ipproto-tcp-socket-options.md)
</dt> <dt>

[<span data-ttu-id="50729-215">**\_Options de socket UDP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="50729-215">**IPPROTO\_UDP Socket Options**</span></span>](ipproto-udp-socket-options.md)
</dt> <dt>

[<span data-ttu-id="50729-216">**IOCTL Winsock**</span><span class="sxs-lookup"><span data-stu-id="50729-216">**Winsock IOCTLs**</span></span>](winsock-ioctls.md)
</dt> </dl>

 

 
