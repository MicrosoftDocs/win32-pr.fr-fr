---
title: Informations d’authentification utilisateur
description: Le service du gestionnaire de connexions d’accès à distance sur l’ordinateur client envoie un nom d’utilisateur et un mot de passe au serveur RAS sur l’ordinateur distant.
ms.assetid: b27bf520-d871-4314-8ed9-3a6a9583ab52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0cb95d0e941c47deb398c03277013e0e0a35f9d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842366"
---
# <a name="user-authentication-information"></a><span data-ttu-id="7601a-103">Informations d’authentification utilisateur</span><span class="sxs-lookup"><span data-stu-id="7601a-103">User Authentication Information</span></span>

<span data-ttu-id="7601a-104">Le service du gestionnaire de connexions d’accès à distance sur l’ordinateur client envoie un nom d’utilisateur et un mot de passe au serveur RAS sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="7601a-104">The Remote Access Connection Manager service on the client computer sends a user name and password to the RAS server on the remote computer.</span></span> <span data-ttu-id="7601a-105">Avant d’établir une connexion, le serveur distant utilise ces informations pour authentifier l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7601a-105">Before it establishes a connection, the remote server uses this information to authenticate the user.</span></span> <span data-ttu-id="7601a-106">Par défaut, le gestionnaire de connexions d’accès à distance envoie le nom d’utilisateur et le mot de passe de l’utilisateur actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="7601a-106">By default, the Remote Access Connection Manager sends the user name and password of the currently logged-on user.</span></span> <span data-ttu-id="7601a-107">Le client RAS peut utiliser la structure [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) spécifiée dans l’appel de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) pour spécifier un nom d’utilisateur et un mot de passe différents.</span><span class="sxs-lookup"><span data-stu-id="7601a-107">The RAS client can use the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure specified in the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call to specify a different user name and password.</span></span>

<span data-ttu-id="7601a-108">Si le serveur distant ne parvient pas à authentifier l’utilisateur avec les informations spécifiées, il peut autoriser l’opération de connexion à passer à l' [état suspendu](paused-states.md) pour permettre au client RAS de collecter différentes données d’authentification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7601a-108">If the remote server cannot authenticate the user with the specified information, it can allow the connection operation to enter a [paused state](paused-states.md) to enable the RAS client to collect different authentication data from the user.</span></span>

 

 