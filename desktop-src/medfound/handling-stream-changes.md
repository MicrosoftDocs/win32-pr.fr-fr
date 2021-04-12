---
description: Cette rubrique décrit comment une transformation de Media Foundation (MFT) doit gérer les modifications de format pendant la diffusion en continu.
ms.assetid: b0a94760-b4dd-4e50-a5ce-a1f674dde156
title: Gestion des modifications de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2adf3cbc0504a37fe611b77047c73f85b9d1e742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201805"
---
# <a name="handling-stream-changes"></a>Gestion des modifications de flux

Cette rubrique décrit comment une transformation de Media Foundation (MFT) doit gérer les modifications de format pendant la diffusion en continu.

> [!IMPORTANT]
>
> Cette rubrique ne s’applique pas aux encodeurs. Les encodeurs ne doivent pas propager les modifications de format comme décrit dans cette rubrique. Les encodeurs doivent uniquement accepter un type d’entrée qui correspond au type de sortie actuellement configuré.

 

## <a name="overview-of-format-changes"></a>Vue d’ensemble des modifications de format

En règle générale, il existe deux raisons pour lesquelles un format peut changer pendant la diffusion en continu.

-   Le client peut basculer vers un flux avec un nouveau format. Par exemple, dans la télévision numérique, cela peut se produire en raison d’un changement de canal.
-   Dans certains formats vidéo, comme H. 264, le flux binaire peut signaler une modification de format. Ces modifications peuvent inclure des modifications apportées à la dominance des champs, à la résolution vidéo ou au proportions en pixels.

Si le type d’encodage change, le client peut avoir besoin de supprimer la MFT du pipeline et de la remplacer par une autre MFT. (Par exemple, le client devra peut-être effectuer une permutation dans un nouveau décodeur.) Cette rubrique ne couvre pas cette situation. Cette rubrique couvre uniquement le cas où la MFT actuelle peut gérer le nouveau format.

Si le format change, la table MFT peut nécessiter un nouveau type d’entrée, un nouveau type de sortie, ou les deux.

-   Les modifications apportées au type d’entrée sont initiées par le client. Une table MFT ne change jamais son propre type d’entrée.
-   Les modifications apportées au type de sortie sont initiées par la table MFT. La table MFT signale qu’elle requiert un nouveau type de sortie et que le client négocie le nouveau type de sortie avec la table MFT.

Trois cas distincts sont donc possibles :

-   Le client définit un nouveau type d’entrée. La table MFT utilise le nouveau format, sans aucune modification de son type de sortie.
-   Le client définit un nouveau type d’entrée, ce qui déclenche une modification du type de sortie.
-   Le type d’entrée ne change pas, mais la table MFT détecte une modification de format dans le flux de données binaire, ce qui nécessite un nouveau type de sortie.

## <a name="implementing-format-changes"></a>Implémentation des modifications de format

Le reste de cette rubrique décrit comment le client doit traiter une modification de format et comment implémenter les modifications de format dans une table MFT.

### <a name="output-type"></a>Type de sortie

Tout MFT peut lancer une modification de son type de sortie, comme suit :

1.  Le client appelle [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). La table MFT répond comme suit :
    1.  La table MFT ne produit pas d’exemple de sortie dans [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).
    2.  La table MFT définit l’indicateur de **modification de \_ \_ \_ \_ format \_ de mémoire tampon de données de sortie MFT** dans le membre **dwStatus** de la structure de [**\_ \_ \_ mémoire tampon de données de sortie MFT**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) .
    3.  La méthode [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) retourne le code d’erreur de la modification du **flux de \_ \_ transformation \_ \_ MF E**.
