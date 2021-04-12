---
title: Configuration du fournisseur de services Microsoft Locator Name
description: Vous pouvez modifier le fournisseur de services de noms que vous avez spécifié en modifiant le fichier de configuration Rpcreg. dat, qui contient les paramètres NSP et les paramètres de protocole RPC. Utilisez un éditeur de texte pour modifier les entrées NSP.
ms.assetid: b499e40e-d38f-4e51-bbce-41af3ff12a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a5334436ce307030048a862f1375a91000b41e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310417"
---
# <a name="configuring-the-microsoft-locator-name-service-provider"></a><span data-ttu-id="00d0f-104">Configuration du fournisseur de services Microsoft Locator Name</span><span class="sxs-lookup"><span data-stu-id="00d0f-104">Configuring the Microsoft Locator Name Service Provider</span></span>

<span data-ttu-id="00d0f-105">Vous pouvez modifier le fournisseur de services de noms que vous avez spécifié en modifiant le fichier de configuration Rpcreg. dat, qui contient les paramètres NSP et les paramètres de protocole RPC.</span><span class="sxs-lookup"><span data-stu-id="00d0f-105">You can change the name service provider you specified by editing the Rpcreg.dat configuration file, which contains the NSP parameters and RPC protocol settings.</span></span> <span data-ttu-id="00d0f-106">Utilisez un éditeur de texte pour modifier les entrées NSP.</span><span class="sxs-lookup"><span data-stu-id="00d0f-106">Use a text editor to change NSP entries.</span></span>

<span data-ttu-id="00d0f-107">**Pour reconfigurer le fournisseur de services de noms Microsoft Locator**</span><span class="sxs-lookup"><span data-stu-id="00d0f-107">**To reconfigure the Microsoft Locator name service provider**</span></span>

1.  <span data-ttu-id="00d0f-108">Ouvrez le fichier Rpcreg. dat à l’aide d’un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="00d0f-108">Open the Rpcreg.dat file using a text editor.</span></span>

    <span data-ttu-id="00d0f-109">Rpcreg. dat se trouve dans le répertoire racine, sauf si vous avez spécifié un chemin d’accès différent au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="00d0f-109">Rpcreg.dat is in the root directory unless you specified a different path during setup.</span></span>

2.  <span data-ttu-id="00d0f-110">Définissez les valeurs suivantes pour les entrées de registre.</span><span class="sxs-lookup"><span data-stu-id="00d0f-110">Set the following values for the registry entries.</span></span> 

    | <span data-ttu-id="00d0f-111">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="00d0f-111">Registry entry</span></span>                                         | <span data-ttu-id="00d0f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="00d0f-112">Value</span></span>                                                                                                                                                 |
    |--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="00d0f-113">\\Protocole Microsoft \\ RPC \\ NameService \\</span><span class="sxs-lookup"><span data-stu-id="00d0f-113">Software\\Microsoft\\RPC \\NameService\\Protocol</span></span>       | <span data-ttu-id="00d0f-114">Séquence de protocole pour le protocole que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="00d0f-114">The protocol sequence for the protocol you are using.</span></span> <span data-ttu-id="00d0f-115">La valeur par défaut est **ncacn \_ NP**.</span><span class="sxs-lookup"><span data-stu-id="00d0f-115">The default is **ncacn\_np**.</span></span>                                                                   |
    | <span data-ttu-id="00d0f-116">Logiciel \\ Microsoft \\ RPC \\ NameService \\ networkAddress</span><span class="sxs-lookup"><span data-stu-id="00d0f-116">Software\\Microsoft\\RPC\\ NameService\\NetworkAddress</span></span> | <span data-ttu-id="00d0f-117">Nom de l’ordinateur exécutant le localisateur qui est utilisé par les clients lors des opérations de recherche du service de nom.</span><span class="sxs-lookup"><span data-stu-id="00d0f-117">The name of the computer running Locator that is used by clients during name service lookup operations.</span></span> <span data-ttu-id="00d0f-118">La valeur par défaut est le contrôleur de domaine principal.</span><span class="sxs-lookup"><span data-stu-id="00d0f-118">The default is the primary domain controller.</span></span> |
    | <span data-ttu-id="00d0f-119">\\Point de \\ \\ terminaison NameService Microsoft RPC \\ logiciel</span><span class="sxs-lookup"><span data-stu-id="00d0f-119">Software\\Microsoft\\RPC\\ NameService\\Endpoint</span></span>       | <span data-ttu-id="00d0f-120">Nom du point de terminaison utilisé par le service de noms.</span><span class="sxs-lookup"><span data-stu-id="00d0f-120">The name of the endpoint used by the name service.</span></span> <span data-ttu-id="00d0f-121">La valeur par défaut est le \\ localisateur de canal \\ .</span><span class="sxs-lookup"><span data-stu-id="00d0f-121">The default is \\pipe\\locator.</span></span>                                                                    |

    

     

3.  <span data-ttu-id="00d0f-122">Enregistrez et fermez le fichier.</span><span class="sxs-lookup"><span data-stu-id="00d0f-122">Save and close the file.</span></span>

 

 




