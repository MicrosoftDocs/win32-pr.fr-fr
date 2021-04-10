---
title: Personnalisation de l’exemple de projet
description: Personnalisation de l’exemple de projet
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Windows Media Player Online stores, personnalisation des exemples de projets
- magasins en ligne, personnalisation des exemples de projets
- types 2 magasins en ligne, personnalisation des exemples de projets
- Magasins en ligne du lecteur Windows Media, exemples de projets
- magasins en ligne, exemples de projets
- types 2 magasins en ligne, exemples de projets
- personnalisation des exemples de projets
- exemples, type 2 magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeec3ebcb74304cd5181783e9c457d6a149b0cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940251"
---
# <a name="customizing-the-sample-project"></a><span data-ttu-id="824e5-111">Personnalisation de l’exemple de projet</span><span class="sxs-lookup"><span data-stu-id="824e5-111">Customizing the Sample Project</span></span>

<span data-ttu-id="824e5-112">Lorsque vous créez votre propre magasin en ligne, vous pouvez modifier les implémentations des méthodes suivantes dans le fichier nommé YourProject. cpp :</span><span class="sxs-lookup"><span data-stu-id="824e5-112">When creating your own online store, you will want to change the implementations of the following methods in the file named YourProject.cpp:</span></span>

-   <span data-ttu-id="824e5-113">**CYourProject :: allowPlay**.</span><span class="sxs-lookup"><span data-stu-id="824e5-113">**CYourProject::allowPlay**.</span></span> <span data-ttu-id="824e5-114">Utilisez cette fonction pour appliquer vos règles d’entreprise afin d’autoriser la lecture du contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="824e5-114">Use this function to apply your business rules for permitting playback of protected content.</span></span>
-   <span data-ttu-id="824e5-115">**CYourProject :: allow cdburn**.</span><span class="sxs-lookup"><span data-stu-id="824e5-115">**CYourProject::allow CDBurn**.</span></span> <span data-ttu-id="824e5-116">Utilisez cette fonction pour appliquer vos règles d’entreprise pour permettre aux utilisateurs de copier du contenu protégé sur un CD.</span><span class="sxs-lookup"><span data-stu-id="824e5-116">Use this function to apply your business rules for allowing users to copy protected content to a CD.</span></span>
-   <span data-ttu-id="824e5-117">**CYourProject :: allowPDATransfer**.</span><span class="sxs-lookup"><span data-stu-id="824e5-117">**CYourProject::allowPDATransfer**.</span></span> <span data-ttu-id="824e5-118">Utilisez cette fonction pour appliquer vos règles d’entreprise pour permettre aux utilisateurs de transférer du contenu protégé vers un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="824e5-118">Use this function to apply your business rules for allowing users to transfer protected content to a portable device.</span></span>
-   <span data-ttu-id="824e5-119">**CYourProject :: startBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="824e5-119">**CYourProject::startBackgroundProcessing**.</span></span> <span data-ttu-id="824e5-120">Utilisez cette fonction pour lancer les tâches de traitement en arrière-plan dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="824e5-120">Use this function to initiate any background processing tasks you require.</span></span> <span data-ttu-id="824e5-121">Par exemple, vous pouvez l’utiliser comme opportunité de vérifier les licences expirées.</span><span class="sxs-lookup"><span data-stu-id="824e5-121">For example, you might use this as an opportunity to check for expired licenses.</span></span>
-   <span data-ttu-id="824e5-122">**CYourProject ::D eviceavailable**.</span><span class="sxs-lookup"><span data-stu-id="824e5-122">**CYourProject::deviceAvailable**.</span></span> <span data-ttu-id="824e5-123">Utilisez cette fonction pour lancer des tâches liées à un appareil connecté.</span><span class="sxs-lookup"><span data-stu-id="824e5-123">Use this function to initiate any tasks related to a connected device.</span></span>
-   <span data-ttu-id="824e5-124">**CYourProject ::P repareforsync**.</span><span class="sxs-lookup"><span data-stu-id="824e5-124">**CYourProject::prepareForSync**.</span></span> <span data-ttu-id="824e5-125">Utilisez cette fonction pour effectuer les tâches nécessaires juste avant de synchroniser des médias numériques sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="824e5-125">Use this function to perform necessary tasks just before synchronizing digital media to the device.</span></span>
-   <span data-ttu-id="824e5-126">**CYourProject :: serviceEvent**.</span><span class="sxs-lookup"><span data-stu-id="824e5-126">**CYourProject::serviceEvent**.</span></span> <span data-ttu-id="824e5-127">Utilisez cette fonction pour commencer et terminer les tâches que vous souhaitez exécuter lorsque votre magasin en ligne est le magasin actif.</span><span class="sxs-lookup"><span data-stu-id="824e5-127">Use this function to begin and end tasks that you want to run when your online store is the active one.</span></span>
-   <span data-ttu-id="824e5-128">**CYourProject :: stopBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="824e5-128">**CYourProject::stopBackgroundProcessing**.</span></span> <span data-ttu-id="824e5-129">Utilisez cette fonction pour arrêter les tâches de traitement en arrière-plan que vous avez démarrées lorsque le lecteur Windows Media a appelé **CYourProject :: startBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="824e5-129">Use this function to stop any background processing tasks you started when Windows Media Player called **CYourProject::startBackgroundProcessing**.</span></span>

