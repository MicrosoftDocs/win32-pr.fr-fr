---
title: Compilation de l’exemple de projet
description: Compilation de l’exemple de projet
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Windows Media Player Online stores, compilation d’exemples de projets
- magasins en ligne, compilation d’exemples de projets
- types 2 magasins en ligne, compilation d’exemples de projets
- Magasins en ligne du lecteur Windows Media, exemples de projets
- magasins en ligne, exemples de projets
- types 2 magasins en ligne, exemples de projets
- Windows Media Player Online stores, Assistant projet
- magasins en ligne, Assistant projet
- type 2 magasins en ligne, Assistant projet
- plug-ins, Assistant projet
- Plug-ins du lecteur Windows Media, Assistant projet
- compilation d’exemples de projets
- exemples, type 2 magasins en ligne
- Assistant projet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ea2382e5852965b246f1ef303e5e70d160cb22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106545731"
---
# <a name="compiling-the-sample-project"></a>Compilation de l’exemple de projet

L’Assistant génère tous les fichiers dont vous avez besoin pour compiler l’exemple de projet. il n’est donc pas nécessaire de modifier les paramètres de projet par défaut. Dans Visual Studio, dans le menu **générer** , cliquez sur **générer la solution** pour générer et inscrire le composant com. Par défaut, la configuration de débogage est active.

> [!Note]  
> Dans Windows Vista et versions ultérieures, le projet ne sera pas généré avec succès, sauf si vous exécutez Visual Studio avec un jeton d’accès administrateur complet. Cliquez avec le bouton droit sur le nom ou l’icône Visual Studio, puis cliquez sur **exécuter en tant qu’administrateur**.

 

Avant de tenter de générer le projet, veillez à configurer votre environnement de développement de façon à ce qu’il pointe vers les dossiers nommés include et lib où vous avez installé le SDK Windows. Le compilateur et l’éditeur de liens auront besoin d’accéder à certains des fichiers de ces dossiers.

Si vous avez exécuté l’utilitaire d’inscription Visual Studio fourni avec le kit de développement logiciel (SDK) Windows Vista, votre environnement de développement a probablement déjà été configuré pour pointer vers les dossiers include et lib de SDK Windows. Dans le cas contraire, vous devez configurer manuellement votre environnement de développement.

Pour configurer manuellement Visual Studio, procédez comme suit.

1.  Dans le menu **Outils** , cliquez sur **Options**.
2.  Cliquez sur **projets et solutions**, puis sur **Répertoires VC + +**.
3.  Sous **afficher les répertoires pour**, cliquez sur **inclure** les fichiers ou les **fichiers de bibliothèque**.
4.  Ajoutez les répertoires pour les fichiers requis.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création du plug-in pour un magasin de type 2 en ligne](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




