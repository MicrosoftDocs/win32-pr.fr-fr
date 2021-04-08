---
description: Pour supprimer une application qui a été installée dans l’État publié, désinstallez-la simplement à l’aide de MsiInstallProduct ou MsiConfigureProduct. Vous pouvez également supprimer une application publiée à partir de la ligne de commande. Consultez Options de ligne de commande.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Suppression d’une application publiée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e8aba31dfd1538afc5585ada41b193c642950a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866077"
---
# <a name="removing-an-advertised-application"></a><span data-ttu-id="a3974-105">Suppression d’une application publiée</span><span class="sxs-lookup"><span data-stu-id="a3974-105">Removing an Advertised Application</span></span>

<span data-ttu-id="a3974-106">Pour supprimer une application qui a été installée dans l’État publié, désinstallez-la simplement à l’aide de [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) ou [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta).</span><span class="sxs-lookup"><span data-stu-id="a3974-106">To remove an application that has been installed in the advertised state, simply uninstall it using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) or [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta).</span></span> <span data-ttu-id="a3974-107">Vous pouvez également supprimer une application publiée à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="a3974-107">You can also remove an advertised application from the command line.</span></span> <span data-ttu-id="a3974-108">Consultez [options de ligne de commande](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="a3974-108">See [Command Line Options](command-line-options.md).</span></span>

<span data-ttu-id="a3974-109">Notez que vous ne pouvez pas supprimer une application publiée si vous avez créé le package de façon à ce que l’exécution d’une installation soit conditionnée par l’instruction **non installée**.</span><span class="sxs-lookup"><span data-stu-id="a3974-109">Note that you may be unable to remove an advertised application if you have authored the package in such a way that running an installation is conditional upon the statement **NOT Installed**.</span></span> <span data-ttu-id="a3974-110">Une application publiée n’est pas installée sur l’ordinateur de l’utilisateur et le programme d’installation ne définit pas la propriété [**installed**](installed.md) .</span><span class="sxs-lookup"><span data-stu-id="a3974-110">An advertised application is not installed on the user's computer and the installer does not set the [**Installed**](installed.md) Property.</span></span> <span data-ttu-id="a3974-111">Le package doit être créé afin que les applications publiées puissent être désinstallées.</span><span class="sxs-lookup"><span data-stu-id="a3974-111">The package must be authored so that advertised applications can be uninstalled.</span></span>

 

 



