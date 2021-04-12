---
title: Installation et configuration des applications RPC
description: Lorsque le système d’exploitation Microsoft Windows est installé sur un serveur ou un client, le programme d’installation installe automatiquement les fichiers d’exécution RPC.
ms.assetid: cfcada3d-cf7c-42a9-9ed4-0b1bba7a98cf
keywords:
- Appel de procédure distante RPC, tâches, installation et configuration d’applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90837261c571276a74bb3a5354c7b9a5db2da6cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462466"
---
# <a name="installing-and-configuring-rpc-applications"></a><span data-ttu-id="377bd-104">Installation et configuration des applications RPC</span><span class="sxs-lookup"><span data-stu-id="377bd-104">Installing and Configuring RPC Applications</span></span>

<span data-ttu-id="377bd-105">Lorsque le système d’exploitation Microsoft Windows est installé sur un serveur ou un client, le programme d’installation installe automatiquement les fichiers d’exécution RPC.</span><span class="sxs-lookup"><span data-stu-id="377bd-105">When the Microsoft Windows operating system is installed on a server or client, setup automatically installs the RPC run-time files.</span></span> <span data-ttu-id="377bd-106">Aucune autre installation RPC n’est requise.</span><span class="sxs-lookup"><span data-stu-id="377bd-106">No further RPC installation is required.</span></span> <span data-ttu-id="377bd-107">Toutefois, vous devez vous assurer que la version de Windows que vous installez prend en charge toutes les fonctionnalités utilisées dans votre application distribuée.</span><span class="sxs-lookup"><span data-stu-id="377bd-107">You must ensure, however, that the version of Windows you install supports all the features used in your distributed application.</span></span>

<span data-ttu-id="377bd-108">Lorsque vous utilisez une application RPC sur un système d’exploitation Windows 3. x ou Microsoft MS-DOS, vous devez copier les fichiers exécutables du runtime RPC sur les ordinateurs Windows 3. x ou MS-DOS qui utiliseront l’application.</span><span class="sxs-lookup"><span data-stu-id="377bd-108">When you use an RPC application on a Windows 3.x or Microsoft MS-DOS operating system, you must copy the RPC run-time executable files to the Windows 3.x or MS-DOS computers that will be using the application.</span></span> <span data-ttu-id="377bd-109">Le répertoire \\ mstools \\ RPC \_ RT16 sur le CD du kit de développement logiciel (SDK) de la plateforme contient une image disque de ces fichiers, ainsi qu’un programme d’installation pour installer les fichiers.</span><span class="sxs-lookup"><span data-stu-id="377bd-109">The directory \\mstools\\rpc\_rt16 on the Platform Software Development Kit (SDK) CD contains a disk image of these files along with a setup program to install the files.</span></span> <span data-ttu-id="377bd-110">Utilisez cette image disque pour créer un disque d’installation à distribuer avec votre application RPC.</span><span class="sxs-lookup"><span data-stu-id="377bd-110">Use this disk image to create an install disk for distribution with your RPC application.</span></span> <span data-ttu-id="377bd-111">Vous pouvez également utiliser des applications clientes 16 bits ciblées vers MS-DOS ou Windows sur un système d’exploitation Windows 32 bits/64 bits.</span><span class="sxs-lookup"><span data-stu-id="377bd-111">You can also use 16-bit client applications targeted toward MS-DOS or Windows on a 32-bit/64-bit Windows operating system.</span></span> <span data-ttu-id="377bd-112">Toutefois, le programme d’installation de votre application doit installer les fichiers exécutables contenus dans cette image disque.</span><span class="sxs-lookup"><span data-stu-id="377bd-112">However, your application's installation program must install the executable files contained in this disk image.</span></span>

<span data-ttu-id="377bd-113">Lorsque vous générez une application RPC pour un client Macintosh, vous devez lier les fichiers nécessaires à l’application au moment de la génération.</span><span class="sxs-lookup"><span data-stu-id="377bd-113">When you build an RPC application for a Macintosh client, you must link the necessary files to the application at build time.</span></span> <span data-ttu-id="377bd-114">Aucune installation RPC supplémentaire n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="377bd-114">No additional RPC installation is needed.</span></span>

<span data-ttu-id="377bd-115">Pour plus d’informations sur les fichiers redistribuables et les contrats de licence, consultez \\Redist.txt de licence \\ et \\ \\License.txt de licence sur le CD de Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="377bd-115">For more details about redistributable files and licensing agreements, see \\LICENSE\\Redist.txt and \\LICENSE\\License.txt on the Platform SDK CD.</span></span>

<span data-ttu-id="377bd-116">Cette section contient des informations sur la configuration d’applications RPC sur une variété de plateformes matérielles et logicielles.</span><span class="sxs-lookup"><span data-stu-id="377bd-116">This section contains information about setting up RPC applications on a variety of hardware and software platforms.</span></span> <span data-ttu-id="377bd-117">Il présente la discussion dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="377bd-117">It presents the discussion in the following sections:</span></span>

-   [<span data-ttu-id="377bd-118">Configuration du fournisseur de services de noms</span><span class="sxs-lookup"><span data-stu-id="377bd-118">Configuring the Name Service Provider</span></span>](configuring-the-name-service-provider.md)
-   [<span data-ttu-id="377bd-119">Informations de Registre</span><span class="sxs-lookup"><span data-stu-id="377bd-119">Registry Information</span></span>](registry-information.md)
-   [<span data-ttu-id="377bd-120">Utilisation de RPC avec le proxy Winsock</span><span class="sxs-lookup"><span data-stu-id="377bd-120">Using RPC with Winsock Proxy</span></span>](using-rpc-with-winsock-proxy.md)
-   [<span data-ttu-id="377bd-121">Installation de SPX/IPX</span><span class="sxs-lookup"><span data-stu-id="377bd-121">SPX/IPX Installation</span></span>](spx-ipx-installation.md)
-   [<span data-ttu-id="377bd-122">Configuration du serveur de sécurité</span><span class="sxs-lookup"><span data-stu-id="377bd-122">Configuring the Security Server</span></span>](configuring-the-security-server.md)

 

 




