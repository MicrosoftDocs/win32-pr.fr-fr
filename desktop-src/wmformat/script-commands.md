---
title: Commandes de script
description: Commandes de script
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- Windows Media Format SDK, commandes de script
- ASF (Advanced Systems Format), commandes de script
- ASF (format des systèmes avancés), commandes de script
- Windows Media Format SDK, flux de scripts
- ASF (Advanced Systems Format), flux de scripts
- ASF (format de systèmes avancés), flux de script
- Windows Media Format SDK, flux
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- scripts, commandes
- scripts, flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57ab446a216624dc8f844f54298aeeaee358ac3
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104032062"
---
# <a name="script-commands"></a>Commandes de script

Les commandes de script prises en charge par le kit de développement logiciel (SDK) Windows Media format sont des paires de chaînes nom et valeur simples. Par exemple, une commande de script courante est « URL », qui est utilisée par le lecteur Windows Media et d’autres applications en cours d’exécution pour ouvrir des pages Web. L’autre moitié de la paire de scripts pour la commande « URL » contient une URL (Uniform Resource Locator) valide, telle que `https://www.adatum.com` . Aucune prise en charge n’est fournie par les objets de ce kit de développement logiciel (SDK) pour des commandes spécifiques. votre application doit inclure une logique pour gérer les commandes que vous utilisez. Vous pouvez utiliser les commandes prises en charge par le lecteur Windows Media pour assurer la compatibilité avec la plupart des joueurs.

Les commandes de script peuvent être remises de deux manières : dans un flux de script ou dans l’en-tête de fichier.

## <a name="script-streams"></a>Flux de script

Vous pouvez fournir des commandes de script dans leur propre flux dans un fichier ASF. Chaque échantillon dans un flux de script contient les deux chaînes de la paire nom/valeur. L’avantage de l’utilisation d’un flux de script est que les commandes sont remises à l’heure de présentation correcte.

## <a name="script-commands-in-the-file-header"></a>Commandes de script dans l’en-tête de fichier

Les commandes de script peuvent être incluses dans l’en-tête de fichier pour être récupérées au moment de la lecture. L’application en cours d’exécution est chargée d’exécuter les commandes de script au moment opportun. L’avantage de l’utilisation de commandes de script dans l’en-tête de fichier est que toutes les commandes de script sont disponibles avant de commencer à recevoir des exemples.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités des fichiers ASF**](asf-file-features.md)
</dt> <dt>

[**Utilisation des commandes de script**](using-script-commands.md)
</dt> </dl>

 

 




