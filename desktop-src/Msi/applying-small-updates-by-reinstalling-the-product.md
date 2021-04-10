---
description: Une petite mise à jour peut être appliquée à une application en réinstallant complètement ou partiellement l’application à partir de la ligne de commande ou d’un programme.
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: Application de petites mises à jour en réinstallant le produit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27b97ff0274baac5a4ec30df244394a609ed525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951780"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a><span data-ttu-id="6b8d3-103">Application de petites mises à jour en réinstallant le produit</span><span class="sxs-lookup"><span data-stu-id="6b8d3-103">Applying Small Updates by Reinstalling the Product</span></span>

<span data-ttu-id="6b8d3-104">Une petite mise à jour peut être appliquée à une application en réinstallant complètement ou partiellement l’application à partir de la ligne de commande ou d’un programme.</span><span class="sxs-lookup"><span data-stu-id="6b8d3-104">A small update can be applied to an application by completely or partially reinstalling the application from the command line or from a program.</span></span>

<span data-ttu-id="6b8d3-105">**Pour propager la petite mise à jour aux utilisateurs actuels (il s’agit d’une réinstallation complète) à partir de la ligne de commande**</span><span class="sxs-lookup"><span data-stu-id="6b8d3-105">**To propagate the small update to current users (this is a complete reinstall) from the command line**</span></span>

1.  <span data-ttu-id="6b8d3-106">À partir de la ligne de commande, utilisez : **msiexec/fvomus \[** _chemin d’accès au fichier. msi mis à jour_ *_\]_* ou **msiexec/i \[** chemin d' _accès à la mise à jour. msi_ *_\] REINSTALL = ALL REINSTALLMODE = vomus_*.</span><span class="sxs-lookup"><span data-stu-id="6b8d3-106">From the command line use either: **msiexec /fvomus \[**_path to updated .msi file_*_\]_* or **msiexec /I \[**_path to updated .msi file_*_\] REINSTALL=ALL REINSTALLMODE=vomus_*.</span></span>
2.  <span data-ttu-id="6b8d3-107">Le fichier. msi mis à jour est mis en cache sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6b8d3-107">The updated .msi file is cached on the user's computer.</span></span> <span data-ttu-id="6b8d3-108">Notez qu’il n’est pas possible pour l’utilisateur de réinstaller le produit à l’aide de la fonction Ajout/suppression de programmes, car le fichier. msi mis à jour n’est pas encore sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6b8d3-108">Note that it is not possible for the user to reinstall the product using Add/Remove Programs because the updated .msi file is not yet on the user's computer.</span></span>

<span data-ttu-id="6b8d3-109">**Pour propager une petite mise à jour à des utilisateurs actuels (il s’agit d’une réinstallation complète) à partir d’un programme**</span><span class="sxs-lookup"><span data-stu-id="6b8d3-109">**To propagate a small update to current users (this is a complete reinstall) from a program**</span></span>

1.  <span data-ttu-id="6b8d3-110">À partir d’un programme, appelez [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) et spécifiez le \_ package REINSTALLMODE, REINSTALLMODE \_ FILEOLDERVERSION, REINSTALLMODE \_ MACHINEDATA, REINSTALLMODE \_ UserData et REINSTALLMODE \_ Shortcut</span><span class="sxs-lookup"><span data-stu-id="6b8d3-110">From a program, call [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) and specify REINSTALLMODE\_PACKAGE, REINSTALLMODE\_FILEOLDERVERSION, REINSTALLMODE\_MACHINEDATA, REINSTALLMODE\_USERDATA, and REINSTALLMODE\_SHORTCUT</span></span>
2.  <span data-ttu-id="6b8d3-111">Le fichier. msi mis à jour est mis en cache sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6b8d3-111">The updated .msi file is cached on the user's computer.</span></span>

<span data-ttu-id="6b8d3-112">La méthode suivante lance une réinstallation des seules fonctionnalités ou composants qui sont affectés par la petite mise à jour.</span><span class="sxs-lookup"><span data-stu-id="6b8d3-112">The following method launches a reinstallation of only those features or components that are affected by the small update.</span></span>

<span data-ttu-id="6b8d3-113">**Pour propager une petite mise à jour aux utilisateurs actuels (il s’agit d’une réinstallation partielle)**</span><span class="sxs-lookup"><span data-stu-id="6b8d3-113">**To propagate a small update to current users (this is a partial reinstall)**</span></span>

1.  <span data-ttu-id="6b8d3-114">Obtenez la liste des noms des fonctionnalités et des composants qui sont affectés par la petite mise à jour.</span><span class="sxs-lookup"><span data-stu-id="6b8d3-114">Obtain a list of the names of features and components that are affected by the small update.</span></span>
2.  <span data-ttu-id="6b8d3-115">À partir de l’invite de commandes, utilisez : **\[ msiexec/i** _chemin d’accès mis à jour. msi_ *_\] REINSTALL = \[_*_Feature List \]_ **REINSTALLMODE = vomus**.</span><span class="sxs-lookup"><span data-stu-id="6b8d3-115">From the command prompt use: **msiexec /I \[**_path to updated .msi file_*_\] REINSTALL=\[_*_Feature list\]_ **REINSTALLMODE=vomus**.</span></span>
3.  <span data-ttu-id="6b8d3-116">Le fichier. msi mis à jour est mis en cache sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6b8d3-116">The updated .msi file is cached on the user's computer.</span></span>

 

 



