---
description: Media Foundation fournit la source de média ASF qu’une application peut utiliser pour représenter un fichier ASF dans la couche de pipeline de l’architecture.
ms.assetid: a2d2b382-d666-4a37-a6a9-0b839fbfbec3
title: Source de média ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75dc682d48339ce4ff707e7859a6962b9f5cfd92
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106539392"
---
# <a name="asf-media-source"></a>Source de média ASF

Media Foundation fournit la source de média ASF qu’une application peut utiliser pour représenter un fichier ASF dans la couche de pipeline de l’architecture.

Pour pouvoir lire un fichier ASF, une application peut utiliser la source de média ASF pour alimenter les données dans un pipeline de lecture. Dans un scénario d’encodage, l’application peut utiliser la source de média ASF comme source pour convertir dans un autre format ou pour convertir un fichier de taux binaire plus élevé en un fichier à vitesse de transmission plus faible sans modifier les formats. La source de média ASF doit être utilisée dans la couche de pipeline, autrement dit, une application doit utiliser la session de média pour contrôler l’opération. Ce niveau d’accès permet aux applications d’accéder aux événements pendant que la session multimédia est en cours. Pour bénéficier d’un accès de niveau inférieur au contenu ASF, une application doit utiliser les composants ASF de la couche WMContainer.

La source de média ASF implémente l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) , qui est l’interface générique pour les sources de média dans Media Foundation. Comme n’importe quelle autre source multimédia, la source de média ASF fournit un descripteur de présentation qui décrit principalement l’objet d’en-tête ASF. En outre, la source de média ASF fournit des descripteurs de flux qui représentent chaque flux dans le contenu multimédia. Pour plus d’informations, consultez [structure des fichiers ASF](asf-file-structure.md).

