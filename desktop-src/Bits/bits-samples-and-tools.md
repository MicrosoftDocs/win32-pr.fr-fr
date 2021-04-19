---
title: Exemples et outils BITS
description: Exemples et outils BITS
ms.assetid: e449da0d-46da-44f9-85f3-4f0e17887bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b651ec8d4a2c3b61381dda488293ff6a3b9f2c90
ms.sourcegitcommit: dc13cc13522097188392392d85f99de48a213984
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2020
ms.locfileid: "106511479"
---
# <a name="bits-samples-and-tools"></a><span data-ttu-id="03ad7-103">Exemples et outils BITS</span><span class="sxs-lookup"><span data-stu-id="03ad7-103">BITS Samples and Tools</span></span>

<span data-ttu-id="03ad7-104">La section suivante contient des exemples C++ pas à pas pour Service de transfert intelligent en arrière-plan (BITS).</span><span class="sxs-lookup"><span data-stu-id="03ad7-104">The following section contains step-by-step C++ examples for Background Intelligent Transfer Service (BITS).</span></span>



| <span data-ttu-id="03ad7-105">Section</span><span class="sxs-lookup"><span data-stu-id="03ad7-105">Section</span></span>                                                            | <span data-ttu-id="03ad7-106">Objectif</span><span class="sxs-lookup"><span data-stu-id="03ad7-106">Purpose</span></span>                                                                                      |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03ad7-107">Exemples d’applications C++ BITS</span><span class="sxs-lookup"><span data-stu-id="03ad7-107">BITS C++ Application Examples</span></span>](bits-c---application-examples.md) | <span data-ttu-id="03ad7-108">Exemples C++ qui illustrent une plage de tâches qui peuvent être effectuées à l’aide des fonctionnalités BITS.</span><span class="sxs-lookup"><span data-stu-id="03ad7-108">C++ examples that demonstrate a range of tasks that can be completed by using BITS features.</span></span> |



 

