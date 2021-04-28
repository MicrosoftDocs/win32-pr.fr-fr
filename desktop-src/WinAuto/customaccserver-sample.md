---
title: Exemple CustomAccServer
description: Exemple CustomAccServer
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f8ee7d82361177af07aa7ad53a6137c39bc38
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088007"
---
# <a name="customaccserver-sample"></a>Exemple CustomAccServer

Cette rubrique contient les sections suivantes.

-   [Description](#description)
-   [Informations sur le téléchargement](#download-information)
-   [Configuration minimale requise](#minimum-requirements)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="description"></a>Description

Cet exemple montre comment implémenter un serveur Microsoft Active Accessibility pour un contrôle personnalisé simple. L’objet accessible pour le contrôle se compose de l’élément racine (une zone de liste) et de ses enfants (les éléments de liste).

## <a name="download-information"></a>Informations sur le téléchargement

L’exemple CustomAccServer est installé dans le cadre du [Kit de développement logiciel (SDK) Microsoft Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) et est disponible à l’emplacement suivant.



| Emplacement    | Chemin d’accès/URL                                                                           |
|-------------|------------------------------------------------------------------------------------|
| Kit de développement logiciel (SDK) Windows | % Program Files% \\ Microsoft SDK \\ \\ \[ numéro de version Windows exemples d' \] \\ exemples d' \\ WinUI \\ MSAA |



 

## <a name="minimum-requirements"></a>Configuration minimale requise



| Produit          | Version                         |
|------------------|---------------------------------|
| Système d’exploitation | Windows XP, Windows Server 2003 |
| Kit de développement logiciel (SDK) Windows      | 7.0                             |
| Visual Studio    | 2008                            |



 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à l’aide de Visual Studio 2008 :

1.  Exécutez l’outil de configuration du kit de développement logiciel (SDK) Microsoft Windows fourni avec le kit de développement logiciel (SDK) pour ajouter des répertoires Include SDK à Visual Studio.
2.  Ouvrez l’Explorateur Windows et accédez au répertoire du projet.
3.  Double-cliquez sur l’icône du fichier. sln (solution) pour ouvrir le projet dans Visual Studio.
4.  Dans le menu **générer** , sélectionnez **générer la solution** pour générer la solution. L’application sera générée dans le répertoire de \\ débogage ou de libération par défaut \\ .

Pour générer l’exemple à partir de la ligne de commande, consultez génération d’exemples dans les notes de publication de SDK Windows à l’emplacement suivant :% Program Files% \\ Microsoft SDK \\ Windows \\ v 7.0 \\ReleaseNotes.htm

## <a name="running-the-sample"></a>Exécution de l'exemple

Pour exécuter l’exemple :

1.  Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.
2.  Tapez AccServer.exe sur la ligne de commande ou double-cliquez sur l’icône de AccServer.exe pour le lancer à partir de l’Explorateur Windows.

Pour exécuter à partir de Visual Studio, appuyez sur F5 ou cliquez sur **Démarrer le débogage** dans le menu **Déboguer** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples](samples.md)
</dt> </dl>

 

 




