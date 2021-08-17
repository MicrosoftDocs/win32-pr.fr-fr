---
title: Utilisation de l’Assistant de plug-in avec Visual Studio
description: Utilisation de l’Assistant de plug-in avec Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- plug-ins Lecteur Windows Media, Visual Studio
- plug-ins, Visual Studio
- génération de plug-ins, Visual Studio
- Lecteur Windows Media Assistant de plug-in, Visual Studio
- Visual Studio, Lecteur Windows Media assistant de Plug-in
- Assistant de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1534d084d2c57d3546427db59274d1bd135bc66e8bf396906ff7776cae9a370f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134332"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a>Utilisation de l’Assistant de plug-in avec Visual Studio

Après avoir installé les composants nécessaires, vous pouvez créer rapidement un plug-in qui servira de point de départ. Les étapes suivantes vous guideront.

1.  Démarrez Microsoft Visual Studio.
2.  Dans le menu **fichier** , pointez sur **nouveau** , puis cliquez sur **Project**.
3.  dans **Types de Project**, sélectionnez **Visual C++ projets**.
4.  dans **modèles**, sélectionnez **Lecteur Windows Media assistant de Plug-** in.
5.  Entrez un nom pour votre projet.
6.  Entrez un emplacement pour votre projet. Il s’agit du dossier dans lequel vos fichiers projet seront copiés.
7.  Cliquez sur **OK** pour démarrer l’Assistant.
8.  Sélectionnez le type de plug-in que vous souhaitez créer.
9.  Complétez les boîtes de dialogue restantes dans l’Assistant.
10. utilisez l’environnement de développement Visual Studio pour générer votre projet.
    > [!Note]  
    > dans Windows Vista et versions ultérieures, le projet ne sera pas généré avec succès, à moins que vous n’exécutiez Visual Studio avec un jeton d’accès administrateur complet. cliquez avec le bouton droit sur le nom ou l’icône Visual Studio, puis cliquez sur **exécuter en tant qu’administrateur**.

     

avant de tenter de générer le projet, veillez à configurer votre environnement de développement de façon à ce qu’il pointe vers les dossiers nommés include et Lib où vous avez installé le SDK Windows. Le compilateur et l’éditeur de liens auront besoin d’accéder à certains des fichiers de ces dossiers.

si vous avez exécuté l’utilitaire d’inscription Visual Studio qui est fourni avec le SDK Windows, votre environnement de développement a probablement déjà été configuré pour pointer vers les dossiers include et Lib SDK Windows. Dans le cas contraire, vous devez configurer manuellement votre environnement de développement.

pour configurer manuellement Visual Studio, procédez comme suit.

1.  Dans le menu **Outils** , cliquez sur **Options**.
2.  cliquez sur **projets et Solutions**, puis sur **VC++ répertoires**.
3.  Sous **afficher les répertoires pour**, cliquez sur **inclure** les fichiers ou les **fichiers de bibliothèque**.
4.  Ajoutez les répertoires pour les fichiers requis.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Génération d’un plug-in](building-a-plug-in.md)
</dt> </dl>

 

 




