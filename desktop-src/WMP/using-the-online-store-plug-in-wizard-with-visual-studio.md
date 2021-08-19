---
title: Utilisation de l’Assistant de plug-in de boutique en ligne avec Visual Studio
description: Utilisation de l’Assistant de plug-in de boutique en ligne avec Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Lecteur Windows Media des magasins en ligne, plug-ins
- magasins en ligne, plug-ins
- types 1 magasins en ligne, plug-ins
- Lecteur Windows Media magasins en ligne, assistant de plug-in
- magasins en ligne, Assistant de plug-in
- tapez 1 magasins en ligne, Assistant de plug-in
- Lecteur Windows Media des magasins en ligne, Visual Studio
- magasins en ligne, Visual Studio
- tapez 1 magasins en ligne, Visual Studio
- plug-ins, Lecteur Windows Media magasins en ligne
- plug-ins, magasins en ligne
- plug-ins, type 1 magasins en ligne
- plug-ins, Visual Studio
- plug-ins, Assistant de plug-in
- Lecteur Windows Media les plug-ins, tapez 1 magasins en ligne
- plug-ins Lecteur Windows Media, magasins en ligne
- plug-ins Lecteur Windows Media, Lecteur Windows Media les magasins en ligne
- plug-ins Lecteur Windows Media, Visual Studio
- plug-ins Lecteur Windows Media, assistant de plug-in
- Visual Studio, Lecteur Windows Media assistant magasins en ligne
- Assistant de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd53a1b83f817e4cfcc7dede80361f56f46ea41da8730f4396330c12af05c73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830680"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a>Utilisation de l’Assistant de plug-in de boutique en ligne avec Visual Studio

Après avoir installé les composants nécessaires, vous pouvez créer rapidement un plug-in qui servira de point de départ. Les étapes suivantes vous guident :

1.  Démarrez Microsoft Visual Studio.
2.  Dans le menu **fichier** , pointez sur **nouveau** , puis cliquez sur **Project**.
3.  dans **Types de Project**, cliquez sur **Visual C++ projets**.
4.  dans **modèles**, cliquez sur **Lecteur Windows Media assistant magasins en ligne**.
5.  Entrez un nom pour votre projet.
6.  Entrez un emplacement pour votre projet. Il s’agit du dossier dans lequel vos fichiers projet seront copiés.
7.  Cliquez sur **OK** pour démarrer l’Assistant.
8.  Sélectionnez **type 1 (intégration profonde)**, puis cliquez sur **suivant**.
9.  Entrez un nom convivial et un serveur de distribution de contenu. Cliquez sur **Terminer**.
10. utilisez l’environnement de développement Visual Studio pour générer votre projet.
    > [!Note]  
    > dans Windows Vista et versions ultérieures, le projet ne sera pas généré avec succès, à moins que vous n’exécutiez Visual Studio avec un jeton d’accès administrateur complet. cliquez avec le bouton droit sur le nom ou l’icône Visual Studio, puis cliquez sur **exécuter en tant qu’administrateur**.

     

avant de tenter de générer le projet, veillez à configurer votre environnement de développement de façon à ce qu’il pointe vers les dossiers nommés include et Lib où vous avez installé le SDK Windows. Le compilateur et l’éditeur de liens auront besoin d’accéder à certains des fichiers de ces dossiers.

si vous avez exécuté l’utilitaire d’inscription Visual Studio qui est fourni avec le SDK Windows, votre environnement de développement a probablement déjà été configuré pour pointer vers les dossiers include et Lib SDK Windows. Dans le cas contraire, vous devez configurer manuellement votre environnement de développement.

pour configurer manuellement Visual Studio, procédez comme suit.

1.  Dans le menu **Outils** , cliquez sur options.
2.  cliquez sur **projets et Solutions**, puis sur **VC++ répertoires**.
3.  Sous **afficher les répertoires pour**, cliquez sur **inclure** les fichiers ou les **fichiers de bibliothèque**.
4.  Ajoutez les répertoires pour les fichiers requis.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création du plug-in pour un magasin de type 1 en ligne](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




