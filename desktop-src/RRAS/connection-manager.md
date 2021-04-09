---
title: Gestionnaire de connexions
description: Les clients qui envisagent de développer des numéroteurs personnalisés à l’aide de l’API du service d’accès à distance peuvent souhaiter enquêter sur le gestionnaire de connexions Microsoft et le kit d’administration du gestionnaire des connexions.
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7959482542630b6dc90149971df08f7944f83fc
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104030868"
---
# <a name="connection-manager"></a><span data-ttu-id="21c91-103">Gestionnaire de connexions</span><span class="sxs-lookup"><span data-stu-id="21c91-103">Connection Manager</span></span>

<span data-ttu-id="21c91-104">Les clients qui envisagent de développer des numéroteurs personnalisés à l’aide de l’API du service d’accès à distance peuvent souhaiter enquêter sur le gestionnaire de connexions Microsoft et le kit d’administration du gestionnaire des connexions.</span><span class="sxs-lookup"><span data-stu-id="21c91-104">Customers who intend to develop custom dialers using the Remote Access Service API may want to investigate Microsoft Connection Manager and the Connection Manager Administration Kit.</span></span> <span data-ttu-id="21c91-105">Le gestionnaire de connexions est le client d’accès à distance géré de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="21c91-105">Connection Manager is Microsoft's managed remote access client.</span></span> <span data-ttu-id="21c91-106">Il permet à un administrateur de créer un package de configuration d’accès à distance à distribuer aux utilisateurs distants de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="21c91-106">It allows an administrator to build a remote access configuration package to be distributed to the administrator's remote users.</span></span> <span data-ttu-id="21c91-107">Pour plus d’informations sur le gestionnaire de connexions et le kit d’administration du gestionnaire des connexions, consultez l’aide en ligne pour Microsoft Windows 2000 Server et les systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="21c91-107">For more information on Connection Manager and the Connection Manager Administration Kit, see the online help for Microsoft Windows 2000 Server and later operating systems.</span></span>

<span data-ttu-id="21c91-108">Vous pouvez trouver le code source d’un exemple d’action personnalisée du gestionnaire de connexions dans le kit de développement logiciel (SDK) complet de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="21c91-108">You can find the source code for a sample Connection Manager custom action in the complete Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="21c91-109">Le kit de développement logiciel (SDK) de plateforme peut être téléchargé sur le [site Web de Microsoft](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="21c91-109">The Platform SDK can be downloaded at the [Microsoft Web site](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="21c91-110">Après l’installation, le chemin d’accès à l’exemple de code est% install chemin% \\ Microsoft SDK \\ Samples \\ netds \\ RAS \\ ConnectionManager, où% install Path% désigne le répertoire d’installation de base du kit de développement logiciel (SDK) de la plateforme (par exemple, C : \\ Program Files).</span><span class="sxs-lookup"><span data-stu-id="21c91-110">After installation, the path to the sample code is %Install Path%\\Microsoft SDK\\Samples\\netds\\Ras\\ConnectionManager, where %Install Path% designates the base installation directory of the Platform SDK (for example, C:\\Program Files).</span></span>

<span data-ttu-id="21c91-111">Les actions personnalisées permettent au client d’accès à distance d’effectuer des actions spécifiques à différents stades du processus de connexion.</span><span class="sxs-lookup"><span data-stu-id="21c91-111">Custom actions make it possible for the remote access client to take specific actions at various points in the connection process.</span></span> <span data-ttu-id="21c91-112">L’action personnalisée présentée dans l’exemple ajuste automatiquement la configuration du serveur proxy pour une connexion en fonction de l’adresse du serveur de la connexion.</span><span class="sxs-lookup"><span data-stu-id="21c91-112">The custom action demonstrated in the sample automatically adjusts the proxy server configuration for a connection based on the connection's server address.</span></span> <span data-ttu-id="21c91-113">Les clients peuvent utiliser cet exemple comme point de départ pour créer leurs propres actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="21c91-113">Customers can use this sample as a starting point for creating their own custom actions.</span></span>

 

 




