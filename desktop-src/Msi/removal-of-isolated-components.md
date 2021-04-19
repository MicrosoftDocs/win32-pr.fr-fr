---
description: Windows Installer effectue les actions suivantes lors de la suppression d’une application lorsque le package contient des composants isolés. En règle générale, \_ le composant partagé est une DLL partagée par l' \_ application composant et d’autres exécutables client.
ms.assetid: 26343a01-9a06-43d5-bbe3-959faf51739d
title: Suppression de composants isolés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf19769067230b82f68a35f7b9fbedcd1c56440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529307"
---
# <a name="removal-of-isolated-components"></a><span data-ttu-id="4ba77-104">Suppression de composants isolés</span><span class="sxs-lookup"><span data-stu-id="4ba77-104">Removal of Isolated Components</span></span>

<span data-ttu-id="4ba77-105">Windows Installer effectue les actions suivantes lors de la suppression d’une application lorsque le package contient des composants isolés.</span><span class="sxs-lookup"><span data-stu-id="4ba77-105">Windows Installer performs the following actions during the removal of an application when the package contains isolated components.</span></span> <span data-ttu-id="4ba77-106">En règle générale, \_ le composant partagé est une DLL partagée par l' \_ application composant et d’autres exécutables client.</span><span class="sxs-lookup"><span data-stu-id="4ba77-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="uninstall"></a><span data-ttu-id="4ba77-107">Désinstaller l’interface</span><span class="sxs-lookup"><span data-stu-id="4ba77-107">Uninstall</span></span>

-   <span data-ttu-id="4ba77-108">Supprimer les fichiers du composant \_ partagé du dossier contenant l' \_ application composant uniquement si l' \_ application composant est également en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="4ba77-108">Remove the files of Component\_Shared from the folder containing Component\_Application only if Component\_Application is also being removed.</span></span>
-   <span data-ttu-id="4ba77-109">Si le bit msidbComponentAttributesSharedDllRefCount est défini dans la [table des composants](component-table.md) , décrémente le refcount SharedDLL.</span><span class="sxs-lookup"><span data-stu-id="4ba77-109">If the msidbComponentAttributesSharedDllRefCount bit is set in the [Component table](component-table.md) decrement the SharedDLL refcount.</span></span>
-   <span data-ttu-id="4ba77-110">Supprimez. Fichier de zéro octet LOCAL à partir du dossier contenant l’application du composant \_ .</span><span class="sxs-lookup"><span data-stu-id="4ba77-110">Remove the .LOCAL zero-byte file from the folder containing Component\_Application.</span></span>
-   <span data-ttu-id="4ba77-111">Supprimer \_ l’application composant de la liste des clients du composant \_ partagé.</span><span class="sxs-lookup"><span data-stu-id="4ba77-111">Remove Component\_Application from the client list of Component\_Shared.</span></span>
-   <span data-ttu-id="4ba77-112">Supprimez toutes les ressources de l' \_ application de composant comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="4ba77-112">Remove all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="4ba77-113">Si d’autres produits sont encore dans la liste des clients du composant \_ partagé :</span><span class="sxs-lookup"><span data-stu-id="4ba77-113">If there are other products remaining on the client list of Component\_Shared:</span></span>

-   <span data-ttu-id="4ba77-114">Supprimer aucun fichier de l’emplacement partagé du composant \_ partagé.</span><span class="sxs-lookup"><span data-stu-id="4ba77-114">Remove no files from the shared location of Component\_Shared.</span></span>

<span data-ttu-id="4ba77-115">Si le refcount SharedDLL pour le composant \_ partagé est 0 après avoir été décrémenté, ou s’il n’y a pas d’autres clients du composant \_ partagés :</span><span class="sxs-lookup"><span data-stu-id="4ba77-115">If the SharedDLL refcount for Component\_Shared is 0 after being decremented, or if there are no other remaining clients of Component\_Shared:</span></span>

-   <span data-ttu-id="4ba77-116">Supprimez les fichiers du composant \_ partagés à partir de l’emplacement partagé.</span><span class="sxs-lookup"><span data-stu-id="4ba77-116">Remove the files of Component\_Shared from the shared location.</span></span>
-   <span data-ttu-id="4ba77-117">Traiter toutes les actions de désinstallation par rapport à ce composant.</span><span class="sxs-lookup"><span data-stu-id="4ba77-117">Process all uninstall actions with respect to this component.</span></span>

 

 



