---
title: Connexion automatique RAS
description: Une fonctionnalité appelée \ 0034 ; connexion par défaut \ 0034 ; a été ajouté au système dans Windows XP.
ms.assetid: 8ef832ed-97e4-4941-adb2-b35ce3a75fd1
keywords:
- Numérotation automatique, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc2da449b91dd34165038b8d9f07b73926a943a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106543406"
---
# <a name="ras-autodial"></a><span data-ttu-id="6f070-104">Connexion automatique RAS</span><span class="sxs-lookup"><span data-stu-id="6f070-104">RAS AutoDial</span></span>

<span data-ttu-id="6f070-105">Une fonctionnalité appelée « connexion par défaut » a été ajoutée au système dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6f070-105">A feature called "default connection" was added to the system in Windows XP.</span></span> <span data-ttu-id="6f070-106">En cas d’échec de tentative de connexion, le système recherche une correspondance explicite (pour le nom Winsock ou le nom de partage) dans la base de données si ce n’est pas le cas, il compose la connexion par défaut, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="6f070-106">If there is a failed connection attempt, the system checks for an explicit match (for Winsock name or share name) in the database if not, it dials the default connection if there is one.</span></span>

<span data-ttu-id="6f070-107">**Windows 2000 :** Lorsqu’une tentative de connexion à une adresse réseau échoue parce que l’ordinateur hôte est inaccessible, la fonctionnalité de numérotation automatique peut démarrer automatiquement une opération de connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="6f070-107">**Windows 2000:** When an attempt to connect to a network address fails because the host cannot be reached, the AutoDial feature can automatically start a dial-up connection operation.</span></span> <span data-ttu-id="6f070-108">Pour ce faire, AutoDial effectue une recherche dans sa base de données d’adresses réseau afin de trouver une entrée de l’annuaire téléphonique qu’il peut utiliser pour établir la connexion.</span><span class="sxs-lookup"><span data-stu-id="6f070-108">To do this, AutoDial searches its database of network addresses to find a phone-book entry that it can use to establish the connection.</span></span>

<span data-ttu-id="6f070-109">**Windows NT 4,0 :  ** RAS conserve une base de données des noms Winsock et/ou des noms de partage que vous avez atteints avec succès alors qu’une connexion RAS/VPN était active.</span><span class="sxs-lookup"><span data-stu-id="6f070-109">**Windows NT 4.0:  ** RAS keeps a database of the Winsock names and/or share names that you have successfully reached while a RAS/VPN connection was active.</span></span> <span data-ttu-id="6f070-110">Plus tard, en cas d’échec d’une tentative de connexion Winsock ou de partage, le système vérifie cette base de données et offre à la fois la connexion stockée.</span><span class="sxs-lookup"><span data-stu-id="6f070-110">Later, when a winsock or share connection attempt fails, the system checks this database and offers to dial the stored connection for you.</span></span>

 

 




