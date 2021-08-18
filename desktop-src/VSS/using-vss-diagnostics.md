---
description: Vsdiagview et Vssagent sont des outils que vous pouvez utiliser pour dépanner des applications VSS. notez que ces outils sont inclus dans le kit de développement logiciel (SDK) de Microsoft Windows pour Windows Vista et versions ultérieures.
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: Utilisation des diagnostics VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7742bf706da0bb8fdd377960a597a61b6592b772df98982cec500434f66c7579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590802"
---
# <a name="using-vss-diagnostics"></a>Utilisation des diagnostics VSS

Vsdiagview et Vssagent sont des outils que vous pouvez utiliser pour dépanner des applications VSS.

> [!Note]  
> ces outils sont inclus dans le kit de développement logiciel (SDK) de Microsoft Windows pour Windows Vista et versions ultérieures. vous pouvez télécharger le SDK Windows à partir de [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

dans l’installation SDK Windows, ces outils se trouvent dans `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (pour 64 bits Windows) et `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (pour le Windows 32 bits).

## <a name="gathering-data"></a>Collecte de données

Vous pouvez collecter des données à l’aide de la commande Vssagent.

**Pour collecter des données à l’aide de Vssagent**

1.  Pour collecter des données à partir de la ligne de commande, utilisez la commande Vssagent comme suit :

    **vssagent-Gather** *xmlFileName * * * .xml**

2.  Pour afficher le fichier de sortie, consultez la section Affichage des données suivante.

## <a name="viewing-data"></a>Affichage des données

L’application Vsdiagview peut être utilisée pour afficher les données qui ont été collectées à l’aide de la commande Vssagent. Vsdiagview affiche les informations suivantes sur l’ordinateur :

-   Informations sur l’ordinateur, telles que la version du système d’exploitation, la mémoire totale disponible et la vitesse du processeur
-   Noms et numéros de version des fichiers binaires VSS
-   Les noms et les propriétés des périphériques de disque et de volume
-   Noms et propriétés de toutes les applications COM+
-   Noms des journaux des événements qui peuvent être utilisés pour diagnostiquer les problèmes VSS
-   Les noms de tous les enregistreurs VSS et les événements qu’ils gèrent
-   Informations sur les autres fichiers de système d’exploitation

**Pour afficher les données à l’aide de Vsdiagview**

1.  Dans le menu fichier, choisissez **ouvrir** pour rechercher un fichier. (L’emplacement par défaut est C : \\ vssdiag.)
2.  Cliquez sur **ouvrir** pour afficher les données.

 

 



