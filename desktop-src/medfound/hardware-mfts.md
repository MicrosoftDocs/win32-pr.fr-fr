---
description: Cette rubrique explique comment écrire une Media Foundation transformation (MFT) qui agit en tant que proxy à un encodeur, à un décodeur ou à un processeur de signal numérique (DSP) matériel.
ms.assetid: 9922d403-5d0d-433f-ad9f-c86142ac0f46
title: Matériel MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5ce05b4fdad6040b51f66f543c1737fc3918d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201804"
---
# <a name="hardware-mfts"></a>Matériel MFTs

> [!Note]  
> Cette rubrique s’applique à Windows 7 ou version ultérieure.

 

Cette rubrique explique comment écrire une Media Foundation transformation (MFT) qui agit en tant que proxy à un encodeur, à un décodeur ou à un processeur de signal numérique (DSP) matériel.

> [!IMPORTANT]
> Si un codec matériel utilise le pilote de classe multimédia AVStream, il ne nécessite pas de MFT personnalisé. Media Foundation fournit un proxy AVStream à cet effet. Les informations contenues dans cette rubrique s’appliquent uniquement dans le cas particulier où le codec matériel n’utilise pas AVStream. Pour plus d’informations, consultez [prise en charge du codec matériel dans AVStream](https://msdn.microsoft.com/library/dd568169.aspx).

 

Cette rubrique contient les sections suivantes :

-   [Introduction](#introduction)
-   [Attributs MFT du matériel](#hardware-mft-attributes)
-   [Séquence de négociation matérielle](#hardware-handshake-sequence)
-   [Traitement des données](#data-processing)
-   [Décodeur/encodeur couplé](#paired-decoderencoder)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Tout codec matériel qui n’est pas basé sur AVStream doit fournir sa propre table MFT pour agir en tant que proxy du pilote. Un codec matériel peut incorporer plusieurs blocs fonctionnels distincts :

-   Encodeur
-   Décodeur
-   Mise à l’échelle des frames/conversion de format

Chacune de ces fonctions doit être gérée par une table MFT distincte. Une table MFT matérielle ne doit jamais jouer le rôle d’un « transcodeur polyvalent ». Au lieu de cela, placez les fonctions d’encodage dans un encodeur MFT et décodez les fonctions dans une table MFT de décodage. Si le matériel offre des conversions de format et de mise à l’échelle des frames, placez ces fonctions dans un processeur vidéo distinct, inscrit dans la catégorie de **\_ \_ \_ processeur vidéo de catégorie MFT** . Si le matériel ne prend pas en charge la mise à l’échelle des cadres ou la conversion de format, Media Foundation fournit un processeur vidéo logiciel.

Les MFTs matériels présentent les conditions générales suivantes :

-   Le matériel MFTs doit utiliser le nouveau modèle de traitement asynchrone, comme décrit dans [MFTS asynchrone](asynchronous-mfts.md).
-   Le matériel MFTs doit prendre en charge les modifications de format dynamique, comme décrit dans [modifications de format dynamique](basic-mft-processing-model.md).

## <a name="hardware-mft-attributes"></a>Attributs MFT du matériel

Une table MFT matérielle doit implémenter les méthodes suivantes liées aux attributs :

-   [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes): retourne un magasin d’attributs pour les attributs MFT globaux.
-   [**IMFTransform :: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes): retourne un magasin d’attributs pour un flux d’entrée.
-   [**IMFTransform :: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes): retourne un magasin d’attributs pour un flux de sortie.

Lorsque la table MFT est créée pour la première fois, elle doit définir les attributs suivants sur son propre magasin d’attributs global (autrement dit, le magasin d’attributs retourné par [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)) :



| Attribut                                                                                    | Description                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_transformation MF \_ asynchrone](mf-transform-async.md)                                               | Doit avoir la valeur **true**. Indique que la table MFT effectue un traitement asynchrone.                                                                                                      |
| [Attribut de l' \_ \_ URL matérielle de l’ÉNUMÉRation MFT \_ \_](mft-enum-hardware-url-attribute.md)                   | Contient le lien symbolique pour le périphérique matériel.<br/> Le chargeur de topologie utilise la présence de cet attribut pour déterminer si un MFT représente un périphérique matériel.<br/> |
| [**\_modification du \_ format dynamique de la prise en charge de \_ MFT \_**](mft-support-dynamic-format-change-attribute.md) | Doit avoir la valeur **true**. Indique que la table MFT prend en charge les modifications de format dynamiques.                                                                                                       |



 

## <a name="hardware-handshake-sequence"></a>Séquence de négociation matérielle

Si deux MFTs représentent le même appareil physique, ils peuvent échanger des données au sein du matériel, par exemple sur un bus matériel. Il n’est pas nécessaire de copier les données dans la mémoire système, puis de les replacer sur l’appareil.

Dans le diagramme suivant, le MFTs intitulé « A » et « B » représentent des blocs fonctionnels au sein du même matériel. Par exemple, dans un scénario de transcodage, « A » peut représenter un décodeur matériel et « B » peut représenter un encodeur matériel. Le passage de données entre « A » et « B » se produit au sein du matériel. La table MFT intitulée « C » est une table MFT de logiciel. Le passage de données de « B » à « C » utilise la mémoire système.

![Diagramme montrant des zones étiquetées a à c et un codec matériel : un point vers b et le codec, le codec pointe vers b et b pointe vers c](images/proxy-mft.png)

Pour établir une connexion matérielle, les deux MFTs matériels doivent utiliser un canal de communication privé. Cette connexion est établie lors de la négociation de format, avant que les types de média ne soient définis et avant le premier appel à [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). Le processus de connexion fonctionne comme suit :

1.  Le chargeur de topologie vérifie à la fois MFTs la présence de l’attribut d' [ \_ \_ \_ \_ attribut d’URL matériel de l’énumération MFT](mft-enum-hardware-url-attribute.md) . Notez qu’elle n’examine pas la valeur de cet attribut.
2.  Si l’attribut de l' [ \_ \_ \_ \_ URL matérielle de l’énumération MFT](mft-enum-hardware-url-attribute.md) est présent sur les deux MFTS, le chargeur de topologie effectue les opérations suivantes :
    1.  Le chargeur de topologie appelle [**IMFTransform :: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) sur la table MFT en amont (A). Cette méthode retourne un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Laissez ce pointeur dénoté *pUpstream*.
    2.  Le chargeur de topologie appelle [**IMFTransform :: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) sur la MFT en aval (B). Cet appel retourne également un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Laissez ce pointeur dénoté *pDownstream*.
    3.  Le chargeur de topologie définit l’attribut [d' \_ \_ \_ attribut de flux connecté MFT](mft-connected-stream-attribute.md) sur *PDownstream* en appelant [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown). La valeur de l’attribut est le pointeur *pUpstream* .
    4.  Le chargeur de topologie affecte la **valeur true** à l’attribut [MFT \_ Connected \_ to \_ HW \_ Stream](mft-connected-to-hw-stream.md) sur *pDownstream* et *pUpstream*.
3.  À ce stade, la table MFT en aval a un pointeur vers le magasin d’attributs de la MFT en amont, comme indiqué dans le diagramme suivant.

    ![diagramme avec chaque MFTS pointant vers son flux, chaque flux pointant vers son magasin et le magasin d’entrée avec une ligne en pointillés dans le magasin de sortie](images/proxy-mft2.png)

    > [!Note]  
    > Par souci de clarté, ce diagramme montre les flux et les magasins d’attributs en tant qu’objets distincts, mais cela n’est pas nécessaire pour l’implémentation.

     

4.  La table MFT en aval utilise le pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pour établir un canal de communication privé avec la table MFT en amont. Étant donné que le canal est privé, le mécanisme exact est défini par l’implémentation. Par exemple, la table MFT peut demander une interface COM privée.

À l’étape 4, la MFT en aval doit vérifier si les deux MFTs partagent le même appareil physique. Si ce n’est pas le cas, ils doivent revenir à l’utilisation de la mémoire système pour le transport des données. Cela permet à la MFT de fonctionner correctement avec les MFTs logicielles et d’autres périphériques matériels.

Si le protocole de transfert s’effectue correctement et que les deux MFTs partagent un canal de données privé, ils n’utilisent pas le modèle de traitement de données standard (décrit dans la section suivante) au niveau du point de connexion. Plus précisément, la MFT en aval n’envoie pas d’événements [METransformNeedInput](metransformneedinput.md) ; Pour plus d’informations, reportez-vous à la section suivante de cette rubrique.

## <a name="data-processing"></a>Traitement des données

Lorsqu’une table MFT matérielle utilise la mémoire système pour le transport de données, le processus fonctionne comme suit :

1.  Pour demander plus d’entrées, la table MFT envoie un événement [METransformNeedInput](metransformneedinput.md) .
2.  L’événement [METransformNeedInput](metransformneedinput.md) fait en sorte que le pipeline appelle [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).
3.  Lorsque la table MFT contient des données de sortie, la table MFT envoie un événement [METransformHaveOutput](metransformhaveoutput.md) .
4.  L’événement [METransformHaveOutput](metransformhaveoutput.md) fait en sorte que le pipeline appelle [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Pour plus d’informations, consultez [MFTS asynchrone](asynchronous-mfts.md).

Toutefois, si la table MFT utilise un canal matériel, elle n’envoie pas ces événements au point de connexion matériel, car tous les transferts de données s’effectuent en interne au sein du matériel. Par conséquent, le pipeline n’appelle pas [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) ou [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sur le point de connexion.

Par exemple, considérons le premier diagramme de cette rubrique. Compte tenu de cette configuration, le traitement des données se produit comme suit :

1.  « A » envoie [METransformNeedInput](metransformneedinput.md) pour demander des données.
2.  Le pipeline appelle [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) sur « A ».
3.  « A » et « B » traitent les données dans le matériel.
4.  Une fois le traitement terminé, « B » envoie un événement [METransformHaveOutput](metransformhaveoutput.md) .
5.  Le pipeline appelle [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sur « B ».

## <a name="paired-decoderencoder"></a>Décodeur/encodeur couplé

Si un décodeur et un encodeur se trouvent sur la même puce matérielle, il peut être préférable de les utiliser ensemble lors du transcodage. Autrement dit, la sélection de l’une d’entre elles doit entraîner la sélection de l’autre dans le pipeline de transcodage. Pour vous assurer que les codecs matériels correspondants sont choisis, les MFTs de codec doivent offrir un type de média personnalisé. Pour créer un type de média personnalisé :

-   Définissez l’attribut de [**\_ type de \_ majeure \_ série MF MT**](mf-mt-major-type-attribute.md) sur **MFMediaType \_ audio** ou **MFMediaType \_ Video**, selon le cas.
-   Définissez l’attribut de [**\_ sous- \_ type MF MT**](mf-mt-subtype-attribute.md) sur une valeur Guid personnalisée.

Les autres attributs de type sont facultatifs. Le décodeur retourne le type personnalisé à partir de son [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), et l’encodeur retourne le type personnalisé à partir de sa méthode [**IMFTransform :: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) . Dans les deux cas, le type personnalisé doit être la première entrée de la liste (*dwTypeIndex* = 0).

Pour fonctionner avec les codecs logiciels, le codec doit également retourner au moins un format standard, tel que NV12 pour la vidéo. Les formats standard doivent apparaître après le type personnalisé (*dwTypeIndex* > 0). Si les deux codecs doivent toujours être couplés et ne peuvent pas interagir avec les codecs logiciels, MFTs doit retourner uniquement le format personnalisé et ne retourne pas de formats standard.

> [!Note]  
> Si un décodeur ne retourne pas de formats standard, il ne peut pas être utilisé pour la lecture avec le [convertisseur vidéo amélioré](enhanced-video-renderer.md). Dans ce cas, elle doit être inscrite en tant que décodeur de transcodage uniquement. Consultez [décodeurs de transcodage uniquement](implementing-a-codec-mft.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture d’une table MFT personnalisée](writing-a-custom-mft.md)
</dt> <dt>

[Implémentation d’une table MFT de codec](implementing-a-codec-mft.md)
</dt> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 




