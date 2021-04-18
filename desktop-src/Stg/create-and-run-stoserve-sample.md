---
title: Créer et exécuter un exemple StoServe
description: L’exemple de client et d’autres exemples associés doivent être compilés avant que vous puissiez exécuter le client.
ms.assetid: 7d8fe758-0008-495d-89ae-a814cb07ea19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46645351eb75ceb6b4f6129049b9e8f2db59dbef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512036"
---
# <a name="create-and-run-stoserve-sample"></a><span data-ttu-id="0b41e-103">Créer et exécuter un exemple StoServe</span><span class="sxs-lookup"><span data-stu-id="0b41e-103">Create and Run StoServe Sample</span></span>

<span data-ttu-id="0b41e-104">L’exemple de client et d’autres exemples associés doivent être compilés avant que vous puissiez exécuter le client.</span><span class="sxs-lookup"><span data-stu-id="0b41e-104">The client sample and other related samples must be compiled before you can run the client.</span></span> <span data-ttu-id="0b41e-105">Pour plus d’informations sur la génération des exemples, consultez [Comment générer des exemples](how-to-build-samples.md).</span><span class="sxs-lookup"><span data-stu-id="0b41e-105">For more details on building the samples, see [How to Build Samples](how-to-build-samples.md).</span></span> <span data-ttu-id="0b41e-106">Si vous avez déjà généré les exemples appropriés, STOCLIEN.EXE est l’exécutable client à exécuter pour l’exemple **StoServe** .</span><span class="sxs-lookup"><span data-stu-id="0b41e-106">If you have already built the appropriate samples, STOCLIEN.EXE is the client executable to run for the **StoServe** sample.</span></span>

## <a name="code-tour"></a><span data-ttu-id="0b41e-107">Visite guidée du code</span><span class="sxs-lookup"><span data-stu-id="0b41e-107">Code Tour</span></span>

<span data-ttu-id="0b41e-108">Le tableau suivant répertorie les fichiers pertinents pour l’exemple **StoServe** .</span><span class="sxs-lookup"><span data-stu-id="0b41e-108">The following table lists the files pertinent to the **StoServe** sample.</span></span>



