---
title: Authentification utilisateur
description: Le protocole d’authentification lui-même peut authentifier l’utilisateur via PEAP (Protected EAP).
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10de1d08a0daffe7fb415c3eab4ba939afa9387
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103679246"
---
# <a name="user-authentication"></a><span data-ttu-id="3623c-103">Authentification utilisateur</span><span class="sxs-lookup"><span data-stu-id="3623c-103">User Authentication</span></span>

<span data-ttu-id="3623c-104">Le protocole d’authentification lui-même peut authentifier l’utilisateur via PEAP (Protected EAP).</span><span class="sxs-lookup"><span data-stu-id="3623c-104">The authentication protocol itself can authenticate the user via Protected EAP (PEAP).</span></span> <span data-ttu-id="3623c-105">Il existe également deux fournisseurs d’authentification intégrés au système d’exploitation : l’authentification de domaine Windows (accessible via les services d’annuaire) et le service RADIUS (Remote Access Dial-in User Service).</span><span class="sxs-lookup"><span data-stu-id="3623c-105">There are also two authentication providers built into the operating system: Windows domain authentication (accessed via Directory Services) and Remote Access Dial-In User Service (RADIUS).</span></span>

<span data-ttu-id="3623c-106">Dans le cas où RADIUS est le fournisseur d’authentification, le plug-in EAP est installé sur le serveur RADIUS plutôt que sur le serveur de point d’accès sans fil (AP), tel qu’un serveur RAS.</span><span class="sxs-lookup"><span data-stu-id="3623c-106">In the case where RADIUS is the authentication provider, the EAP Plug-in is installed on the RADIUS server rather than on the wireless Access Point (AP) server, such as a RAS server.</span></span> <span data-ttu-id="3623c-107">Le serveur AP transmet les paquets EAP directement du client au service d’authentification sur le serveur RADIUS.</span><span class="sxs-lookup"><span data-stu-id="3623c-107">The AP server passes EAP packets directly from the client to the authentication service on the RADIUS server.</span></span> <span data-ttu-id="3623c-108">Le serveur AP ne traite aucune des informations contenues dans les paquets EAP, mais il doit accepter les clés de chiffrement générées PEAP côté serveur, à pleine puissance (256 bits) pour créer la connexion sécurisée.</span><span class="sxs-lookup"><span data-stu-id="3623c-108">The AP server does not process any of the information in the EAP packets, but it must accept the server-side, full strength (256 bit) PEAP generated encryption keys in order to create the secure connection.</span></span>

 

 




