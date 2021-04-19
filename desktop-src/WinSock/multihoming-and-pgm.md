---
description: Une attention particulière doit être accordée aux expéditeurs ou aux destinataires PGM multirésidents. Cette page décrit les considérations et fournit des instructions pour les meilleures pratiques de programmation.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Hébergement multiple et PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142527c7fdf3e5d34d80c51e4002bc21ad47691c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516871"
---
# <a name="multihoming-and-pgm"></a><span data-ttu-id="3bbe0-104">Hébergement multiple et PGM</span><span class="sxs-lookup"><span data-stu-id="3bbe0-104">Multihoming and PGM</span></span>

<span data-ttu-id="3bbe0-105">Une attention particulière doit être accordée aux expéditeurs ou aux destinataires PGM multirésidents.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-105">Special consideration must be given to multihomed PGM senders or receivers.</span></span> <span data-ttu-id="3bbe0-106">Cette page décrit les considérations et fournit des instructions pour les meilleures pratiques de programmation.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-106">This page describes the considerations, and provides guidelines for best programming practices.</span></span>

## <a name="multihomed-pgm-sender"></a><span data-ttu-id="3bbe0-107">Expéditeur PGM multirésident</span><span class="sxs-lookup"><span data-stu-id="3bbe0-107">Multihomed PGM Sender</span></span>

<span data-ttu-id="3bbe0-108">Quand une application ne parvient pas à spécifier une interface lors de l’appel de la fonction [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , la première interface disponible est utilisée.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-108">When an application fails to specify an interface upon calling the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function, the first available interface is used.</span></span> <span data-ttu-id="3bbe0-109">Si aucune interface n’est disponible, la **connexion** échoue.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-109">If no interface is available, **connect** fails.</span></span>

<span data-ttu-id="3bbe0-110">Lorsqu’une application spécifie une interface à l’aide de l’option [RM \_ Set \_ Send \_ If](socket-options.md) Socket, une tentative de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) est effectuée implicitement vers cette interface à l’aide du protocole TCP/IP, et échoue si le protocole TCP/IP échoue à la demande de liaison.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-110">When an application specifies an interface using the [RM\_SET\_SEND\_IF](socket-options.md) socket option, a [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) attempt is made implicitly to that interface using TCP/IP, and fails if TCP/IP fails the bind request.</span></span> <span data-ttu-id="3bbe0-111">Si l’interface est définie à l’aide de RM \_ Set Send s’il y a \_ \_ plusieurs fois, seul le dernier ensemble d’interfaces est applicable.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-111">If the interface is set using RM\_SET\_SEND\_IF multiple times, only the last interface set successfully is applicable.</span></span>

<span data-ttu-id="3bbe0-112">Windows Sockets gère l’interface définie et, si cette interface disparaît, la session est déconnectée.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-112">Windows Sockets maintains which interface is set, and if that interface disappears, the session is disconnected.</span></span>

## <a name="multihomed-pgm-receiver"></a><span data-ttu-id="3bbe0-113">Récepteur PGM multirésident</span><span class="sxs-lookup"><span data-stu-id="3bbe0-113">Multihomed PGM Receiver</span></span>

<span data-ttu-id="3bbe0-114">Quand une application ne parvient pas à spécifier une interface lors de l’appel de la fonction [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , l’interface par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-114">When an application fails to specify an interface upon calling the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function, the default interface is used.</span></span> <span data-ttu-id="3bbe0-115">Si aucune interface n’est disponible, la [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) échoue.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-115">If no interface is available, [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) fails.</span></span>

<span data-ttu-id="3bbe0-116">Lorsqu’une application spécifie une ou plusieurs interfaces sur lesquelles écouter, à l’aide de [RM \_ Add \_ Receive \_ si](socket-options.md), Windows Sockets tente de se lier à l’interface ou aux interfaces demandées à l’aide de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-116">When an application specifies one or more interfaces on which to listen, using [RM\_ADD\_RECEIVE\_IF](socket-options.md), Windows Sockets attempts to bind to the requested interface or interfaces using TCP/IP.</span></span> <span data-ttu-id="3bbe0-117">Toute erreur de TCP/IP entraîne l’échec de cette requête.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-117">Any error from TCP/IP causes this request to fail.</span></span> <span data-ttu-id="3bbe0-118">Contrairement au cas de l’expéditeur PGM, l’ajout de plusieurs fois à une interface de réception entraîne la publication de l’écoute sur toutes les interfaces ajoutées avec succès.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-118">Unlike the PGM sender case, adding a receive interface multiple times result in the listens being posted on all the successfully added interfaces.</span></span> <span data-ttu-id="3bbe0-119">Utilisez l' \_ \_ option recevoir si le socket RM del \_ pour arrêter l’écoute sur une interface.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-119">Use the RM\_DEL\_RECEIVE\_IF socket option to stop listening on an interface.</span></span>

<span data-ttu-id="3bbe0-120">Windows Sockets ne conserve pas l’État sur plusieurs interfaces d’écoute spécifiées et s’appuie plutôt sur le protocole TCP/IP pour le faire.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-120">Windows Sockets does not maintain state about multiple specified listening interfaces, and instead relies on TCP/IP to do so.</span></span> <span data-ttu-id="3bbe0-121">Toutefois, une fois qu’une session est en cours, les sockets Windows effectuent le suivi de l’interface entrante pour cette session et, si cette interface disparaît, Windows Sockets déconnecte la session.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-121">Once a session is in progress, however, Windows Sockets track the incoming interface for that session, and if that interface disappears, Windows Sockets disconnects the session.</span></span>

 

 



