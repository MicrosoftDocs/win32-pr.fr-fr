---
description: Lorsque des privilèges élevés ne sont pas nécessaires pour installer un package Windows Installer, l’auteur du package peut supprimer la boîte de dialogue que le contrôle de compte d’utilisateur affiche pour inviter les utilisateurs à autoriser les utilisateurs à effectuer des autorisations d’administrateur.
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: Création de packages sans la boîte de dialogue UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dcd44bf7d2250e12e7cafde46b57978b48cceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756231"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a><span data-ttu-id="27bf1-103">Création de packages sans la boîte de dialogue UAC</span><span class="sxs-lookup"><span data-stu-id="27bf1-103">Authoring Packages without the UAC Dialog Box</span></span>

<span data-ttu-id="27bf1-104">Lorsque des privilèges élevés ne sont pas nécessaires pour installer un package Windows Installer, l’auteur du package peut supprimer la boîte de dialogue que le [*contrôle de compte d’utilisateur*](u-gly.md) affiche pour inviter les utilisateurs à autoriser les utilisateurs à effectuer des autorisations d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="27bf1-104">When elevated privileges are not required to install a Windows Installer package, the author of the package can suppress the dialog box that [*User Account Control*](u-gly.md) (UAC) displays to prompt users for administrator authorization.</span></span>

<span data-ttu-id="27bf1-105">Pour supprimer l’affichage de la boîte de dialogue contrôle de compte d’utilisateur lors de l’installation de l’application, l’auteur du package doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="27bf1-105">To suppress the display of the UAC dialog box when installing the application, the author of the package should do the following:</span></span>

-   <span data-ttu-id="27bf1-106">Installez l’application à l’aide du programme d’installation de Windows 4,0 ou version ultérieure sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="27bf1-106">Install the application using Window Installer 4.0 or later on Windows Vista.</span></span>
-   <span data-ttu-id="27bf1-107">Ne dépendez pas de l’utilisation de privilèges système élevés pour installer l’application sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="27bf1-107">Do not depend on using elevated system privileges to install the application on the computer.</span></span>
-   <span data-ttu-id="27bf1-108">Installez l’application dans le contexte par utilisateur et faites-en le contexte d’installation par défaut du package.</span><span class="sxs-lookup"><span data-stu-id="27bf1-108">Install the application in the per-user context and make this the default installation context of the package.</span></span> <span data-ttu-id="27bf1-109">Si la propriété [**ALLUSERS**](allusers.md) n’est pas définie, le programme d’installation installe le package dans le contexte par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="27bf1-109">If the [**ALLUSERS**](allusers.md) property is not set, the installer installs the package in the per-user context.</span></span> <span data-ttu-id="27bf1-110">Si vous n’incluez pas la propriété **ALLUSERS** dans la [table de propriétés](property-table.md), le programme d’installation ne définit pas cette propriété et, par conséquent, l’installation par utilisateur devient le contexte d’installation par défaut.</span><span class="sxs-lookup"><span data-stu-id="27bf1-110">If you do not include the **ALLUSERS** property in the [Property table](property-table.md), the installer does not set this property and so per-user installation becomes the default installation context.</span></span> <span data-ttu-id="27bf1-111">Vous pouvez remplacer cette valeur par défaut en définissant la propriété **ALLUSERS** sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="27bf1-111">You can override this default by setting the **ALLUSERS** property on the command line.</span></span>
-   <span data-ttu-id="27bf1-112">Définissez le bit 3 dans la propriété [**Résumé du nombre de mots**](word-count-summary.md) pour indiquer que les privilèges élevés ne sont pas nécessaires pour installer l’application.</span><span class="sxs-lookup"><span data-stu-id="27bf1-112">Set Bit 3 in the [**Word Count Summary**](word-count-summary.md) property to indicate that elevated privileges are not required to install the application.</span></span>

 

 



