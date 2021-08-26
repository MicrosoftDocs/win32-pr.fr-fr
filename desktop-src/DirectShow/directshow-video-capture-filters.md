---
description: DirectShow Filtres de capture vidéo
ms.assetid: e4d1452d-ceac-4b5c-b9ba-ad4722ecff76
title: DirectShow Filtres de capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cafe2815376ddb2a099c309228ba1bf24ae9315f305edb7312b88dd1196f82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966329"
---
# <a name="directshow-video-capture-filters"></a>DirectShow Filtres de capture vidéo

les filtres de Capture dans DirectShow disposent de certaines fonctionnalités qui les distinguent des autres types de filtres. bien que le [générateur de Graph de Capture](capture-graph-builder.md) masque de nombreux détails, il est judicieux de lire cette section afin d’avoir une compréhension générale des DirectShow graphiques de Capture.

**Épingler les catégories**

Un filtre de capture possède souvent au moins deux broches de sortie qui fournissent le même type de données (par exemple, un code confidentiel d’aperçu et un code PIN de capture). Par conséquent, les types de média ne sont pas un bon moyen de distinguer les codes confidentiels. Au lieu de cela, les codes confidentiels se distinguent par leur fonctionnalité, qui est identifiée à l’aide d’un GUID, appelé *catégorie de code confidentiel*.

Pour plus d’informations sur la façon d’interroger des codes confidentiels pour leur catégorie, consultez [utilisation des catégories de code confidentiel](working-with-pin-categories.md). Toutefois, pour la plupart des applications, vous n’aurez pas à interroger directement les broches. Au lieu de cela, différentes méthodes [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) prennent des paramètres qui spécifient la catégorie de code confidentiel sur laquelle opérer. le générateur de Graph de Capture localise automatiquement le code confidentiel correct.

**Prévisualiser les broches et les broches de capture**

Certains périphériques de capture vidéo ont des broches de sortie distinctes pour l’aperçu et la capture. La broche d’aperçu est utilisée pour afficher la vidéo à l’écran, tandis que le code confidentiel de capture est utilisé pour écrire la vidéo dans un fichier.

Un pin de préversion et un code PIN de capture présentent les différences suivantes :

-   Un pin de préversion supprime les frames en fonction des besoins pour maintenir le débit sur le code confidentiel de capture.
-   Chaque frame d’un code PIN de capture est horodaté avec l’heure de la séquence de flux de la trame. Un pin d’aperçu n’horodatage pas les exemples qu’il livre.

La raison pour laquelle les images d’aperçu n’ont pas de datage est que le graphique de filtre introduit une faible latence dans le flux. Si l’heure de la capture est utilisée comme heure de présentation, le convertisseur vidéo traite chaque échantillon comme un peu plus tard. Cela peut amener le convertisseur vidéo à déposer des frames pendant qu’il essaie de rattraper son retard. La suppression des horodatages garantit que le convertisseur présente chaque échantillon lorsqu’il arrive, sans supprimer les frames.

La catégorie de code confidentiel pour les codes confidentiels de l’aperçu est l’aperçu de la catégorie d’ÉPINGLe \_ \_ La catégorie des broches de capture est la \_ capture de catégorie pin \_ .

**Broches de port vidéo**

Un port vidéo est une connexion matérielle entre un périphérique vidéo (par exemple, un tuner TV analogique) et la carte vidéo. Un port vidéo permet à l’appareil d’envoyer des données vidéo directement à la carte graphique. La vidéo est affichée à l’écran à l’aide d’une superposition matérielle. Un port vidéo peut être un câble réel qui connecte deux appareils sur des cartes distinctes. Il peut également s’agir d’une connexion câblée sur la même carte.

L’avantage d’un port vidéo est que la vidéo passe directement en mémoire vidéo, sans qu’il y ait de travail par le processeur. Toutefois, les ports vidéo présentent certains inconvénients :

-   Un port vidéo utilise toujours la surface de recouvrement pendant la capture, que vous souhaitiez ou non afficher un aperçu de la vidéo.
-   Le basculement entre les frames se produit automatiquement, ce qui complique la synchronisation du retournement avec d’autres opérations vidéo.

Si un périphérique de capture utilise un port vidéo, le filtre de capture a une broche de port vidéo au lieu d’un code confidentiel d’aperçu. La catégorie de code confidentiel pour les broches de port vidéo est broche \_ catégorie \_ VIDEOPORT.

Chaque filtre de capture a au moins un code PIN de capture. En outre, il peut avoir un code PIN de préversion ou un code PIN de port vidéo, mais jamais les deux à la fois. Les filtres peuvent avoir plusieurs broches de capture et des codes confidentiels, chacun disposant d’un type de support distinct. Par conséquent, un filtre unique peut avoir un code PIN de capture vidéo, un code confidentiel vidéo, un code confidentiel de capture audio et un code confidentiel audio preview. (Toutefois, il n’y a rien d’équivalent à un port vidéo pour l’audio.)

**Filtres WDM en amont**

Windows Les périphériques de modèle de pilote (WDM) peuvent nécessiter des filtres supplémentaires en amont du filtre de capture. Ces filtres sont les suivants :

-   [Filtre Tuner TV](tv-tuner-filter.md). Contrôle le paramétrage des tuners TV analogiques.
-   [Filtre audio TV](tv-audio-filter.md). Contrôle les paramètres audio pour les tuners TV analogiques.
-   [Filtre de distributeur vidéo analogique](analog-video-crossbar-filter.md). Achemine les signaux audio et vidéo via le périphérique matériel. Par exemple, un appareil peut avoir plusieurs entrées, telles que S-Video et vidéo composite. Le filtre de distributeur permet à l’application de sélectionner l’entrée.

bien qu’il s’agisse de filtres distincts dans DirectShow, ils représentent généralement le même périphérique matériel. Chaque filtre contrôle une fonction différente de l’appareil. Les filtres sont connectés par des broches, mais aucune donnée multimédia n’est déplacée sur les connexions de code confidentiel. Par conséquent, les codes confidentiels sur ces filtres ne se connectent pas en établissant un type de média. Au lieu de cela, ils utilisent des valeurs GUID appelées *moyennes*. Les GUID moyens sont définis de manière unique pour un minipilote de périphérique donné. Par exemple, le filtre Tuner TV et le filtre de capture vidéo pour la même carte TV prennent tous deux en charge le même support, ce qui permet à l’application de générer le graphique correctement.

Dans la pratique, à condition que vous utilisiez **ICaptureGraphBuilder2** pour créer vos graphiques de capture, ces filtres sont ajoutés automatiquement au graphique. Pour plus d’informations, consultez [filtres de pilote de classe WDM](wdm-class-driver-filters.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la capture vidéo dans DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



