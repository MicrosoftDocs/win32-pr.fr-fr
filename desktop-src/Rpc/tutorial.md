---
title: Didacticiel
description: Ce didacticiel vous guide tout au long des étapes nécessaires à la création d’une application distribuée simple, à un seul client et à un seul serveur à partir d’une application autonome existante.
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- RPC appel de procédure distante, didacticiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c19b0d8ec3b3eb55cf29ccfd87eca43775c2ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029575"
---
# <a name="tutorial"></a><span data-ttu-id="bfeab-104">Didacticiel</span><span class="sxs-lookup"><span data-stu-id="bfeab-104">Tutorial</span></span>

<span data-ttu-id="bfeab-105">Ce didacticiel vous guide tout au long des étapes nécessaires à la création d’une application distribuée simple, à un seul client et à un seul serveur à partir d’une application autonome existante.</span><span class="sxs-lookup"><span data-stu-id="bfeab-105">This tutorial takes you through the steps required to create a simple, single-client, single-server distributed application from an existing standalone application.</span></span> <span data-ttu-id="bfeab-106">Ces étapes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="bfeab-106">These steps are:</span></span>

-   <span data-ttu-id="bfeab-107">Créer des fichiers de définition d’interface et de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="bfeab-107">Create interface definition and application configuration files.</span></span>
-   <span data-ttu-id="bfeab-108">Utilisez le compilateur MIDL pour générer des stubs client et serveur en langage C à partir de ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="bfeab-108">Use the MIDL compiler to generate C-language client and server stubs and headers from those files.</span></span>
-   <span data-ttu-id="bfeab-109">Écrire une application cliente qui gère sa connexion au serveur.</span><span class="sxs-lookup"><span data-stu-id="bfeab-109">Write a client application that manages its connection to the server.</span></span>
-   <span data-ttu-id="bfeab-110">Écrivez une application serveur qui contient les procédures distantes réelles.</span><span class="sxs-lookup"><span data-stu-id="bfeab-110">Write a server application that contains the actual remote procedures.</span></span>
-   <span data-ttu-id="bfeab-111">Compilez et liez ces fichiers à la bibliothèque Runtime RPC pour produire l’application distribuée.</span><span class="sxs-lookup"><span data-stu-id="bfeab-111">Compile and link these files to the RPC run-time library to produce the distributed application.</span></span>

<span data-ttu-id="bfeab-112">L’application cliente transmet une chaîne de caractères au serveur dans un appel de procédure distante, et le serveur imprime la chaîne « Hello, World » à sa sortie standard.</span><span class="sxs-lookup"><span data-stu-id="bfeab-112">The client application passes a character string to the server in a remote procedure call, and the server prints the string "Hello, World" to its standard output.</span></span>

<span data-ttu-id="bfeab-113">Les fichiers sources complets de cet exemple d’application, avec du code supplémentaire pour gérer l’entrée de la ligne de commande et pour sortir les différents messages d’état de l’utilisateur, se trouvent dans le \\ répertoire RPC Hello du kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="bfeab-113">The complete source files for this example application, with additional code to handle command-line input and to output various status messages to the user, are in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="bfeab-114">Cette section présente la discussion dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="bfeab-114">This section presents its discussion in the following topics:</span></span>

-   [<span data-ttu-id="bfeab-115">Application autonome</span><span class="sxs-lookup"><span data-stu-id="bfeab-115">The Standalone Application</span></span>](the-standalone-application.md)
-   [<span data-ttu-id="bfeab-116">Définition de l’interface</span><span class="sxs-lookup"><span data-stu-id="bfeab-116">Defining the Interface</span></span>](defining-the-interface.md)
-   [<span data-ttu-id="bfeab-117">Génération de l’UUID</span><span class="sxs-lookup"><span data-stu-id="bfeab-117">Generating the UUID</span></span>](generating-the-uuid.md)
-   [<span data-ttu-id="bfeab-118">Fichier IDL</span><span class="sxs-lookup"><span data-stu-id="bfeab-118">The IDL File</span></span>](the-idl-file.md)
-   [<span data-ttu-id="bfeab-119">Fichier ACF</span><span class="sxs-lookup"><span data-stu-id="bfeab-119">The ACF File</span></span>](the-acf-file.md)
-   [<span data-ttu-id="bfeab-120">Génération des fichiers stub</span><span class="sxs-lookup"><span data-stu-id="bfeab-120">Generating the Stub Files</span></span>](generating-the-stub-files.md)
-   [<span data-ttu-id="bfeab-121">L’application cliente</span><span class="sxs-lookup"><span data-stu-id="bfeab-121">The Client Application</span></span>](the-client-application.md)
-   [<span data-ttu-id="bfeab-122">Application serveur</span><span class="sxs-lookup"><span data-stu-id="bfeab-122">The Server Application</span></span>](the-server-application.md)
-   [<span data-ttu-id="bfeab-123">Arrêt de l’application serveur</span><span class="sxs-lookup"><span data-stu-id="bfeab-123">Stopping the Server Application</span></span>](stopping-the-server-application.md)
-   [<span data-ttu-id="bfeab-124">Compilation et liaison</span><span class="sxs-lookup"><span data-stu-id="bfeab-124">Compiling and Linking</span></span>](compiling-and-linking.md)
-   [<span data-ttu-id="bfeab-125">Exécution de l’application</span><span class="sxs-lookup"><span data-stu-id="bfeab-125">Running the Application</span></span>](running-the-application.md)

 

 




