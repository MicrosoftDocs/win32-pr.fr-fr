---
description: Les auteurs des packages d’installation peuvent spécifier que le programme d’installation copie les fichiers partagés (les dll communément partagés) d’une application dans le dossier de l’application plutôt que dans un emplacement partagé.
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: Composants isolés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f29f614dfd819e093c5729a9a97a076247d281d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750117"
---
# <a name="isolated-components"></a><span data-ttu-id="5dc70-103">Composants isolés</span><span class="sxs-lookup"><span data-stu-id="5dc70-103">Isolated Components</span></span>

<span data-ttu-id="5dc70-104">Les auteurs des packages d’installation peuvent spécifier que le programme d’installation copie les fichiers partagés (les dll communément partagés) d’une application dans le dossier de l’application plutôt que dans un emplacement partagé.</span><span class="sxs-lookup"><span data-stu-id="5dc70-104">Authors of installation packages can specify that the installer copy the shared files (commonly shared DLLs) of an application into that application's folder rather than to a shared location.</span></span> <span data-ttu-id="5dc70-105">Ce jeu de fichiers (dll) privé est ensuite utilisé uniquement par l’application.</span><span class="sxs-lookup"><span data-stu-id="5dc70-105">This private set of files (DLLs) are then used only by the application.</span></span> <span data-ttu-id="5dc70-106">L’isolation de l’application avec ses composants partagés de cette manière présente les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="5dc70-106">Isolating the application together with its shared components in this manner has the following advantages:</span></span>

-   <span data-ttu-id="5dc70-107">L’application utilise toujours les versions des fichiers partagés avec lesquels elle a été déployée.</span><span class="sxs-lookup"><span data-stu-id="5dc70-107">The application always uses the versions of the shared files with which it was deployed.</span></span>
-   <span data-ttu-id="5dc70-108">L’installation de l’application ne remplace pas les autres versions des fichiers partagés par d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="5dc70-108">Installing the application does not overwrite other versions of the shared files by other applications.</span></span>
-   <span data-ttu-id="5dc70-109">Les installations ultérieures d’autres applications utilisant des versions différentes des fichiers partagés ne peuvent pas remplacer les fichiers utilisés par cette application.</span><span class="sxs-lookup"><span data-stu-id="5dc70-109">Subsequent installations of other applications using different versions of the shared files cannot overwrite the files used by this application.</span></span>

<span data-ttu-id="5dc70-110">Étant donné que l’implémentation actuelle de COM conserve un seul chemin d’accès complet dans le registre pour chaque paire CLSID/contexte, elle force toutes les applications à utiliser la même version d’une DLL partagée.</span><span class="sxs-lookup"><span data-stu-id="5dc70-110">Because the current implementation of COM keeps a single full path in the registry for each CLSID/Context pair, it forces all applications to use the same version of a shared DLL.</span></span> <span data-ttu-id="5dc70-111">Pour permettre à une application de conserver une copie privée d’un serveur COM, le chargeur du système dans Windows 2000 vérifie la présence d’un. Fichier LOCAL dans le dossier de l’application.</span><span class="sxs-lookup"><span data-stu-id="5dc70-111">To enable an application to keep a private copy of a COM server, the system loader in Windows 2000 checks for the presence of a .LOCAL file in the application's folder.</span></span> <span data-ttu-id="5dc70-112">Si le chargeur de système détecte un. Fichier LOCAL, il modifie sa logique de recherche pour préférer les dll situées dans le même dossier que l’application.</span><span class="sxs-lookup"><span data-stu-id="5dc70-112">If the system loader detects a .LOCAL file, it alters its search logic to prefer DLLs located in the same folder as the application.</span></span>

<span data-ttu-id="5dc70-113">Lorsque Windows Installer exécute l' [action IsolateComponents](isolatecomponents-action.md) , il copie les fichiers du composant (généralement une DLL partagée) spécifiés dans la \_ colonne Shared Component de la [table IsolatedComponent](isolatedcomponent-table.md) dans le même dossier que le composant (généralement un fichier. exe) spécifié dans la \_ colonne application du composant.</span><span class="sxs-lookup"><span data-stu-id="5dc70-113">When Windows Installer runs the [IsolateComponents action](isolatecomponents-action.md) they copy the files of the component (commonly a shared DLL) specified in the Component\_Shared column of the [IsolatedComponent table](isolatedcomponent-table.md) into the same folder as the component (commonly an .exe file) specified in the Component\_Application column.</span></span> <span data-ttu-id="5dc70-114">Le programme d’installation crée un fichier dans ce répertoire, avec une longueur de zéro octet, avec le nom de fichier Short du fichier de clé pour l’application de composant \_ (en général, le nom est le même que le fichier. exe de l’application) ajouté à. Localisé.</span><span class="sxs-lookup"><span data-stu-id="5dc70-114">The installer creates a file in this directory, zero bytes in length, having the short file name of the key file for Component\_Application (typically the name is the same as the application's .exe) appended with .LOCAL.</span></span> <span data-ttu-id="5dc70-115">Le programme d’installation utilise l’inscription du composant dans son emplacement partagé et n’écrit pas d’informations d’inscription pour la copie du composant dans l’emplacement privé.</span><span class="sxs-lookup"><span data-stu-id="5dc70-115">The installer uses the registration for the component in its shared location and does not write any registration information for the copy of the component in the private location.</span></span>

<span data-ttu-id="5dc70-116">Pour plus d’informations, consultez :</span><span class="sxs-lookup"><span data-stu-id="5dc70-116">For more information, see:</span></span>

-   [<span data-ttu-id="5dc70-117">Installation de composants isolés</span><span class="sxs-lookup"><span data-stu-id="5dc70-117">Installation of Isolated Components</span></span>](installation-of-isolated-components.md)
-   [<span data-ttu-id="5dc70-118">Réinstallation de composants isolés</span><span class="sxs-lookup"><span data-stu-id="5dc70-118">Reinstallation of Isolated Components</span></span>](reinstallation-of-isolated-components.md)
-   [<span data-ttu-id="5dc70-119">Suppression de composants isolés</span><span class="sxs-lookup"><span data-stu-id="5dc70-119">Removal of Isolated Components</span></span>](removal-of-isolated-components.md)
-   [<span data-ttu-id="5dc70-120">Utilisation des composants isolés</span><span class="sxs-lookup"><span data-stu-id="5dc70-120">Using Isolated Components</span></span>](using-isolated-components.md)

 

 



