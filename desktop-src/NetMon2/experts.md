---
description: Un expert est une bibliothèque de liens dynamiques (DLL) Microsoft Win32 qui analyse le trafic réseau collecté par un fournisseur de paquets réseau (NPP) et placé dans un fichier de capture.
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: Expert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf5fc0096b15d590bf70859443667f2d9969f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538841"
---
# <a name="expert"></a><span data-ttu-id="22fd6-103">Expert</span><span class="sxs-lookup"><span data-stu-id="22fd6-103">Expert</span></span>

<span data-ttu-id="22fd6-104">Un expert est une bibliothèque de liens dynamiques (DLL) Microsoft Win32 qui analyse le trafic réseau collecté par un [*fournisseur de paquets réseau*](n.md) (NPP) et placé dans un fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="22fd6-104">An expert is a Microsoft Win32 dynamic-link library (DLL) that analyzes network traffic collected by a [*network packet provider*](n.md) (NPP), and placed in a capture file.</span></span> <span data-ttu-id="22fd6-105">Une fois les données capturées et stockées dans un fichier de capture, l’expert travaille avec un analyseur, également appelé analyseur de protocole, pour analyser les données contenues dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="22fd6-105">After the data is captured and stored in a capture file, the expert works with a parser, also referred to as a protocol parser, to analyze the data in the file.</span></span> <span data-ttu-id="22fd6-106">Par exemple, vous pouvez examiner les frames du fichier de capture et utiliser un [*analyseur*](p.md) pour reconnaître des protocoles tels que le protocole SMB (Server Message Block) ou le protocole TCP/IP (Transmission Control Protocol/Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="22fd6-106">For example, you can examine the frames of the capture file and use a [*parser*](p.md) to recognize protocols such as server message block (SMB), or Transmission Control Protocol/Internet Protocol (TCP/IP).</span></span>

<span data-ttu-id="22fd6-107">Vous pouvez concevoir un expert pour travailler avec tous les analyseurs de Moniteur réseau et tous les analyseurs que vous créez vous-même.</span><span class="sxs-lookup"><span data-stu-id="22fd6-107">You can design an expert to work with all of the Network Monitor parsers, and any parsers that you create yourself.</span></span>

<span data-ttu-id="22fd6-108">Une fois que la correspondance de protocoles demandée identifie un frame spécifique, l’expert extrait des données du frame.</span><span class="sxs-lookup"><span data-stu-id="22fd6-108">After a requested match of protocols identifies a specific frame, the expert extracts data from the frame.</span></span> <span data-ttu-id="22fd6-109">Vous pouvez programmer l’expert pour manipuler des informations dans des données utilisables que l’Moniteur réseau observateur d’événements affiche.</span><span class="sxs-lookup"><span data-stu-id="22fd6-109">You can program the expert to manipulate information into usable data that the Network Monitor Event Viewer displays.</span></span>

<span data-ttu-id="22fd6-110">Vous pouvez configurer un expert au moment de l’exécution, puis utiliser Moniteur réseau pour enregistrer les données de configuration utilisateur en vue de les réutiliser avec différents fichiers de capture.</span><span class="sxs-lookup"><span data-stu-id="22fd6-110">You can configure an expert at run time, and then use Network Monitor to save user configuration data for reuse with different capture files.</span></span> <span data-ttu-id="22fd6-111">Vous pouvez utiliser un expert pour fournir des données de corrélation et des résolutions personnalisées pour les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="22fd6-111">You can use an expert to provide correlation data and custom resolutions for end users.</span></span> <span data-ttu-id="22fd6-112">Pour plus d’informations sur la création d’informations de configuration HTML, consultez la [page de référence des événements](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="22fd6-112">For more information about the creation of HTML-based configuration information, see [Event Reference Page](event-reference-page.md).</span></span>

<span data-ttu-id="22fd6-113">Pendant l’installation de Moniteur réseau, les dll d’experts suivantes sont installées dans le sous-répertoire experts :</span><span class="sxs-lookup"><span data-stu-id="22fd6-113">During Network Monitor setup, the following expert DLLs are installed in the Experts sub-directory:</span></span>

-   <span data-ttu-id="22fd6-114">Coalesce.dll</span><span class="sxs-lookup"><span data-stu-id="22fd6-114">Coalesce.dll</span></span>
-   <span data-ttu-id="22fd6-115">Propdist.dll</span><span class="sxs-lookup"><span data-stu-id="22fd6-115">Propdist.dll</span></span>
-   <span data-ttu-id="22fd6-116">Protdist.dll</span><span class="sxs-lookup"><span data-stu-id="22fd6-116">Protdist.dll</span></span>
-   <span data-ttu-id="22fd6-117">Resptime.dll</span><span class="sxs-lookup"><span data-stu-id="22fd6-117">Resptime.dll</span></span>
-   <span data-ttu-id="22fd6-118">Tcpipe.dll</span><span class="sxs-lookup"><span data-stu-id="22fd6-118">Tcpipe.dll</span></span>
-   <span data-ttu-id="22fd6-119">Topuser.dll</span><span class="sxs-lookup"><span data-stu-id="22fd6-119">Topuser.dll</span></span>

<span data-ttu-id="22fd6-120">Lorsque vous démarrez Moniteur réseau, la fonction [**DllMain**](dllmain-expert.md) crée tous les experts dans le sous-répertoire experts.</span><span class="sxs-lookup"><span data-stu-id="22fd6-120">When you start Network Monitor, the [**DllMain**](dllmain-expert.md) function builds all experts in the experts subdirectory.</span></span> <span data-ttu-id="22fd6-121">Lorsque l’utilisateur sélectionne **experts** dans le menu **Outils** de l’interface utilisateur Moniteur réseau, moniteur réseau charge les dll d’experts.</span><span class="sxs-lookup"><span data-stu-id="22fd6-121">When the user selects **Experts** on the **Tools** menu of the Network Monitor UI, Network Monitor loads the expert DLLs.</span></span> <span data-ttu-id="22fd6-122">L’expert est appelé via le point d’entrée de l' [expert Register](register-expert.md) pour fournir des informations de base sur l’expert.</span><span class="sxs-lookup"><span data-stu-id="22fd6-122">The expert is called through the [Register Expert](register-expert.md) entry point to provide basic details about the expert.</span></span>

![boîte de dialogue experts du moniteur réseau](images/expick.png)

<span data-ttu-id="22fd6-124">Moniteur réseau appelle les fonctions suivantes pour gérer l’expert :</span><span class="sxs-lookup"><span data-stu-id="22fd6-124">Network Monitor calls the following functions to manage the expert:</span></span>

-   [<span data-ttu-id="22fd6-125">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="22fd6-125">**DllMain**</span></span>](dllmain-expert.md)
-   [<span data-ttu-id="22fd6-126">**Inscrire un expert**</span><span class="sxs-lookup"><span data-stu-id="22fd6-126">**Register Expert**</span></span>](register-expert.md)
-   [<span data-ttu-id="22fd6-127">**Utilisez**</span><span class="sxs-lookup"><span data-stu-id="22fd6-127">**Run**</span></span>](run.md)
-   [<span data-ttu-id="22fd6-128">**Configurer**</span><span class="sxs-lookup"><span data-stu-id="22fd6-128">**Configure**</span></span>](configure.md)

<span data-ttu-id="22fd6-129">L’expert doit implémenter chacune des fonctions précédentes.</span><span class="sxs-lookup"><span data-stu-id="22fd6-129">The expert must implement each of the preceding functions.</span></span>

 

 



