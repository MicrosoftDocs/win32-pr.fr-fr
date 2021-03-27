---
description: Cette rubrique explique comment utiliser le vérificateur de type de fichier fourni dans le kit de développement logiciel (SDK) Windows 7.
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: Utilisation du vérificateur de type de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f083897499f972f945867a0c02318df192e734d9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104211139"
---
# <a name="how-to-use-the-file-type-verifier"></a>Utilisation du vérificateur de type de fichier

Cette rubrique explique comment utiliser le vérificateur de type de fichier fourni dans le kit de [développement logiciel (SDK) Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Si votre programme crée des types de fichiers avec lesquels les utilisateurs sont censés interagir à partir du shell Windows (généralement stocké dans le dossier connu d’un utilisateur tel que **Mes documents**), il est très important de tester votre application et de vérifier que les fichiers qu’elle crée sont correctement enregistrés et de fournir une expérience utilisateur de haute qualité lors de la navigation et de la recherche de fichiers. Cela est particulièrement important si vous prévoyez que les utilisateurs exécutent vos applications sur Windows 7, qui s’appuie sur des gestionnaires de types de fichiers de haute qualité pour la plupart des fonctionnalités de l’interpréteur de commandes.

Pour vérifier votre type de fichier à l’aide du vérificateur de type de fichier, procédez comme suit.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Installez l’application dans votre environnement de test et copiez le vérificateur de type de fichier dans cet environnement. Le vérificateur de type de fichier est disponible dans le [Kit de développement logiciel (SDK) Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

### <a name="step-2"></a>Étape 2 :

Utilisez votre application pour créer un fichier à tester.

### <a name="step-3"></a>Étape 3 :

Démarrez le vérificateur de type de fichier.

### <a name="step-4"></a>Étape 4 :

Sélectionnez la catégorie pour votre type de fichier, comme illustré dans la capture d’écran suivante.

![Capture d’écran montrant la fonction glisser-déplacer.](images/file-assoc/filetypeverifier1.png)

La sélection de catégorie détermine l’ensemble des tests qui seront exécutés par l’outil. Si votre type peut appartenir à plusieurs catégories (par exemple, un fichier TIF peut être une image ou un document en fonction du contenu), exécutez à nouveau l’outil avec chaque catégorie appropriée.

### <a name="step-5"></a>Étape 5 :

À l’aide de l’Explorateur Windows, localisez un fichier à tester et utilisez la souris pour le faire glisser vers la cible dans le vérificateur de type de fichier, comme illustré dans la capture d’écran suivante.

![capture d’écran montrant la fonction glisser-déplacer](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a>Étape 6 :

Attendez que l’outil de vérification de type de fichier parcoure une série de tests. La progression du test est indiquée par la barre de progression, comme dans la capture d’écran suivante.

![capture d’écran montrant la barre de progression](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a>Étape 7 :

Examinez le résumé des résultats de vos tests de type de fichier de document, comme illustré dans la capture d’écran suivante.

![capture d’écran montrant le résumé des résultats](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a>Étape 8 :

Cliquez sur l’un des résultats de la page Résumé pour afficher le journal détaillé. Un exemple de journal pour un gestionnaire d’aperçus est illustré dans la capture d’écran suivante.

![capture d’écran montrant le journal du gestionnaire d’aperçus](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a>Étape 9 :

Pour enregistrer une copie du fichier journal, cliquez sur **enregistrer le fichier journal** en bas de l’affichage du journal et choisissez un emplacement approprié pour le stocker sur votre ordinateur.

### <a name="step-10"></a>Étape 10 :

Si des erreurs sont signalées, apportez les modifications appropriées à votre application et réexécutez l’outil pour vérifier que les échecs ne s’afficheront plus dans les tests. Si des avertissements sont signalés, évaluez-les et déterminez s’ils sont pertinents pour votre type de fichier particulier et apportez les modifications appropriées à votre application si nécessaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows 7, SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 



