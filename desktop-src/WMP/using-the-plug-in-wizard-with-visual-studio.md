---
title: Utilisation de l’Assistant de plug-in avec Visual Studio
description: Utilisation de l’Assistant de plug-in avec Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Plug-ins du lecteur Windows Media, Visual Studio
- plug-ins, Visual Studio
- génération de plug-ins, Visual Studio
- Assistant de plug-in Windows Media Player, Visual Studio
- Visual Studio, Assistant de plug-in du lecteur Windows Media
- Assistant de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7f7db9bdc2a99a42f60c2faf38605e50e7dd3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310397"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a>Utilisation de l’Assistant de plug-in avec Visual Studio

Après avoir installé les composants nécessaires, vous pouvez créer rapidement un plug-in qui servira de point de départ. Les étapes suivantes vous guideront.

1.  Démarrez Microsoft Visual Studio.
2.  Dans le menu **fichier** , pointez sur **nouveau** , puis cliquez sur **projet**.
3.  Dans **types de projets**, sélectionnez **Visual C++ projets**.
4.  Dans **modèles**, sélectionnez **Assistant plug-in du lecteur Windows Media**.
5.  Entrez un nom pour votre projet.
6.  Entrez un emplacement pour votre projet. Il s’agit du dossier dans lequel vos fichiers projet seront copiés.
7.  Cliquez sur **OK** pour démarrer l’Assistant.
8.  Sélectionnez le type de plug-in que vous souhaitez créer.
9.  Complétez les boîtes de dialogue restantes dans l’Assistant.
10. Utilisez l’environnement de développement Visual Studio pour générer votre projet.
    > [!Note]  
    > Dans Windows Vista et versions ultérieures, le projet ne sera pas généré avec succès, sauf si vous exécutez Visual Studio avec un jeton d’accès administrateur complet. Cliquez avec le bouton droit sur le nom ou l’icône Visual Studio, puis cliquez sur **exécuter en tant qu’administrateur**.

     

Avant de tenter de générer le projet, veillez à configurer votre environnement de développement de façon à ce qu’il pointe vers les dossiers nommés include et lib où vous avez installé le SDK Windows. Le compilateur et l’éditeur de liens auront besoin d’accéder à certains des fichiers de ces dossiers.

Si vous avez exécuté l’utilitaire d’inscription Visual Studio fourni avec le SDK Windows, votre environnement de développement a probablement déjà été configuré pour pointer vers les dossiers include et lib SDK Windows. Dans le cas contraire, vous devez configurer manuellement votre environnement de développement.

Pour configurer manuellement Visual Studio, procédez comme suit.

1.  Dans le menu **Outils** , cliquez sur **Options**.
2.  Cliquez sur **projets et solutions**, puis sur **Répertoires VC + +**.
3.  Sous **afficher les répertoires pour**, cliquez sur **inclure** les fichiers ou les **fichiers de bibliothèque**.
4.  Ajoutez les répertoires pour les fichiers requis.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Génération d’un plug-in](building-a-plug-in.md)
</dt> </dl>

 

 