2.  Le client appelle [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Cette méthode retourne un jeu de types de sortie mis à jour.
3.  Le client appelle [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) pour définir un nouveau type de sortie.
4.  Le client reprend l’appel de [**ProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) / [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

### <a name="input-type"></a>Type d’entrée

Les modifications apportées au type d’entrée sont lancées par le client, jamais par la MFT. Si le type d’entrée change, il peut déclencher une modification du type de sortie.

La séquence exacte d’événements dépend de la valeur de l’attribut de modification de la [**\_ prise en charge du \_ \_ format \_ dynamique de la table MFT**](mft-support-dynamic-format-change-attribute.md) .



| Valeur     | Description                                                     |
|-----------|-----------------------------------------------------------------|
| **FALSE** | Avant de définir un nouveau type d’entrée, le client doit vider la table MFT. |
| **TRUE**  | Le client peut définir un nouveau type d’entrée sans vider la MFT.   |



 

Une table MFT expose cet attribut par le biais de sa méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . La valeur par défaut de cet attribut est **false**. Si la MFT ne définit pas l’attribut, traitez la valeur comme **false**.

**La \_ modification du format dynamique de la prise en charge MFT \_ \_ \_ est false**

1.  Le client envoie le message de [**\_ drainage de \_ commande \_ de message MFT**](mft-message-command-drain.md) .
2.  Le client draine la MFT en appelant [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) jusqu’à ce que **ProcessOutput** retourne la **\_ transformation MF E \_ \_ nécessite \_ plus \_ d’entrée**.
3.  Le client appelle [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) pour définir le nouveau type d’entrée.
4.  La table MFT valide le type d’entrée. Si le type n’est pas valide, [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) retourne **MF \_ E \_ INVALIDMEDIATYPE** ou un autre code d’erreur. Sinon, **SetInputType** retourne S \_ OK.
5.  En supposant que le type d’entrée est valide, la table MFT évalue si le type de sortie change également. Si ce n’est pas le cas, la diffusion continue et aucune autre action n’est requise.
6.  Si le type de sortie change :
    1.  La table MFT invalide son type de média de sortie actuel et met à jour la liste des types de médias de sortie disponibles.
    2.  L’appel suivant à [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) retourne **la \_ \_ modification du \_ flux \_ de transformation MF E**, comme décrit dans la section précédente.
    3.  Le client appelle [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) pour accéder à la liste mise à jour des types de sortie.
    4.  Le client appelle [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

**La \_ modification du format dynamique de la prise en charge MFT \_ \_ \_ est vraie**

1.  Le client appelle [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) pour définir le nouveau type d’entrée.
2.  La table MFT valide le type d’entrée. Si le type n’est pas valide, [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) retourne **MF \_ E \_ INVALIDMEDIATYPE** ou un autre code d’erreur. Sinon, **SetInputType** retourne S \_ OK.
3.  En supposant que le type d’entrée est valide, la table MFT évalue si le type de sortie change également. Si ce n’est pas le cas, la diffusion continue et aucune autre action n’est requise.
4.  Avant que le type de sortie ne change, la table MFT doit traiter tous les exemples d’entrée mis en cache, comme suit :
    1.  La table MFT n’invalide pas son type de sortie actuel.
    2.  La table MFT produit autant de sortie que possible des exemples d’entrée mis en cache.
    3.  Il est facultatif que la table MFT accepte de nouveaux exemples d’entrée lors du traitement des exemples mis en cache. Si c’est le cas, les nouveaux exemples d’entrée utilisent le nouveau format d’entrée, de sorte que la MFT doit assurer le suivi du point lorsque le format a changé.
5.  Une fois que la MFT a traité tous les exemples qu’il a reçus avant la modification du type d’entrée, [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) retourne la **\_ modification du flux de \_ transformation \_ \_ MF E**.
6.  La table MFT invalide son type de sortie actuel et met à jour la liste des types de médias de sortie disponibles.
7.  Le client négocie le nouveau type de sortie, comme décrit précédemment.

Un [MFTS asynchrone](asynchronous-mfts.md) doit retourner la valeur **true** pour l’attribut de [**\_ \_ \_ \_ modification de format dynamique de la prise en charge de MFT**](mft-support-dynamic-format-change-attribute.md) . Lors de l’utilisation d’une table MFT asynchrone, le client peut supposer que l’attribut de **\_ \_ \_ \_ modification de format dynamique de la table MFT prend** la valeur **true**.

Lorsque [**la \_ prise en charge de la \_ \_ mise en forme dynamique \_**](mft-support-dynamic-format-change-attribute.md) par la MFT prend la **valeur true**, la principale différence réside dans le fait que le client n’est pas obligé de vider la MFT avant de définir un nouveau type d’entrée. Par conséquent, le type d’entrée peut changer pendant que la table MFT contient des exemples d’entrée. Il est important que la MFT ne supprime pas simplement ces exemples. En outre, le type de sortie ne peut pas changer tant que la table MFT n’a pas traité toutes ses données mises en cache.

Le paragraphe précédent s’applique particulièrement aux décodeurs vidéo, qui peuvent recevoir des frames inter-codés hors de l’ordre temporel et doivent donc les mettre en cache. Si une table MFT ne met pas en cache les exemples d’entrée, le drainage est essentiellement une absence d’opération. Dans ce cas, la table MFT peut définir la [**\_ \_ \_ \_ modification du format dynamique de la table MFT**](mft-support-dynamic-format-change-attribute.md) sur **false** (ou laissez l’attribut désactivé).

Notez également que chaque MFT est censé gérer les modifications de format correctement après avoir été vidé. L’attribut de [**\_ \_ \_ \_ modification de format dynamique de la table MFT**](mft-support-dynamic-format-change-attribute.md) indique si la table MFT prend en charge les changements de format sans purge.

## <a name="change-in-interlace-mode"></a>Changer en mode entrelacé

Les modifications apportées au mode d’entrelacement de vidéos sont un cas particulier, car ils n’invalident pas le type de média actuel. Au lieu de cela, le mode entrelacé est spécifié pour chaque image vidéo en définissant des attributs sur l’exemple de support. Une table MFT vidéo doit vérifier chaque échantillon d’entrée pour la présence de ces indicateurs.

Le mode entrelacé peut changer lorsque la trame de champ supérieure passe du champ supérieur au champ inférieur, ou lorsque la vidéo bascule entre des images progressives et entrelacées.

Pour plus d’informations, consultez [entrelacer les indicateurs sur les exemples](video-interlacing.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture d’une table MFT personnalisée](writing-a-custom-mft.md)
</dt> </dl>

 

 



