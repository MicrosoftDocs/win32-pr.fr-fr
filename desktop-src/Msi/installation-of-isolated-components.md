---
description: Windows Installer effectue les actions suivantes lors de l’installation d’une application lorsque le package contient des composants isolés. En règle générale, \_ le composant partagé est une DLL partagée par l' \_ application composant et d’autres exécutables client.
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Installation de composants isolés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c1b9a7e21c212474701409e887d0afd5517774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753765"
---
# <a name="installation-of-isolated-components"></a><span data-ttu-id="a45bb-104">Installation de composants isolés</span><span class="sxs-lookup"><span data-stu-id="a45bb-104">Installation of Isolated Components</span></span>

<span data-ttu-id="a45bb-105">Windows Installer effectue les actions suivantes lors de l’installation d’une application lorsque le package contient des composants isolés.</span><span class="sxs-lookup"><span data-stu-id="a45bb-105">Windows Installer performs the following actions during installation of an application when the package contains isolated components.</span></span> <span data-ttu-id="a45bb-106">En règle générale, \_ le composant partagé est une DLL partagée par l' \_ application composant et d’autres exécutables client.</span><span class="sxs-lookup"><span data-stu-id="a45bb-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="installation"></a><span data-ttu-id="a45bb-107">Installation</span><span class="sxs-lookup"><span data-stu-id="a45bb-107">Installation</span></span>

-   <span data-ttu-id="a45bb-108">Copiez les fichiers du composant \_ partagé dans le même dossier que le composant \_ application Component uniquement si l' \_ application composant est également en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="a45bb-108">Copy the files of Component\_Shared into the same folder as Component\_Application only if Component\_Application is also being installed.</span></span>
-   <span data-ttu-id="a45bb-109">Créez un fichier de zéro octet avec le nom de fichier abrégé du fichier de clé de l’application de composant \_ .</span><span class="sxs-lookup"><span data-stu-id="a45bb-109">Create a zero-byte file with the short file name of the key file of Component\_Application.</span></span> <span data-ttu-id="a45bb-110">Recherchez ce fichier dans le même dossier que le composant \_ application.</span><span class="sxs-lookup"><span data-stu-id="a45bb-110">Locate this file in the same folder as Component\_Application.</span></span> <span data-ttu-id="a45bb-111">Ajoutez l’extension. LOCAL pour ce nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="a45bb-111">Append the extension .LOCAL to this file name.</span></span>
-   <span data-ttu-id="a45bb-112">Incrémentez le refcount SharedDLL si le bit msidbComponentAttributesSharedDllRefCount est défini dans la colonne attributs de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a45bb-112">Increment the SharedDLL refcount if the msidbComponentAttributesSharedDllRefCount bit is set in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="a45bb-113">Inscrire \_ l’application composant en tant que client du composant \_ partagé et enregistrer un chemin d’accès de clé pointant vers l’emplacement partagé du composant \_ partagé.</span><span class="sxs-lookup"><span data-stu-id="a45bb-113">Register Component\_Application as a client of Component\_Shared and register a key path pointing to the shared location of Component\_Shared.</span></span>
-   <span data-ttu-id="a45bb-114">Installez toutes les ressources de l’application de composant \_ comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="a45bb-114">Install all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="a45bb-115">Si \_ le composant partagé ou son fichier de clé est déjà installé sur l’ordinateur, ne copiez pas les fichiers dans l’emplacement partagé du composant \_ partagé.</span><span class="sxs-lookup"><span data-stu-id="a45bb-115">If Component\_Shared or its key file is already installed on the computer do not copy files to the shared location of Component\_Shared.</span></span>

<span data-ttu-id="a45bb-116">Si \_ le composant partagé ou son fichier de clé n’est pas encore installé sur l’ordinateur :</span><span class="sxs-lookup"><span data-stu-id="a45bb-116">If Component\_Shared or its key file is not yet installed on the computer:</span></span>

-   <span data-ttu-id="a45bb-117">Copiez les fichiers du composant \_ partagé dans l’emplacement partagé.</span><span class="sxs-lookup"><span data-stu-id="a45bb-117">Copy the files of Component\_Shared to the shared location.</span></span>
-   <span data-ttu-id="a45bb-118">Traite toutes les actions d’installation du composant \_ partagé.</span><span class="sxs-lookup"><span data-stu-id="a45bb-118">Process all install actions for Component\_Shared.</span></span>
-   <span data-ttu-id="a45bb-119">Si le composant \_ partagé est un composant com, enregistrez le chemin d’accès com complet afin que la syntaxe \[ $Component \] et \[ \# FileKey \] pointent vers l’emplacement partagé du composant \_ partagé.</span><span class="sxs-lookup"><span data-stu-id="a45bb-119">If Component\_Shared is a COM component, register the full COM path such that the syntax \[$Component\] and \[\#FileKey\] point to the shared location of Component\_Shared.</span></span>

 

 



