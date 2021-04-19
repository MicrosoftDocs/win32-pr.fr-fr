---
title: Utilisation de l’Assistant de plug-in de boutique en ligne avec Visual Studio
description: Utilisation de l’Assistant de plug-in de boutique en ligne avec Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Windows Media Player Online stores, plug-ins
- magasins en ligne, plug-ins
- types 1 magasins en ligne, plug-ins
- Windows Media Player Online stores, Assistant plug-in
- magasins en ligne, Assistant de plug-in
- tapez 1 magasins en ligne, Assistant de plug-in
- Windows Media Player Online stores, Visual Studio
- magasins en ligne, Visual Studio
- types 1 magasins en ligne, Visual Studio
- plug-ins, Windows Media Player Online stores
- plug-ins, magasins en ligne
- plug-ins, type 1 magasins en ligne
- plug-ins, Visual Studio
- plug-ins, Assistant de plug-in
- Plug-ins du lecteur Windows Media, type 1 magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne Windows Media Player
- Plug-ins du lecteur Windows Media, Visual Studio
- Plug-ins du lecteur Windows Media, Assistant plug-in
- Visual Studio, Assistant Windows Media Player stores Online
- Assistant de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c9aadbb9cef4b44cb421bf8a4737cc408c5220
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508964"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a>Utilisation de l’Assistant de plug-in de boutique en ligne avec Visual Studio

Après avoir installé les composants nécessaires, vous pouvez créer rapidement un plug-in qui servira de point de départ. Les étapes suivantes vous guident :

1.  Démarrez Microsoft Visual Studio.
2.  Dans le menu **fichier** , pointez sur **nouveau** , puis cliquez sur **projet**.
3.  Dans **types de projets**, cliquez sur **projets de Visual C++**.
4.  Dans **modèles**, cliquez sur **Assistant magasins en ligne du lecteur Windows Media**.
5.  Entrez un nom pour votre projet.
6.  Entrez un emplacement pour votre projet. Il s’agit du dossier dans lequel vos fichiers projet seront copiés.
7.  Cliquez sur **OK** pour démarrer l’Assistant.
8.  Sélectionnez **type 1 (intégration profonde)**, puis cliquez sur **suivant**.
9.  Entrez un nom convivial et un serveur de distribution de contenu. Cliquez sur **Terminer**.
10. Utilisez l’environnement de développement Visual Studio pour générer votre projet.
    > [!Note]  
    > Dans Windows Vista et versions ultérieures, le projet ne sera pas généré avec succès, sauf si vous exécutez Visual Studio avec un jeton d’accès administrateur complet. Cliquez avec le bouton droit sur le nom ou l’icône Visual Studio, puis cliquez sur **exécuter en tant qu’administrateur**.

     

Avant de tenter de générer le projet, veillez à configurer votre environnement de développement de façon à ce qu’il pointe vers les dossiers nommés include et lib où vous avez installé le SDK Windows. Le compilateur et l’éditeur de liens auront besoin d’accéder à certains des fichiers de ces dossiers.

Si vous avez exécuté l’utilitaire d’inscription Visual Studio fourni avec le SDK Windows, votre environnement de développement a probablement déjà été configuré pour pointer vers les dossiers include et lib SDK Windows. Dans le cas contraire, vous devez configurer manuellement votre environnement de développement.

Pour configurer manuellement Visual Studio, procédez comme suit.

1.  Dans le menu **Outils** , cliquez sur options.
2.  Cliquez sur **projets et solutions**, puis sur **Répertoires VC + +**.
3.  Sous **afficher les répertoires pour**, cliquez sur **inclure** les fichiers ou les **fichiers de bibliothèque**.
4.  Ajoutez les répertoires pour les fichiers requis.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création du plug-in pour un magasin de type 1 en ligne](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




