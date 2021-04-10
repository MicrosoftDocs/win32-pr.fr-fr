---
title: Publication des services COM+
description: Les services COM fournissent un proxy d’application sous la forme d’un package Windows Installer (MSI).
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Publication des services COM+
- Active Directory, utilisation de, publication d’un service, services COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9044b72b4a604a4d863315963cd097be67f6afce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028596"
---
# <a name="publishing-com-services"></a><span data-ttu-id="00d87-105">Publication des services COM+</span><span class="sxs-lookup"><span data-stu-id="00d87-105">Publishing COM+ Services</span></span>

<span data-ttu-id="00d87-106">Les services COM fournissent un proxy d’application sous la forme d’un package Windows Installer (MSI).</span><span class="sxs-lookup"><span data-stu-id="00d87-106">COM-based services provide an application-proxy in the form of a Windows installer (MSI) package.</span></span> <span data-ttu-id="00d87-107">Ce fichier. msi contient le nom du serveur à utiliser et d’autres éléments requis, tels que les proxy/stubs et les bibliothèques de types requis pour le marshaling.</span><span class="sxs-lookup"><span data-stu-id="00d87-107">This .msi file contains the server name to be used and other required elements, such as proxy/stubs and type libraries required for marshalling.</span></span> <span data-ttu-id="00d87-108">Le composant logiciel enfichable Services de composants génère automatiquement ces proxys d’application pour les applications serveur COM+.</span><span class="sxs-lookup"><span data-stu-id="00d87-108">The Component Services snap-in auto-generate these application proxies for COM+ Server applications.</span></span>

<span data-ttu-id="00d87-109">Les proxys d’application sont publiés dans des objets de stratégie dans Active Directory à l’aide de l’éditeur de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="00d87-109">The application proxies are published into policy objects in Active Directory using the Group Policy Editor.</span></span> <span data-ttu-id="00d87-110">Aucune intervention spéciale n’est nécessaire dans l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="00d87-110">No special intervention is required in the client application.</span></span> <span data-ttu-id="00d87-111">Le compte d’ordinateur/utilisateur sur l’ordinateur client doit se trouver dans une unité d’organisation configurée pour utiliser l’objet de stratégie dans lequel les proxys d’application sont publiés.</span><span class="sxs-lookup"><span data-stu-id="00d87-111">The computer/user account on the client computer must be in an OU configured to use the policy object in which the application proxies are published.</span></span> <span data-ttu-id="00d87-112">Le Binder COM localise automatiquement le serveur au moyen du répertoire lorsque le client établit une instance des objets concernés.</span><span class="sxs-lookup"><span data-stu-id="00d87-112">The COM binder automatically locates the server by means of the directory when the client establishes an instance of the objects concerned.</span></span>

 

 