<span data-ttu-id="03ad7-109">En outre, le service BITS comprend les exemples suivants dans SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="03ad7-109">In addition, BITS includes the following samples in Windows SDK.</span></span> <span data-ttu-id="03ad7-110">Les exemples se trouvent sous *InstallDirectory* \\ Web Samples \\ .</span><span class="sxs-lookup"><span data-stu-id="03ad7-110">The samples are located under *InstallDirectory*\\Samples\\Web.</span></span> <span data-ttu-id="03ad7-111">Chaque exemple comprend un fichier de Readme.txt qui explique comment installer et exécuter l’exemple.</span><span class="sxs-lookup"><span data-stu-id="03ad7-111">Each sample includes a Readme.txt file that explains how to install and run the sample.</span></span> <span data-ttu-id="03ad7-112">Vous pouvez télécharger le SDK Windows à partir du [Kit de développement logiciel (SDK) Microsoft Windows](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="03ad7-112">You can download the Windows SDK from [Microsoft Windows Software Development Kit](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="03ad7-113">Le service BITS est inclus dans le kit de développement logiciel (SDK) principal.</span><span class="sxs-lookup"><span data-stu-id="03ad7-113">BITS is included in the Core SDK.</span></span>

> [!Note]  
> <span data-ttu-id="03ad7-114">Windows Vista : les exemples de cette page sont inclus dans le [Microsoft Windows SDK pour Windows Vista](https://www.microsoft.com/download/details.aspx?id=30998).</span><span class="sxs-lookup"><span data-stu-id="03ad7-114">Windows Vista: The samples on this page are included in the [Microsoft Windows SDK for Windows Vista](https://www.microsoft.com/download/details.aspx?id=30998).</span></span> <span data-ttu-id="03ad7-115">Toutefois, l’exemple ClientCert n’est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="03ad7-115">However, the ClientCert sample is not included.</span></span>

 



| <span data-ttu-id="03ad7-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="03ad7-116">Sample</span></span>       | <span data-ttu-id="03ad7-117">Objectif</span><span class="sxs-lookup"><span data-stu-id="03ad7-117">Purpose</span></span>                                                                                                                                                                                                                                  |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03ad7-118">\_IE bits</span><span class="sxs-lookup"><span data-stu-id="03ad7-118">BITS\_IE</span></span>     | <span data-ttu-id="03ad7-119">Montre comment utiliser les [interfaces](bits-interfaces.md) bits pour télécharger des fichiers à partir d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="03ad7-119">Shows how to use the BITS [interfaces](bits-interfaces.md) to download files from a server.</span></span>                                                                                                                                             |
| <span data-ttu-id="03ad7-120">Commandes</span><span class="sxs-lookup"><span data-stu-id="03ad7-120">Controls</span></span>     | <span data-ttu-id="03ad7-121">Montre comment utiliser les [interfaces](bits-interfaces.md) bits pour contrôler et configurer les options bits, y compris l’utilisation de certaines méthodes d’administration du cache d’homologue.</span><span class="sxs-lookup"><span data-stu-id="03ad7-121">Shows how to use the BITS [interfaces](bits-interfaces.md) to control and configure BITS options, including using some of the peer cache administration methods.</span></span><br/> <span data-ttu-id="03ad7-122">**BITS 4,0 :** L’exemple Controls est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="03ad7-122">**BITS 4.0:** The Controls sample is deprecated.</span></span><br/> |
| <span data-ttu-id="03ad7-123">Téléchargements</span><span class="sxs-lookup"><span data-stu-id="03ad7-123">Downloads</span></span>    | <span data-ttu-id="03ad7-124">Montre comment utiliser les [interfaces](bits-interfaces.md) bits pour télécharger des fichiers à partir d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="03ad7-124">Shows how to use the BITS [interfaces](bits-interfaces.md) to download files from a server.</span></span>                                                                                                                                             |
| <span data-ttu-id="03ad7-125">HTTPHeaders</span><span class="sxs-lookup"><span data-stu-id="03ad7-125">HTTPHeaders</span></span>  | <span data-ttu-id="03ad7-126">Montre comment utiliser les [interfaces](bits-interfaces.md) bits pour modifier les en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="03ad7-126">Shows how to use the BITS [interfaces](bits-interfaces.md) to modify HTTP headers.</span></span>                                                                                                                                                      |
| <span data-ttu-id="03ad7-127">Pair</span><span class="sxs-lookup"><span data-stu-id="03ad7-127">PeerCaching</span></span>  | <span data-ttu-id="03ad7-128">Montre comment utiliser les [interfaces](bits-interfaces.md) bits pour permettre à un travail de télécharger à partir d’un homologue.</span><span class="sxs-lookup"><span data-stu-id="03ad7-128">Shows how to use the BITS [interfaces](bits-interfaces.md) to enable a job to download from a peer.</span></span><br/> <span data-ttu-id="03ad7-129">**BITS 4,0 :** L’exemple de cache de la cache est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="03ad7-129">**BITS 4.0:** The PeerCaching sample is deprecated.</span></span><br/>                                                           |
| <span data-ttu-id="03ad7-130">Charge</span><span class="sxs-lookup"><span data-stu-id="03ad7-130">Uploads</span></span>      | <span data-ttu-id="03ad7-131">Montre comment utiliser les [interfaces](bits-interfaces.md) bits pour télécharger un fichier.</span><span class="sxs-lookup"><span data-stu-id="03ad7-131">Shows how to use the BITS [interfaces](bits-interfaces.md) to upload a file.</span></span>                                                                                                                                                            |
| <span data-ttu-id="03ad7-132">UploadSample</span><span class="sxs-lookup"><span data-stu-id="03ad7-132">UploadSample</span></span> | <span data-ttu-id="03ad7-133">Montre comment utiliser les [interfaces](bits-interfaces.md) bits pour télécharger un fichier sur un serveur et recevoir une réponse.</span><span class="sxs-lookup"><span data-stu-id="03ad7-133">Shows how to use the BITS [interfaces](bits-interfaces.md) to upload a file to a server and receive a reply.</span></span>                                                                                                                            |



 

<span data-ttu-id="03ad7-134">Le service BITS fournit l’outil suivant.</span><span class="sxs-lookup"><span data-stu-id="03ad7-134">BITS provides the following tool.</span></span>



| <span data-ttu-id="03ad7-135">Outil</span><span class="sxs-lookup"><span data-stu-id="03ad7-135">Tool</span></span>                            | <span data-ttu-id="03ad7-136">Objectif</span><span class="sxs-lookup"><span data-stu-id="03ad7-136">Purpose</span></span>                                                                         |
|---------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="03ad7-137">BITSAdmin</span><span class="sxs-lookup"><span data-stu-id="03ad7-137">BITSAdmin</span></span>](bitsadmin-tool.md) | <span data-ttu-id="03ad7-138">Outil en ligne de commande pour créer des travaux de téléchargement ou de téléchargement et surveiller leur progression.</span><span class="sxs-lookup"><span data-stu-id="03ad7-138">Command-line tool to create download or upload jobs and monitor their progress.</span></span> |



 

## <a name="additional-information"></a><span data-ttu-id="03ad7-139">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="03ad7-139">Additional Information</span></span>

<span data-ttu-id="03ad7-140">Si vous avez besoin d’informations supplémentaires, envisagez de poser des questions dans le groupe de discussion BITS Microsoft. Windows. public. backgroundtransfer.</span><span class="sxs-lookup"><span data-stu-id="03ad7-140">If you need additional information, consider asking questions in the BITS newsgroup microsoft.windows.public.backgroundtransfer.</span></span>

<span data-ttu-id="03ad7-141">Le serveur de groupe de discussion est msnews.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="03ad7-141">The newsgroup server is msnews.microsoft.com.</span></span>

 

 