-   [Création de la source de média ASF](#creating-the-asf-media-source)
-   [Paramètres de configuration pour la source de média ASF](#configuration-settings-for-the-asf-media-source)
-   [Modèle objet de source de média ASF](#asf-media-source-object-model)
-   [Services source de média ASF](#asf-media-source-services)
    -   [Traduction du code temporel](#timecode-translation)
-   [Rubriques connexes](#related-topics)

## <a name="creating-the-asf-media-source"></a>Création de la source de média ASF

Pour créer la source de média ASF, l’application doit utiliser le programme de [résolution de source](source-resolver.md). Pour créer la source de média ASF, l’application doit fournir la source pour laquelle le programme de résolution source crée la source du média ASF. Les informations sur la source doivent être fournies en spécifiant l’URL du fichier source ou le flux d’octets qui contient le média. Si l’application choisit de créer la source du média ASF en spécifiant l’URL, elle doit appeler [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) pour une opération synchrone ou **IMFSourceResolver :: Begin... EndCreateObjectFromURL** pour l’opération asynchrone. Le processus de création de la source du média à partir d’un flux d’octets est similaire. L’application doit appeler [**IMFSourceResolver :: CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) pour une opération synchrone ou **IMFSourceResolver :: Begin... EndCreateObjectFromBytestream** pour l’opération asynchrone. Ces appels doivent spécifier le \_ \_ MEDIASOURCE de résolution MF dans le paramètre *dwFlags* . Pour plus d’informations sur l’utilisation de cet indicateur, consultez Utilisation du programme de résolution source.

Si l’application spécifie une URL, pour un fichier local, la chaîne d’URL peut contenir le chemin d’accès du fichier multimédia ou peut avoir pour préfixe le schéma « fichier : ». L’extension de nom de fichier doit être « . ASF », « . WM », L « . WMA » ou « . wmv ». Pour un fichier ASF sur le réseau, le programme de résolution source crée la [source réseau](network-source-features.md), qui utilise la source de média ASF.

Pendant le processus de création d’objet, le programme de résolution source recherche la liste des gestionnaires de schémas et les gestionnaires de flux d’octets dans le registre système et charge le gestionnaire correspondant le plus proche qui peut analyser le contenu multimédia et également créer l’objet source du média en dessous. Quelle que soit la méthode utilisée pour créer la source du média (URL et flux d’octets), le programme de résolution source crée un flux d’octets et lit le contenu du média source dans le flux d’octets. Pour plus d’informations, consultez [gestionnaires de modèles et gestionnaires de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md).

Pour obtenir un exemple de code sur la création d’une source multimédia, consultez [utilisation du programme de résolution source](using-the-source-resolver.md).

## <a name="configuration-settings-for-the-asf-media-source"></a>Paramètres de configuration pour la source de média ASF

Le programme de résolution source interroge les fonctionnalités du flux d’octets sous-jacent et détermine que les opérations sont autorisées sur la source du média nouvellement créée. Une de ces fonctionnalités est enquête de recherche. Si une opération de recherche est autorisée, l’application peut spécifier le mode de recherche utilisé par la source du média lors de la recherche d’un point particulier dans la présentation.

Une application peut définir le mode de recherche, pour la source du média, à utiliser lors de la création de l’objet. Une fois la source du média ASF créée avec le mode de recherche spécifié, elle ne peut pas être modifiée sur la source du média ou modifiée dynamiquement au cours d’une présentation. Les préférences de recherche sont spécifiées en tant que propriétés dans l’appel de l’application aux méthodes de programme de résolution source appropriées utilisées pour créer la source du média. Ces propriétés sont définies dans une banque de propriétés et transmises au paramètre *pProps* . Si ces propriétés ne sont pas passées, la source du média fonctionne avec les paramètres par défaut. Pour plus d’informations sur la définition de ces propriétés, consultez [configuration d’une source de média](configuring-a-media-source.md).

Si la recherche est autorisée, la source du média ASF prend en charge les modes de recherche suivants :

-   Recherche exacte : dans ce mode, la source du média ASF s’appuie sur l’objet d’index ASF du fichier ASF. Si le fichier n’a pas d’objet index, la recherche exacte est désactivée et l’un des autres modes est utilisé en fonction des propriétés spécifiées par l’application définies sur la source du média.
-   Recherche approximative : ce mode est demandé par l’application en transmettant [**MFPKEY \_ ASFMediaSource \_ ApproxSeek**](mfpkey-asfmediasource-approxseek-property.md) dans la Banque de propriétés aux méthodes de programme de résolution source appropriées. Toutefois, la recherche approximative n’est utilisée que si le flux d’octets ne prend pas en charge la recherche basée sur le temps. Dans ce mode, la source du média détermine une heure de début qui est relativement plus proche du temps de recherche. Si le fichier ASF contient un objet d’index ASF, il est utilisé pour calculer l’heure de début. La recherche approximative est moins précise mais plus rapide que la recherche exacte, car la durée de rendu du premier échantillon à l’heure de début prédéterminée est plus rapide.
-   Recherche itérative : pour définir ce mode, l’application doit définir la propriété [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) . La recherche itérative est un algorithme permettant de trouver une position dans un fichier ASF qui ne contient aucun objet d’index ASF. Dans ce mode, la source du média détermine une estimation approximative du point de recherche en lisant le décalage du flux d’octets. Elle utilise une série de approximations, en fonction de la vitesse de transmission moyenne, pour se rapprocher progressivement du temps de recherche cible. (L’algorithme est similaire à une recherche binaire.) La recherche itérative peut prendre plus de temps que la recherche à l’aide de l’objet index. elle est donc désactivée par défaut. Si vous définissez cette propriété, utilisez les propriétés suivantes pour définir les paramètres de recherche : [MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max \_ Count](mfpkey-asfmediasource-iterativeseek-max-count.md)[MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Tolerance \_ en \_ millisecondes](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md). Ces propriétés définissent respectivement le nombre maximal d’itérations et la tolérance. L’algorithme s’arrête lorsqu’il atteint le nombre maximal d’itérations, ou lorsqu’il trouve un paquet dont la distance par rapport à l’heure de recherche est comprise dans la tolérance spécifiée.

Pour résumer, l’application a la possibilité de choisir une recherche approximative ou itérative lorsque le fichier ASF ne contient pas d’objet d’index ASF.

## <a name="asf-media-source-object-model"></a>Modèle objet de source de média ASF

La source de média ASF implémente l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) et expose les interfaces suivantes. Une application peut obtenir une référence à ces interfaces en appelant **IMFMediaSource :: QueryInterface** sur la source du média ASF.



| Interface                                                | Description                                                                                                                                        |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | Obligatoire pour toutes les sources multimédias.                                                                                                                    |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Obligatoire pour toutes les sources multimédias. Permet aux applications d’extraire des événements de la source du média via la session multimédia.                                 |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Interroge la source du média pour l’interface de service spécifiée.                                                                                      |
| [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)               | Définit et obtient les propriétés de la source du média. Chaque propriété contient un nom descriptif et une valeur.                                               |
| [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                       | Décrit les métadonnées du fichier ASF.                                                                                                           |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)       | Récupère une collection de métadonnées, soit pour une présentation complète, soit pour un flux de la présentation.                                      |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Interroge la plage des taux de lecture pris en charge, y compris la lecture inversée.                                                                |
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                 | Obtient ou définit la vitesse de lecture.                                                                                                                    |
| [**IMFTrustedInput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput)               | Obtient l’ITA pour chacun des flux ASF contenus dans la source.                                                                                  |
| [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient)                     | Permet à une source de média de recevoir un pointeur vers l’interface [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) , qui est utilisée pour créer des objets dans le processus PMP. |
| [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)     | Convertit entre les codes de temps de la société d’appareils de télévision et de téléviseurs et les unités de temps de 100 nanosecondes.                              |



 

## <a name="asf-media-source-services"></a>Services source de média ASF

La source de média ASF fournit différents services dont l’étendue est un fichier ASF. Pour obtenir un pointeur vers un service particulier, l’application doit utiliser l’un des identificateurs de service suivants dans son appel à [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice). Pour plus d’informations, consultez [interfaces de service](service-interfaces.md).



| Identificateur de service               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SERVICE de contrôle de la \_ fréquence MF \_ \_       | À l’aide de cet identificateur, une application peut obtenir un pointeur vers des interfaces [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) ou [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) . En utilisant l’objet de prise en charge des taux implémenté par la source du média, l’application peut vérifier si un taux particulier est pris en charge par le fichier de média ASF sous-jacent, ce qui permet également d’obtenir le taux le plus rapide et le plus lent. En utilisant l’objet de contrôle de fréquence, l’application peut récupérer et définir la vitesse de lecture. Si l’application spécifie une vitesse particulière pour la lecture, la source de média ASF vérifie d’abord si le taux demandé est compris dans les limites du taux de transfert (déterminé par les tarifs rapides et les taux les plus lents), puis définit la vitesse. Cela ne vérifie pas les conditions variables, car le débit binaire peut changer à tout moment en fonction de la bande passante réseau. Pour plus d’informations, [le contrôle](rate-control.md)de la fréquence. |
| \_service de fournisseur de métadonnées MF \_ \_  | À l’aide de cet identificateur, l’application peut obtenir un pointeur vers l’interface [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) de la source de média ASF. Cette interface fournit l’accès aux informations sur le fichier ASF spécifiquement sur les objets d’en-tête ASF et les flux contenus dans le contenu multimédia. Les informations d’en-tête sont exposées par le biais d’attributs de descripteur de présentation et les informations de flux sont fournies via les attributs de descripteur Pour plus d’informations sur ces attributs, consultez [Media Foundation attributs pour les objets d’en-tête ASF](media-foundation-attributes-for-asf-header-objects.md). En plus des informations qui sont exposées par le biais d’attributs, il existe également des métadonnées descriptives, qui sont définies en tant que propriétés.                                                                                                 |
| \_service de \_ Gestionnaire de propriétés MF \_   | À l’aide de cet identificateur, l’application peut obtenir un pointeur vers l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) de la source de média ASF. La Banque de propriétés contient toutes les métadonnées relatives au fichier ASF. Cet identificateur est une nouveauté de Windows 7 et remplace le \_ \_ service de fournisseur de métadonnées MF \_ pour l’obtention des propriétés de métadonnées.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_service de statistiques MFNETSOURCE \_ | Pour plus d’informations, consultez récupération des statistiques réseau dans la [journalisation du client](client-logging.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| \_service de code temporel MF \_            | À l’aide de cet identificateur, l’application peut obtenir un pointeur vers l’interface [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) de la source du média. Cette implémentation peut être utilisée pour effectuer des traductions de code temporel, telles que la conversion du code de temps SMPTE en unités de 100-nano seconde et inversement.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="timecode-translation"></a>Traduction du code temporel

La source de média ASF fournit un service de traduction de code d’heure qui permet à votre application de convertir le code de temps SMPTE en heure de présentation la plus proche (en unité de 100 nanosecondes). Inversement, l’application peut également obtenir le code de temps pour l’heure de présentation demandée. Le service est disponible via l’interface [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) , que la source de média ASF implémente. Les appels de méthode sur ce pointeur d’interface sont asynchrones qui peuvent s’exécuter à partir de votre thread d’application principal sans bloquer l’interface utilisateur de votre application.

Les étapes suivantes résument la procédure de traduction du code temporel :

1.  Accédez à l’interface [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) de la source de média ASF en appelant [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) et en spécifiant l’identificateur de **\_ \_ service de code temporel MF** .
2.  Appelez [**IMFTimecodeTranslate :: BeginConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverttimecodetohns) ou [**IMFTimecodeTranslate :: BeginConvertHNSToTimecode**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverthnstotimecode) et spécifiez l’heure à traduire. Pour **BeginConvertTimecodeToHNS** , le code de temps doit être spécifié en tant que variable [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) avec le type de données **VT \_ i8** . La méthode **BeginConvertHNSToTimecode** requiert le temps en unités de 100 nanosecondes comme type [**MFTIME**](mftime.md) .
3.  Terminez l’opération asynchrone en appelant [**IMFTimecodeTranslate :: EndConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-endconverttimecodetohns) ou **IMFTimecodeTranslate :: EndConvertTimecodeToHNS** de manière appropriée.

Pendant la création de la source du média, le programme de résolution source crée un flux d’octets pour le fichier à partir duquel la source du média lit le contenu ASF. Pour que les conversions de temps soient réussies, le flux d’octets associé au fichier ASF doit avoir des fonctionnalités de recherche ; dans le cas contraire, l’application obtient l' \_ erreur MF E \_ BYTESTREAM \_ not \_ recherchée à partir de l’appel **Begin...** . Une autre exigence pour les conversions de temps est que le fichier ASF, représenté par la source de média ASF, doit avoir des objets d’index ASF. Les heures de présentation et les codes d’heure sont extraits des objets d’index ASF qui maintiennent tous les index et les points de recherche correspondants pour le fichier ASF. Pour la traduction de code dans le temps, le fichier ASF doit contenir un objet index simple ; pour la traduction du code de temps en présentation, le fichier ASF doit avoir un objet index. Les opérations de conversion s’appuient sur l' *indexeur* sous-jacent (composant WMContainer) pour analyser et lire l’objet index associé au fichier ASF. Si le fichier ne contient pas d’objet index, l’application reçoit de manière asynchrone le \_ code d’erreur MF E \_ no \_ index.

Pour traduire le temps demandé par l’application, la source du média énumère les flux dans le fichier et recherche le flux qui contient l’objet d’index ASF approprié. Si un flux de ce type est trouvé, la source du média analyse les paquets ASF du flux est analysé jusqu’à ce que le code d’heure correct soit atteint. Après avoir trouvé l’exemple correct, il récupère l’heure de présentation correspondante ou le code de temps de l’exemple, puis le retourne à l’appelant.

### <a name="script-command-support"></a>Prise en charge des commandes de script

Lorsque vous générez une topologie ASF qui contient un flux de script, un nœud de flux de script est ajouté à la topologie. Ce nœud enverra IMFSamples à l’heure appropriée. Le IMFSample fourni par le nœud source du script stocke les données dans le IMFMediaBuffer associé à l’exemple. Vous pouvez appeler CopyToBuffer sur l’exemple pour récupérer un IMFMediaBuffer, puis appeler Lock sur la mémoire tampon pour récupérer les données. 

Les charges utiles de flux de script sont empaquetées dans la mémoire tampon sous la forme d’une chaîne de type, suivie de NULL, puis de la chaîne de commande, puis de la valeur NULL. Les chaînes sont au format ASF Unicode.

Par exemple, une charge utile peut se présenter comme suit (où \ 0 indique un caractère NULL) :

*URL\0http://contoso.com\0*

*Text\0This est un caption\0*



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Composants ASF de couche de pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