## <a name="working-with-media-and-playlist-objects"></a><span data-ttu-id="824e5-130">Utilisation d’objets multimédias et playlists</span><span class="sxs-lookup"><span data-stu-id="824e5-130">Working with Media and Playlist Objects</span></span>

<span data-ttu-id="824e5-131">La méthode **allowPlay** fournit un pointeur vers l’interface **IWMPMedia** en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="824e5-131">The **allowPlay** method provides a pointer to the **IWMPMedia** interface as a parameter.</span></span> <span data-ttu-id="824e5-132">Cette interface est l’interface du lecteur Windows Media qui représente les objets multimédias.</span><span class="sxs-lookup"><span data-stu-id="824e5-132">This interface is the Windows Media Player interface that represents media objects.</span></span> <span data-ttu-id="824e5-133">En appelant les méthodes sur cette interface, vous pouvez utiliser les attributs et les propriétés d’un élément multimédia individuel.</span><span class="sxs-lookup"><span data-stu-id="824e5-133">By calling the methods on this interface, you can work with the attributes and properties of an individual media item.</span></span>

<span data-ttu-id="824e5-134">Les méthodes **allowCDBurn** et **allowPDATransfer** fournissent un pointeur vers l’interface **IWMPPlaylist** en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="824e5-134">The **allowCDBurn** and **allowPDATransfer** methods provide a pointer to the **IWMPPlaylist** interface as a parameter.</span></span> <span data-ttu-id="824e5-135">Cette interface est l’interface du lecteur Windows Media qui représente les objets de sélection.</span><span class="sxs-lookup"><span data-stu-id="824e5-135">This interface is the Windows Media Player interface that represents playlist objects.</span></span> <span data-ttu-id="824e5-136">En appelant les méthodes sur cette interface, vous pouvez utiliser les attributs et les propriétés d’une sélection, ajouter des éléments à une sélection ou supprimer des éléments d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="824e5-136">By calling the methods on this interface, you can work with the attributes and properties of a playlist, add items to a playlist, or remove items from a playlist.</span></span>

<span data-ttu-id="824e5-137">Pour savoir comment supprimer un élément d’une sélection par programme, consultez l’implémentation de **CAllowBaseDialog <T> :: OnRemoveMediaFromPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="824e5-137">To learn how to remove an item from a playlist programmatically, see the implementation of **CAllowBaseDialog<T>::OnRemoveMediaFromPlaylist**.</span></span> <span data-ttu-id="824e5-138">Pour en savoir plus sur l’utilisation des objets multimédias et playlist, consultez [modèle objet Player pour les langages de script](player-object-model-for-scripting-languages.md).</span><span class="sxs-lookup"><span data-stu-id="824e5-138">To learn more about working with media and playlist objects, see [Player Object Model for Scripting Languages](player-object-model-for-scripting-languages.md).</span></span>

## <a name="code-that-can-be-removed"></a><span data-ttu-id="824e5-139">Code pouvant être supprimé</span><span class="sxs-lookup"><span data-stu-id="824e5-139">Code That Can Be Removed</span></span>

<span data-ttu-id="824e5-140">Vous souhaiterez probablement supprimer le code qui ouvre les boîtes de dialogue, car il est peu probable que vous souhaitiez que les utilisateurs décident des éléments multimédias qui peuvent être lus ou copiés.</span><span class="sxs-lookup"><span data-stu-id="824e5-140">You will probably want to remove the code that opens dialog boxes because it is unlikely that you will want users deciding which media items can be played or copied.</span></span> <span data-ttu-id="824e5-141">À partir de YourProject. h, supprimez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="824e5-141">From YourProject.h, remove the following code:</span></span>

-   <span data-ttu-id="824e5-142">Déclaration de **CAllowBaseDialog**.</span><span class="sxs-lookup"><span data-stu-id="824e5-142">The declaration of **CAllowBaseDialog**.</span></span>
-   <span data-ttu-id="824e5-143">Déclaration de **CAllowBurnDialog**.</span><span class="sxs-lookup"><span data-stu-id="824e5-143">The declaration of **CAllowBurnDialog**.</span></span>
-   <span data-ttu-id="824e5-144">Déclaration de **CAllowTransferDialog**.</span><span class="sxs-lookup"><span data-stu-id="824e5-144">The declaration of **CAllowTransferDialog**.</span></span>

<span data-ttu-id="824e5-145">À partir de YourProject. cpp, supprimez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="824e5-145">From YourProject.cpp, remove the following code:</span></span>

-   <span data-ttu-id="824e5-146">Implémentation de **CAllowBaseDialog <T> :: OnInitDialog**.</span><span class="sxs-lookup"><span data-stu-id="824e5-146">The implementation of **CAllowBaseDialog<T>::OnInitDialog**.</span></span>
-   <span data-ttu-id="824e5-147">Implémentation de **CAllowBaseDialog <T> :: OnRemoveMediaFromPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="824e5-147">The implementation of **CAllowBaseDialog<T>::OnRemoveMediaFromPlaylist**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="824e5-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="824e5-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="824e5-149">**Création du plug-in pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="824e5-149">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




