---
title: Lecture des fichiers protégés
description: Lecture des fichiers protégés
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- Windows Media Format SDK, lire les fichiers protégés
- Windows Media Format SDK, fichiers protégés
- ASF (Advanced Systems Format), lire les fichiers protégés
- ASF (format des systèmes avancés), lire les fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- ASF (Advanced Systems Format), WMStubDRM. lib
- ASF (format avancé des systèmes), WMStubDRM. lib
- WMStubDRM. lib, lecture des fichiers protégés
- WMStubDRM. lib, fichiers protégés
- gestion des droits numériques (DRM), WMStubDRM. lib
- DRM (gestion des droits numériques), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b2110708a28daae1e86ba3dac2ea1f18ad16fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723410"
---
# <a name="reading-protected-files"></a><span data-ttu-id="61648-115">Lecture des fichiers protégés</span><span class="sxs-lookup"><span data-stu-id="61648-115">Reading Protected Files</span></span>

<span data-ttu-id="61648-116">La lecture d’un fichier protégé par DRM ou d’un flux réseau implique la tentative d’ouvrir le fichier (ou de se connecter au flux), puis de gérer les événements qui peuvent être envoyés à partir des composants DRM.</span><span class="sxs-lookup"><span data-stu-id="61648-116">Reading a DRM-protected file or network stream basically involves attempting to open the file (or connect to the stream) and then handling any events that might be sent from the DRM components.</span></span>

<span data-ttu-id="61648-117">Si un lecteur n’est pas compatible DRM (ne lie pas à une bibliothèque wmstubdrm. lib valide) l’appel de [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) échoue lorsqu’il tente d’ouvrir un fichier protégé et retourne \_ du \_ contenu protégé par le service NS \_ ou une erreur associée.</span><span class="sxs-lookup"><span data-stu-id="61648-117">If a player is not DRM-enabled (does not link to a valid wmstubdrm.lib library) the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) call fails when it tries to open a protected file and returns NS\_E\_PROTECTED\_CONTENT or some related error.</span></span>

<span data-ttu-id="61648-118">Quand une application compatible DRM tente d’ouvrir un fichier protégé par DRM, le composant DRM recherche automatiquement une licence valide dans le système local.</span><span class="sxs-lookup"><span data-stu-id="61648-118">When a DRM-enabled application attempts to open a DRM-protected file, the DRM component automatically searches the local system for a valid license.</span></span> <span data-ttu-id="61648-119">S’il en existe un, le composant DRM déchiffre automatiquement le fichier d’une manière totalement transparente pour l’application.</span><span class="sxs-lookup"><span data-stu-id="61648-119">If one is found, the DRM component automatically decrypts the file in a way that is completely transparent to the application.</span></span> <span data-ttu-id="61648-120">L’action qu’une application peut effectuer sur le fichier déchiffré dépend des droits spécifiés dans la licence.</span><span class="sxs-lookup"><span data-stu-id="61648-120">The action that an application may perform on the decrypted file depends on the rights specified in the license.</span></span> <span data-ttu-id="61648-121">Pour obtenir une description complète des droits possibles, consultez la documentation du kit de développement logiciel (SDK) Windows Media Rights Manager.</span><span class="sxs-lookup"><span data-stu-id="61648-121">For a full description of possible rights, see the Windows Media Rights Manager SDK documentation.</span></span>

<span data-ttu-id="61648-122">Si l’application ne dispose pas d’une licence valide pour un fichier, le lecteur reçoit une notification d’État du composant DRM.</span><span class="sxs-lookup"><span data-stu-id="61648-122">If the application does not have a valid license for a file, the player receives a status notification from the DRM component.</span></span> <span data-ttu-id="61648-123">L’application de lecteur peut ensuite lancer le processus d' [*acquisition de licence*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="61648-123">The player application can then initiate the [*license acquisition*](wmformat-glossary.md) process.</span></span> <span data-ttu-id="61648-124">Après la réception d’une licence valide, le fichier est accessible.</span><span class="sxs-lookup"><span data-stu-id="61648-124">After a valid license has been received, the file can be accessed.</span></span> <span data-ttu-id="61648-125">Les sections suivantes décrivent les tâches de base qu’une application doit effectuer lors de l’implémentation du processus d’acquisition de licence :</span><span class="sxs-lookup"><span data-stu-id="61648-125">The following sections describe the basic tasks that an application must perform in implementing the license acquisition process:</span></span>

-   [<span data-ttu-id="61648-126">Spécification des actions à effectuer</span><span class="sxs-lookup"><span data-stu-id="61648-126">Specifying the Actions To Be Performed</span></span>](specifying-the-actions-to-be-performed.md)
-   [<span data-ttu-id="61648-127">Gestion des événements d’acquisition de licence</span><span class="sxs-lookup"><span data-stu-id="61648-127">Handling License Acquisition Events</span></span>](handling-license-acquisition-events.md)
-   [<span data-ttu-id="61648-128">Individualiser des applications DRM</span><span class="sxs-lookup"><span data-stu-id="61648-128">Individualizing DRM Applications</span></span>](individualizing-drm-applications.md)
-   [<span data-ttu-id="61648-129">Gestion des événements d’individualisation</span><span class="sxs-lookup"><span data-stu-id="61648-129">Handling Individualization Events</span></span>](handling-individualization-events.md)

> [!Note]  
> <span data-ttu-id="61648-130">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="61648-130">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="61648-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="61648-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61648-132">**Fonctionnalités de Rights Management numérique**</span><span class="sxs-lookup"><span data-stu-id="61648-132">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="61648-133">**Liste des attributs DRM**</span><span class="sxs-lookup"><span data-stu-id="61648-133">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="61648-134">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="61648-134">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="61648-135">**Activation de la prise en charge de DRM**</span><span class="sxs-lookup"><span data-stu-id="61648-135">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




