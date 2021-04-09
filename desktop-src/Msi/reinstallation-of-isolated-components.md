---
description: Windows Installer effectue les actions suivantes lors de la réinstallation d’une application lorsque le package contient des composants isolés. En règle générale, \_ le composant partagé est une DLL partagée par l' \_ application composant et d’autres exécutables client.
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: Réinstallation de composants isolés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad1c7fb53eb09e96882209f7738e95be9b4a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864829"
---
# <a name="reinstallation-of-isolated-components"></a><span data-ttu-id="64cf2-104">Réinstallation de composants isolés</span><span class="sxs-lookup"><span data-stu-id="64cf2-104">Reinstallation of Isolated Components</span></span>

<span data-ttu-id="64cf2-105">Windows Installer effectue les actions suivantes lors de la réinstallation d’une application lorsque le package contient des composants isolés.</span><span class="sxs-lookup"><span data-stu-id="64cf2-105">Windows Installer performs the following actions during reinstallation of an application when the package contains isolated components.</span></span> <span data-ttu-id="64cf2-106">En règle générale, \_ le composant partagé est une DLL partagée par l' \_ application composant et d’autres exécutables client.</span><span class="sxs-lookup"><span data-stu-id="64cf2-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="reinstallation"></a><span data-ttu-id="64cf2-107">La réinstallation</span><span class="sxs-lookup"><span data-stu-id="64cf2-107">Reinstallation</span></span>

-   <span data-ttu-id="64cf2-108">Réinstallez les fichiers du composant \_ partagés dans le même dossier que le composant \_ application Component uniquement si l' \_ application composant est également en cours de réinstallation.</span><span class="sxs-lookup"><span data-stu-id="64cf2-108">Reinstall of the files of Component\_Shared into the same folder as Component\_Application only if Component\_Application is also being reinstalled.</span></span>
-   <span data-ttu-id="64cf2-109">N’incrémentez pas la liste des clients du composant \_ partagé et n’incrémentez pas le nombre de SharedDLL.</span><span class="sxs-lookup"><span data-stu-id="64cf2-109">Do not increment the client list of Component\_Shared and do not increment the SharedDLL count.</span></span>
-   <span data-ttu-id="64cf2-110">Recréez le fichier de zéro octet avec le nom de fichier abrégé du fichier de clé de l’application de composant \_ .</span><span class="sxs-lookup"><span data-stu-id="64cf2-110">Recreate the zero-byte file with the short file name of the key file of Component\_Application.</span></span> <span data-ttu-id="64cf2-111">Ce fichier doit se trouver dans le même dossier que \_ le composant application et avoir l’extension. Localisé.</span><span class="sxs-lookup"><span data-stu-id="64cf2-111">This file must be located in the same folder as Component\_Application and have the extension .LOCAL.</span></span>
-   <span data-ttu-id="64cf2-112">Réinstallez toutes les ressources de l' \_ application de composant comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="64cf2-112">Reinstall all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="64cf2-113">Si le refcount SharedDLL pour le composant \_ partagé est supérieur à 1, ou si d’autres produits sont conservés dans la liste des clients du composant \_ partagé :</span><span class="sxs-lookup"><span data-stu-id="64cf2-113">If the SharedDLL refcount for Component\_Shared is more than 1, or if other products remain on the client list of Component\_Shared:</span></span>

-   <span data-ttu-id="64cf2-114">Ne réinstallez aucun fichier à l’emplacement partagé du composant \_ partagé.</span><span class="sxs-lookup"><span data-stu-id="64cf2-114">Reinstall no files to the shared location of Component\_Shared.</span></span>

<span data-ttu-id="64cf2-115">Si le refcount SharedDLL pour le composant \_ partagé est égal à 1, ou s’il n’existe aucun autre client restant du composant \_ partagé :</span><span class="sxs-lookup"><span data-stu-id="64cf2-115">If the SharedDLL refcount for Component\_Shared equals 1, or if there are no other remaining clients of Component\_Shared:</span></span>

-   <span data-ttu-id="64cf2-116">Réinstallez les fichiers du composant \_ partagés dans l’emplacement partagé à l’aide des règles de contrôle de [version des fichiers](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="64cf2-116">Reinstall of the files of Component\_Shared into the shared location using the [File Versioning Rules](file-versioning-rules.md).</span></span>
-   <span data-ttu-id="64cf2-117">Traiter toutes les actions de réinstallation pour le composant \_ partagé.</span><span class="sxs-lookup"><span data-stu-id="64cf2-117">Process all reinstall actions for Component\_Shared.</span></span>
-   <span data-ttu-id="64cf2-118">Si le composant \_ partagé est un composant com, enregistrez le chemin d’accès com complet afin que la syntaxe du programme d’installation \[ $Component \] et \[ \# FileKey \] pointer vers l’emplacement partagé du composant \_ partagé.</span><span class="sxs-lookup"><span data-stu-id="64cf2-118">If Component\_Shared is a COM component, register the full COM path such that the installer syntaxes \[$Component\] and \[\#FileKey\] point to the shared location of Component\_Shared.</span></span>

 

 



