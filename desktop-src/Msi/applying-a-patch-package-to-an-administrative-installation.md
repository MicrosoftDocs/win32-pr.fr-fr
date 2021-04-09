---
description: Vous pouvez appliquer la petite mise à jour à une image source d’administration de MNP2000.msi en installant l’exemple de correctif MNP2000. msp créé lors de la génération d’un package de correctifs.
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: Application d’un package de correctifs à une installation d’administration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e0645bdd2c472e725a3a5eeef22693aa35b8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951784"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a><span data-ttu-id="fedf6-103">Application d’un package de correctifs à une installation d’administration</span><span class="sxs-lookup"><span data-stu-id="fedf6-103">Applying a Patch Package to an Administrative Installation</span></span>

<span data-ttu-id="fedf6-104">Vous pouvez appliquer la petite mise à jour à une image source d’administration de MNP2000.msi en installant l’exemple de correctif MNP2000. msp créé lors de la [génération d’un package de correctifs](generating-a-patch-package.md).</span><span class="sxs-lookup"><span data-stu-id="fedf6-104">You may apply the small update to an administrative source image of MNP2000.msi by installing the sample patch MNP2000.msp created in [Generating a Patch Package](generating-a-patch-package.md).</span></span> <span data-ttu-id="fedf6-105">La mise à jour peut ensuite être propagée aux utilisateurs en demandant qu’ils réinstallent l’application à partir de la nouvelle image source d’administration.</span><span class="sxs-lookup"><span data-stu-id="fedf6-105">The update can then be propagated to users by requesting that they reinstall the application from the new administrative source image.</span></span>

<span data-ttu-id="fedf6-106">Un administrateur peut utiliser la ligne de commande suivante pour mettre à jour l’image source administrative située dans//Server/MNP2000.msi vers une nouvelle image source qui est la même que celle produite par une installation d’administration à partir d’un CD-ROM entièrement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="fedf6-106">An administrator can use the following command line to update the administrative source image located at //server/MNP2000.msi to a new source image that is the same as would be produced by an administrative installation from a fully updated CD-ROM.</span></span>

<span data-ttu-id="fedf6-107">**msiexec/a//Server/MNP2000.msi/p MNP2000. msp**</span><span class="sxs-lookup"><span data-stu-id="fedf6-107">**msiexec /a //server/MNP2000.msi /p MNP2000.msp**</span></span>

<span data-ttu-id="fedf6-108">Les membres du groupe de travail utilisant MNP2000 doivent ensuite réinstaller l’application à partir de la nouvelle image source d’administration pour recevoir la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="fedf6-108">Members of the workgroup using MNP2000 then must reinstall the application from the new administrative source image to receive the update.</span></span>

<span data-ttu-id="fedf6-109">Pour réinstaller complètement les applications et mettre en cache le fichier. msi mis à jour sur l’ordinateur de l’utilisateur, les utilisateurs peuvent entrer l’une ou l’autre des commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="fedf6-109">To completely reinstall the applications and cache the updated .msi file on the user's computer, users may enter either of the following commands.</span></span>

<span data-ttu-id="fedf6-110">**msiexec/fvomus//Server/MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="fedf6-110">**msiexec /fvomus //server/MNP2000.msi**</span></span>

<span data-ttu-id="fedf6-111">**msiexec/I//Server/MNP2000.msi REINSTALL = ALL REINSTALLMODE = vomus**</span><span class="sxs-lookup"><span data-stu-id="fedf6-111">**msiexec /I //server/MNP2000.msi REINSTALL=ALL REINSTALLMODE=vomus**</span></span>

<span data-ttu-id="fedf6-112">Pour réinstaller uniquement la fonctionnalité de concert mise à jour et mettre en cache le fichier. msi mis à jour sur l’ordinateur de l’utilisateur, les utilisateurs peuvent entrer la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="fedf6-112">To reinstall only the updated Concert feature and cache the updated .msi file on the user's computer, users may enter the following command.</span></span>

<span data-ttu-id="fedf6-113">**msiexec/I//Server/MNP2000.msi REINSTALL = concert REINSTALLMODE = vomus**</span><span class="sxs-lookup"><span data-stu-id="fedf6-113">**msiexec /I //server/MNP2000.msi REINSTALL=Concert REINSTALLMODE=vomus**</span></span>

## <a name="next-example"></a><span data-ttu-id="fedf6-114">Exemple suivant</span><span class="sxs-lookup"><span data-stu-id="fedf6-114">Next example</span></span>

[<span data-ttu-id="fedf6-115">Exemple de localisation</span><span class="sxs-lookup"><span data-stu-id="fedf6-115">A Localization Example</span></span>](a-localization-example.md)

 

 



