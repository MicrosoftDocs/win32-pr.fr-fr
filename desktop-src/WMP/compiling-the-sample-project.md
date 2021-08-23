---
title: Compilation de l’exemple de Project
description: Compilation de l’exemple de Project
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Lecteur Windows Media des magasins en ligne, compilation d’exemples de projets
- magasins en ligne, compilation d’exemples de projets
- types 2 magasins en ligne, compilation d’exemples de projets
- Lecteur Windows Media des magasins en ligne, exemples de projets
- magasins en ligne, exemples de projets
- types 2 magasins en ligne, exemples de projets
- Lecteur Windows Media les magasins en ligne, assistant projet
- magasins en ligne, Assistant projet
- type 2 magasins en ligne, Assistant projet
- plug-ins, Assistant projet
- plug-ins Lecteur Windows Media, assistant projet
- compilation d’exemples de projets
- exemples, type 2 magasins en ligne
- Assistant projet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55b2f5a4b6d29b227b08654cfcde2a89cc97b224fc756251ae9554f029f22416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763939"
---
# <a name="compiling-the-sample-project"></a>Compilation de l’exemple de Project

L’Assistant génère tous les fichiers dont vous avez besoin pour compiler l’exemple de projet. il n’est donc pas nécessaire de modifier les paramètres de projet par défaut. dans Visual Studio, dans le menu **générer** , cliquez sur **générer la Solution** pour générer et inscrire le composant COM. Par défaut, la configuration de débogage est active.

> [!Note]  
> dans Windows Vista et versions ultérieures, le projet ne sera pas généré avec succès, à moins que vous n’exécutiez Visual Studio avec un jeton d’accès administrateur complet. cliquez avec le bouton droit sur le nom ou l’icône Visual Studio, puis cliquez sur **exécuter en tant qu’administrateur**.

 

avant de tenter de générer le projet, veillez à configurer votre environnement de développement de façon à ce qu’il pointe vers les dossiers nommés include et Lib où vous avez installé le SDK Windows. Le compilateur et l’éditeur de liens auront besoin d’accéder à certains des fichiers de ces dossiers.

si vous avez exécuté l’utilitaire d’inscription Visual Studio fourni avec le kit de développement logiciel (SDK) Windows Vista, votre environnement de développement a probablement déjà été configuré pour pointer vers les dossiers include et Lib SDK Windows. Dans le cas contraire, vous devez configurer manuellement votre environnement de développement.

pour configurer manuellement Visual Studio, procédez comme suit.

1.  Dans le menu **Outils** , cliquez sur **Options**.
2.  cliquez sur **projets et Solutions**, puis sur **VC++ répertoires**.
3.  Sous **afficher les répertoires pour**, cliquez sur **inclure** les fichiers ou les **fichiers de bibliothèque**.
4.  Ajoutez les répertoires pour les fichiers requis.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création du plug-in pour un magasin de type 2 en ligne](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




