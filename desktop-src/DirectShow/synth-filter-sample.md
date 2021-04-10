---
description: Exemple de filtre Synth
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: Exemple de filtre Synth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd569091df92eca3fbff4d8cb200150d6e6bfdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868518"
---
# <a name="synth-filter-sample"></a>Exemple de filtre Synth

## <a name="description"></a>Description

Le filtre Synth est un filtre source qui génère des formes d’ondes audio.

Ce filtre illustre la génération de graphiques dynamiques. Il peut basculer entre le format audio PCM non compressé et le \_ format MS ADPCM compressé (Microsoft adaptative Delta Pulse Code Modulation).

Ce filtre apparaît dans GraphEdit comme « filtre de synthétiseur audio ».

Pour plus d’informations sur la génération de graphiques dynamiques, consultez [génération de graphiques dynamiques](dynamic-graph-building.md).

## <a name="usage"></a>Utilisation

Le filtre Synth permet à l’utilisateur de définir la forme d’onde, la fréquence, le nombre de canaux et d’autres propriétés via la page de propriétés. Pour définir le point de terminaison supérieur ou inférieur de la plage de fréquences balayées, maintenez la touche Maj enfoncée tout en réglant le curseur fréquence. Le filtre prend également en charge une interface personnalisée, ISynth2, pour la définition de ces propriétés.

Pour illustrer la fonctionnalité de création de graphique dynamique, procédez comme suit :

1.  Générez le filtre et inscrivez-le avec l’utilitaire regsvr32.
2.  Lancez GraphEdit.
3.  Insérez le filtre de synthétiseur audio. Il apparaît dans la catégorie filtres DirectShow.
4.  Affichez la broche de sortie du filtre.
5.  Cliquez sur le bouton **lecture** .
6.  Ouvrez la page de propriétés du filtre.
7.  Dans la zone format de sortie, sélectionnez PCM ou Microsoft ADPCM.

## <a name="programming-notes"></a>Notes de programmation

Cet exemple contient les fichiers suivants :

-   Dynsrc. h, dynsrc. cpp : contient deux classes de base pour les filtres sources qui prennent en charge la génération de graphiques dynamiques, CDynamicSource et CDynamicSourceStream.
-   ISynth. h : déclare l’interface ISynth2 personnalisée pour définir des propriétés sur le filtre.
-   Resource. h : contient des constantes de ressource.
-   Synth. def : exporte les fonctions DLL requises par la bibliothèque COM.
-   Synth. h, synth. cpp : contient la classe CAudioSynth, qui génère les données audio et la classe CSynthFilter, qui implémente le filtre.
-   Synth. RC : contient les ressources utilisées par le filtre.
-   Synthprp. h, Synthprp. cpp : implémente la page de propriétés du filtre.

La classe CDynamicSource est adaptée à partir de la classe de base [**CSource**](csource.md) . Elle utilise une ou plusieurs broches de sortie dérivées de la classe CDynamicSourceStream. La classe CDynamicSourceStream est adaptée à partir de la classe [**CSourceStream**](csourcestream.md) , mais dérive de la classe [**CDynamicOutputPin**](cdynamicoutputpin.md) plutôt que de la classe [**CBaseOutputPin**](cbaseoutputpin.md) .

Les méthodes suivantes de la classe CDynamicSource sont introuvables dans [**CSource**](csource.md):

-   Stop : signale l’événement Stop ([**CDynamicOutputPin :: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)) et arrête le thread de travail pour tous les codes confidentiels non connectés. Sur un code confidentiel connecté, la méthode inactive du pin arrête le thread de travail.
-   Pause : réinitialise l’événement d’arrêt.
-   JoinFilterGraph : appelle la méthode [**CDynamicOutputPin :: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) sur chaque pin.

Les méthodes suivantes de la classe CDynamicSourceStream sont introuvables dans [**CSourceStream**](csourcestream.md):

-   DestroySourceThread : arrête le thread de travail.
-   FatalError : signale une erreur au gestionnaire de graphique de filtre.
-   OutputPinNeedsToBeReconnected : signale que la broche de sortie doit être reconnectée. Lorsque cette méthode est appelée, le thread de travail appelle la méthode [**CDynamicOutputPin ::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) pour reconnecter le code confidentiel.

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] du kit de développement logiciel (SDK)* \\ \\ fichiers multimédias de \\ \\ filtres DirectShow \\ .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples DirectShow](directshow-samples.md)
</dt> </dl>

 

 