| <span data-ttu-id="0b41e-109">Fichiers</span><span class="sxs-lookup"><span data-stu-id="0b41e-109">Files</span></span>        | <span data-ttu-id="0b41e-110">Description</span><span class="sxs-lookup"><span data-stu-id="0b41e-110">Description</span></span>                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b41e-111">STOSERVE.TXT</span><span class="sxs-lookup"><span data-stu-id="0b41e-111">STOSERVE.TXT</span></span> | <span data-ttu-id="0b41e-112">Brève description de l’exemple</span><span class="sxs-lookup"><span data-stu-id="0b41e-112">Short sample description</span></span>                                                                                                  |
| <span data-ttu-id="0b41e-113">ADOPTE</span><span class="sxs-lookup"><span data-stu-id="0b41e-113">MAKEFILE</span></span>     | <span data-ttu-id="0b41e-114">Makefile générique pour la génération de l’exemple de code STOSERVE.DLL de cette leçon.</span><span class="sxs-lookup"><span data-stu-id="0b41e-114">The generic makefile for building the STOSERVE.DLL code sample of this lesson.</span></span>                                            |
| <span data-ttu-id="0b41e-115">STOSERVE. Manutention</span><span class="sxs-lookup"><span data-stu-id="0b41e-115">STOSERVE.H</span></span>   | <span data-ttu-id="0b41e-116">Fichier include pour déclarer comme importé ou définir comme exporté les fonctions de service dans STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="0b41e-116">The include file for declaring as imported or defining as exported the service functions in STOSERVE.DLL.</span></span>                 |
| <span data-ttu-id="0b41e-117">STOSERVE. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="0b41e-117">STOSERVE.CPP</span></span> | <span data-ttu-id="0b41e-118">Fichier d’implémentation principal pour STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="0b41e-118">The main implementation file for STOSERVE.DLL.</span></span> <span data-ttu-id="0b41e-119">A DllMain et les fonctions du serveur COM (par exemple, DllGetClassObject).</span><span class="sxs-lookup"><span data-stu-id="0b41e-119">Has DllMain and the COM server functions (for example, DllGetClassObject).</span></span> |
| <span data-ttu-id="0b41e-120">STOSERVE. DEF</span><span class="sxs-lookup"><span data-stu-id="0b41e-120">STOSERVE.DEF</span></span> | <span data-ttu-id="0b41e-121">Fichier de définition de module.</span><span class="sxs-lookup"><span data-stu-id="0b41e-121">The module definition file.</span></span> <span data-ttu-id="0b41e-122">Exporte les fonctions de logement du serveur.</span><span class="sxs-lookup"><span data-stu-id="0b41e-122">Exports server housing functions.</span></span>                                                             |
| <span data-ttu-id="0b41e-123">STOSERVE. Release</span><span class="sxs-lookup"><span data-stu-id="0b41e-123">STOSERVE.RC</span></span>  | <span data-ttu-id="0b41e-124">Fichier de définition de ressource DLL pour l’exécutable.</span><span class="sxs-lookup"><span data-stu-id="0b41e-124">The DLL resource definition file for the executable.</span></span>                                                                      |
| <span data-ttu-id="0b41e-125">STOSERVE. ICO</span><span class="sxs-lookup"><span data-stu-id="0b41e-125">STOSERVE.ICO</span></span> | <span data-ttu-id="0b41e-126">Ressource icône pour l’exécutable.</span><span class="sxs-lookup"><span data-stu-id="0b41e-126">The icon resource for the executable.</span></span>                                                                                     |
| <span data-ttu-id="0b41e-127">Serveurs. Manutention</span><span class="sxs-lookup"><span data-stu-id="0b41e-127">SERVER.H</span></span>     | <span data-ttu-id="0b41e-128">Fichier include pour l’objet C++ de contrôle serveur.</span><span class="sxs-lookup"><span data-stu-id="0b41e-128">The include file for the server control C++ object.</span></span>                                                                       |
| <span data-ttu-id="0b41e-129">Serveurs. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="0b41e-129">SERVER.CPP</span></span>   | <span data-ttu-id="0b41e-130">Fichier d’implémentation pour l’objet C++ de contrôle serveur.</span><span class="sxs-lookup"><span data-stu-id="0b41e-130">The implementation file for the server control C++ object.</span></span>                                                                |
| <span data-ttu-id="0b41e-131">Fabrique. Manutention</span><span class="sxs-lookup"><span data-stu-id="0b41e-131">FACTORY.H</span></span>    | <span data-ttu-id="0b41e-132">Fichier include pour les objets COM de la fabrique de classe du serveur.</span><span class="sxs-lookup"><span data-stu-id="0b41e-132">The include file for the server's class factory COM objects.</span></span>                                                              |
| <span data-ttu-id="0b41e-133">Fabrique. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="0b41e-133">FACTORY.CPP</span></span>  | <span data-ttu-id="0b41e-134">Fichier d’implémentation pour les fabriques de classe du serveur.</span><span class="sxs-lookup"><span data-stu-id="0b41e-134">The implementation file for the server's class factories.</span></span>                                                                 |
| <span data-ttu-id="0b41e-135">Entre. Manutention</span><span class="sxs-lookup"><span data-stu-id="0b41e-135">CONNECT.H</span></span>    | <span data-ttu-id="0b41e-136">Fichier include pour les classes énumérateur de point de connexion, point de connexion et énumérateur de connexion.</span><span class="sxs-lookup"><span data-stu-id="0b41e-136">The include file for the connection point enumerator, connection point, and connection enumerator classes.</span></span>                |
| <span data-ttu-id="0b41e-137">Entre. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="0b41e-137">CONNECT.CPP</span></span>  | <span data-ttu-id="0b41e-138">Fichier d’implémentation pour les objets énumérateur de point de connexion, point de connexion et énumérateur de connexion.</span><span class="sxs-lookup"><span data-stu-id="0b41e-138">The implementation file for the connection point enumerator, connection point, and connection enumerator objects.</span></span>         |
| <span data-ttu-id="0b41e-139">Imprimé. Manutention</span><span class="sxs-lookup"><span data-stu-id="0b41e-139">PAPER.H</span></span>      | <span data-ttu-id="0b41e-140">Fichier include pour la classe d’objets COM du colivre.</span><span class="sxs-lookup"><span data-stu-id="0b41e-140">The include file for the COPaper COM object class.</span></span>                                                                        |
| <span data-ttu-id="0b41e-141">Imprimé. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="0b41e-141">PAPER.CPP</span></span>    | <span data-ttu-id="0b41e-142">Le fichier d’implémentation pour la classe d’objets COM du colivre et les points de connexion.</span><span class="sxs-lookup"><span data-stu-id="0b41e-142">The implementation file for the COPaper COM object class and the connection points.</span></span>                                       |
| <span data-ttu-id="0b41e-143">STOSERVE. DSP</span><span class="sxs-lookup"><span data-stu-id="0b41e-143">STOSERVE.DSP</span></span> | <span data-ttu-id="0b41e-144">Microsoft Visual Studio fichier projet.</span><span class="sxs-lookup"><span data-stu-id="0b41e-144">Microsoft Visual Studio Project file.</span></span>                                                                                     |



 

<span data-ttu-id="0b41e-145">Les principales rubriques traitées dans cette présentation du code sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b41e-145">The major topics covered in this code tour are:</span></span>

-   <span data-ttu-id="0b41e-146">Méthodes de l’interface [**IPaper**](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="0b41e-146">The [**IPaper**](ipaper-methods.md) interface methods.</span></span>
-   <span data-ttu-id="0b41e-147">Utilisation par le biais de l’interface [**IPaperSink**](ipapersink-methods.md) pour les notifications client.</span><span class="sxs-lookup"><span data-stu-id="0b41e-147">COPaper's use of the [**IPaperSink**](ipapersink-methods.md) interface for client notifications.</span></span>
-   <span data-ttu-id="0b41e-148">[**Structures**](structures---stoserve.md) dans StoServe.</span><span class="sxs-lookup"><span data-stu-id="0b41e-148">[**Structures**](structures---stoserve.md) in StoServe.</span></span>
-   <span data-ttu-id="0b41e-149">[Considérations Unicode](unicode-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="0b41e-149">[Unicode considerations](unicode-considerations.md).</span></span>

 

 




