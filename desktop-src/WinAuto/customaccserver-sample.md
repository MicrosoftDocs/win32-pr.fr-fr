---
title: Exemple CustomAccServer
description: Exemple CustomAccServer
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ebf1ecde2821208d788b20b5cb0fc1a00403c1607fb4604eb92845daf49d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325988"
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

l’exemple CustomAccServer est installé dans le cadre du [kit de développement logiciel (SDK) de Microsoft Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) et est disponible à l’emplacement suivant.



| Emplacement    | Chemin d’accès/URL                                                                           |
|-------------|------------------------------------------------------------------------------------|
| Kit de développement logiciel (SDK) Windows | % Program Files% \\ Microsoft sdk \\ Windows \\ \[ numéro de version \] \\ exemples \\ winui \\ msaa |



 

## <a name="minimum-requirements"></a>Configuration minimale requise



| Produit          | Version                         |
|------------------|---------------------------------|
| Système d’exploitation | Windows XP, Windows Server 2003 |
| Kit de développement logiciel (SDK) Windows      | 7.0                             |
| Visual Studio    | 2008                            |



 

## <a name="building-the-sample"></a>Génération de l'exemple

pour générer l’exemple à l’aide de Visual Studio 2008 :

1.  exécutez l’outil de Configuration du kit de développement logiciel (sdk) de Microsoft Windows fourni avec le kit de développement logiciel (sdk) pour ajouter des répertoires include sdk à Visual Studio.
2.  ouvrez Windows Explorer et accédez au répertoire du projet.
3.  Double-cliquez sur l’icône du fichier. sln (solution) pour ouvrir le projet dans Visual Studio.
4.  Dans le menu **générer** , sélectionnez **générer la solution** pour générer la solution. L’application sera générée dans le répertoire de \\ débogage ou de libération par défaut \\ .

pour générer l’exemple à partir de la ligne de commande, consultez génération d’exemples dans les notes de publication de SDK Windows à l’emplacement suivant :% Program Files% \\ Microsoft sdk \\ Windows \\ v 7.0 \\ReleaseNotes.htm

## <a name="running-the-sample"></a>Exécution de l'exemple

Pour exécuter l’exemple :

1.  accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’explorateur de Windows.
2.  tapez AccServer.exe sur la ligne de commande ou double-cliquez sur l’icône de AccServer.exe pour le lancer à partir de Windows Explorer.

pour exécuter à partir de Visual Studio, appuyez sur F5 ou cliquez sur **démarrer le débogage** dans le menu **déboguer** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples](samples.md)
</dt> </dl>

 

 




