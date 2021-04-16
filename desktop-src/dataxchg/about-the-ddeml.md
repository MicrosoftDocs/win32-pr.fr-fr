---
title: À propos de DDEML
description: Cette rubrique traite de l’échange dynamique de données.
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- Interface utilisateur Windows, échange dynamique de données (DDE)
- Échange dynamique de données (DDE), à propos de
- DDE (échange dynamique de données), à propos de
- échange de données, échange dynamique de données (DDE)
- Interface utilisateur Windows, bibliothèque de gestion des échange dynamique de données (DDEML)
- Bibliothèque de gestion des échange dynamique de données (DDEML), à propos de
- DDEML (bibliothèque de gestion échange dynamique de données), à propos de
- échange de données, bibliothèque de gestion des échange dynamique de données (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ed77565c8b4e20841ad2ef80ae84c1f5c39724
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507447"
---
# <a name="about-the-ddeml"></a><span data-ttu-id="65925-111">À propos de DDEML</span><span class="sxs-lookup"><span data-stu-id="65925-111">About the DDEML</span></span>

<span data-ttu-id="65925-112">Échange dynamique de données (DDE) diffère du mécanisme de transfert de données du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="65925-112">Dynamic Data Exchange (DDE) differs from the clipboard data-transfer mechanism.</span></span> <span data-ttu-id="65925-113">L’une des différences est que le presse-papiers est presque toujours utilisé comme réponse ponctuelle à une action spécifique de l’utilisateur, par exemple en cliquant sur **coller** à partir d’un menu.</span><span class="sxs-lookup"><span data-stu-id="65925-113">One difference is that the clipboard is almost always used as a one-time response to a specific action by the user — such as clicking **Paste** from a menu.</span></span> <span data-ttu-id="65925-114">Bien que l’échange DDE puisse également être initié par un utilisateur, il continue généralement sans l’intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="65925-114">Although DDE can also be initiated by a user, it typically continues without the user's further involvement.</span></span>

<span data-ttu-id="65925-115">La bibliothèque de gestion des échange dynamique de données (DDEML) fournit une interface qui simplifie la tâche d’ajout de la fonctionnalité DDE à une application.</span><span class="sxs-lookup"><span data-stu-id="65925-115">The Dynamic Data Exchange Management Library (DDEML) provides an interface that simplifies the task of adding DDE capability to an application.</span></span> <span data-ttu-id="65925-116">Au lieu d’envoyer, de publier et de traiter des messages DDE directement, une application utilise les fonctions fournies par le DDEML pour gérer les conversations DDE.</span><span class="sxs-lookup"><span data-stu-id="65925-116">Instead of sending, posting, and processing DDE messages directly, an application uses the functions provided by the DDEML to manage DDE conversations.</span></span> <span data-ttu-id="65925-117">Une conversation DDE est l’interaction entre les applications client et serveur.</span><span class="sxs-lookup"><span data-stu-id="65925-117">A DDE conversation is the interaction between client and server applications.</span></span> <span data-ttu-id="65925-118">Le DDEML fournit également un moyen de gérer les chaînes et les données partagées entre les applications DDE.</span><span class="sxs-lookup"><span data-stu-id="65925-118">The DDEML also provides a means for managing the strings and data shared among DDE applications.</span></span> <span data-ttu-id="65925-119">Au lieu d’utiliser des atomes et des pointeurs vers des objets mémoire partagés, les applications DDE créent et échangent des handles de chaîne, qui identifient les chaînes et les handles de données qui identifient les objets DDE.</span><span class="sxs-lookup"><span data-stu-id="65925-119">Instead of using atoms and pointers to shared memory objects, DDE applications create and exchange string handles, which identify strings, and data handles, which identify DDE objects.</span></span> <span data-ttu-id="65925-120">DDEML fournit une fonction ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) qui permet à une application serveur d’inscrire les noms de service qu’elle prend en charge.</span><span class="sxs-lookup"><span data-stu-id="65925-120">The DDEML provides a function ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) that enables a server application to register the service names it supports.</span></span> <span data-ttu-id="65925-121">Les noms de service sont ensuite diffusés à d’autres applications dans le système, qui utilisent les noms pour se connecter au serveur.</span><span class="sxs-lookup"><span data-stu-id="65925-121">The service names are then broadcast to other applications in the system, which use the names to connect to the server.</span></span> <span data-ttu-id="65925-122">Le DDEML garantit également la compatibilité entre les applications DDE en exigeant qu’elles implémentent le protocole DDE de manière cohérente.</span><span class="sxs-lookup"><span data-stu-id="65925-122">The DDEML also ensures compatibility among DDE applications by requiring them to implement the DDE protocol in a consistent manner.</span></span>

<span data-ttu-id="65925-123">Les applications existantes utilisant le protocole DDE basé sur des messages sont entièrement compatibles avec celles qui utilisent DDEML. autrement dit, une application utilisant un DDE basé sur des messages peut établir des conversations et exécuter des transactions avec des applications à l’aide de DDEML.</span><span class="sxs-lookup"><span data-stu-id="65925-123">Existing applications using the message-based DDE protocol are fully compatible with those that use the DDEML; that is, an application using message-based DDE can establish conversations and perform transactions with applications using the DDEML.</span></span> <span data-ttu-id="65925-124">Au lieu d’utiliser des messages DDE dans votre nouvelle application, tirez parti du DDEML et des nombreuses améliorations qu’il offre.</span><span class="sxs-lookup"><span data-stu-id="65925-124">Instead of using DDE messages in your new application, take advantage of the DDEML and the many improvements it offers.</span></span>

<span data-ttu-id="65925-125">Pour utiliser DDEML, vous devez inclure DDEML. Fichier d’en-tête H dans vos fichiers sources, lien avec USER32. Fichier LIB, et assurez-vous que le fichier DDEML.DLL réside dans le chemin d’accès du système.</span><span class="sxs-lookup"><span data-stu-id="65925-125">To use the DDEML, you must include the DDEML.H header file in your source files, link with the USER32.LIB file, and ensure that the DDEML.DLL file resides in the system's path.</span></span>

<span data-ttu-id="65925-126">Chaque fois qu’une fonction DDEML échoue, une application peut appeler la fonction [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) pour déterminer la cause de l’échec.</span><span class="sxs-lookup"><span data-stu-id="65925-126">Whenever a DDEML function fails, an application can call the [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) function to determine the cause of the failure.</span></span> <span data-ttu-id="65925-127">**DdeGetLastError** retourne une valeur d’erreur qui spécifie la cause de l’erreur la plus récente.</span><span class="sxs-lookup"><span data-stu-id="65925-127">**DdeGetLastError** returns an error value that specifies the cause of the most recent error.</span></span>

 

 




