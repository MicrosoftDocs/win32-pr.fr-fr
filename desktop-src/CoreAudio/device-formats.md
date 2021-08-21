---
description: Formats d’appareil
ms.assetid: 591437e4-21ef-42f1-a752-7f50440cbd63
title: Formats d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332f3ecd4b30213328552077bdef040a63e31992deaf217b77838dd0cd0797f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957338"
---
# <a name="device-formats"></a>Formats d’appareil

pour une application audio, l’un des avantages de l’utilisation d’une api audio de niveau supérieur, comme DirectSound ou la Windows fonctions **waveOutXxx** multimédias, est que l’api effectue automatiquement une conversion entre les formats de flux utilisés par l’application et les formats utilisés par le périphérique audio. En revanche, les API audio principales sont plus restrictives, car elles nécessitent des flux d’application pour utiliser des formats qui sont identiques à, ou qui sont étroitement liés aux formats utilisés par l’appareil. Ainsi, les applications qui utilisent les API audio de base pour lire ou enregistrer des flux audio peuvent être nécessaires pour effectuer une partie ou la totalité des conversions entre les formats de flux.

Une application qui utilise WASAPI pour gérer des flux en mode partagé peut s’appuyer sur le moteur audio pour effectuer uniquement des conversions de format limitées. Le moteur audio peut effectuer une conversion entre une taille d’échantillon PCM standard utilisée par l’application et les échantillons à virgule flottante que le moteur utilise pour son traitement interne. Toutefois, le format d’un flux d’application doit généralement avoir le même nombre de canaux et le même taux d’échantillonnage que le format de flux utilisé par l’appareil.

Si une application utilise un appareil en mode exclusif, l’application doit utiliser un format de flux pris en charge explicitement par le matériel audio. En mode exclusif, l’application et l’appareil échangent les données audio directement, sans intervention du moteur audio.

De nombreux périphériques audio prennent en charge les formats de flux PCM et non-PCM. Toutefois, le moteur audio ne peut mélanger que des flux PCM. Ainsi, seuls les flux en mode exclusif peuvent avoir des formats non-PCM. En outre, seuls les formats non PCM avec des taux de données fixes sont pris en charge en mode exclusif. un exemple de format non-PCM à débit fixe est un flux Audio 48-kHz Windows Media Audio Professional (WMA Pro) qui passe par un lien S/PDIF (Sony digital interface) au format numérique sans être décodé. pour plus d’informations sur l’utilisation des flux de Pro WMA sur S/PDIF, consultez la documentation suivante :

-   description de la \_ \_ balise wave format \_ wave SPDIF SPDIF-format dans la documentation Windows DDK.
-   le livre blanc intitulé « prise en charge des pilotes audio pour le Format WMA Pro-sur-S/PDIF » sur les [Technologies de périphériques audio pour Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) site web.

WASAPI utilise une structure **WAVEFORMATEX** ou **WAVEFORMATEXTENSIBLE** pour spécifier un format de flux. Une structure **WAVEFORMATEXTENSIBLE** est effectivement une structure **WAVEFORMATEX** qui a été étendue pour décrire un plus grand nombre de formats. Tout format qui peut être décrit par une structure **WAVEFORMATEX** autonome peut également être décrit par une structure **WAVEFORMATEXTENSIBLE** .

Le premier membre de la structure **WAVEFORMATEXTENSIBLE** est une structure **WAVEFORMATEX** . Le contenu d’une structure **WAVEFORMATEX** indique s’il s’agit d’une structure **WAVEFORMATEX** autonome ou d’une partie d’une structure **WAVEFORMATEXTENSIBLE** .

Une structure **WAVEFORMATEX** autonome peut décrire correctement un format avec un ou deux canaux et une taille d’échantillon qui est un multiple de 8 bits. En soi, une structure **WAVEFORMATEX** ne peut pas spécifier le mappage de canaux aux positions de haut-parleur. De plus, bien que **WAVEFORMATEX** spécifie la taille du conteneur pour chaque échantillon audio, il ne peut pas spécifier le nombre de bits de précision dans un échantillon (par exemple, 20 bits de précision dans un conteneur de 24 bits). En revanche, la structure **WAVEFORMATEXTENSIBLE** peut spécifier le mappage des canaux aux intervenants et le nombre de bits de précision dans chaque échantillon.

pour plus d’informations sur **WAVEFORMATEX** et **WAVEFORMATEXTENSIBLE**, consultez la documentation Windows DDK.

à partir de Windows 7, **WAVEFORMATEXTENSIBLE** a été étendu pour représenter les formats d’appareil pour la transmission de données audio encodées via une interface compatible IEC 61937. Pour plus d’informations sur la nouvelle structure, consultez [représentation des formats des transmissions IEC 61937](representing-formats-for-iec-61937-transmissions.md).

### <a name="specifying-the-device-format"></a>Spécification du format du périphérique

Les méthodes WASAPI suivantes utilisent les structures **WAVEFORMATEX** et **WAVEFORMATEXTENSIBLE** pour décrire les formats de flux :

-   [**IAudioClient::GetMixFormat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)
-   [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)

La méthode **GetMixFormat** récupère le format de flux que le moteur audio utilise pour son traitement interne des flux en mode partagé. La méthode utilise toujours une structure **WAVEFORMATEXTENSIBLE** , au lieu d’une structure **WAVEFORMATEX** autonome, pour spécifier le format.

La méthode **IsFormatSupported** indique si un périphérique de point de terminaison audio prend en charge un format de flux particulier. L’appelant doit spécifier si le format de flux est destiné à être utilisé en mode partagé ou en mode exclusif. Pour les formats en mode partagé, la méthode interroge le moteur audio pour déterminer s’il prend en charge le format spécifié. Pour les formats en mode exclusif, la méthode interroge le pilote de périphérique. Certains pilotes de périphérique signalent qu’ils prennent en charge un format PCM à 1 ou 2 canaux si le format est spécifié par une structure **WAVEFORMATEX** autonome, mais ils rejettent le même format s’ils sont spécifiés par une structure **WAVEFORMATEXTENSIBLE** . Pour obtenir des résultats fiables à partir de ces pilotes, les applications en mode exclusif doivent appeler **IsFormatSupported** deux fois pour chaque format PCM à 1 ou 2 canaux : un appel doit utiliser une structure **WAVEFORMATEX** autonome pour spécifier le format, et l’autre appel doit utiliser une structure **WAVEFORMATEXTENSIBLE** pour spécifier le même format.

Une fois qu’une application a utilisé **GetMixFormat** ou **IsFormatSupported** pour trouver un format approprié pour un flux en mode partagé ou en mode exclusif, l’application peut appeler la méthode **Initialize** pour initialiser un flux de ce format. Une application qui tente d’initialiser un flux en mode partagé dont le format n’est pas identique à celui obtenu à partir de la méthode **GetMixFormat** , mais qui a le même nombre de canaux et le même taux d’échantillonnage que le format Mix, est susceptible d’échouer. Avant **d’appeler Initialize**, l’application peut appeler **IsFormatSupported** pour vérifier que **Initialize** accepte le format.

Le format Mix que le moteur audio utilise pour son traitement interne des flux en mode partagé est étroitement lié à, mais il n’est pas nécessairement identique au format de flux que l’appareil de point de terminaison audio utilise en mode partagé. par le biais du panneau de configuration Windows multimédia, Mmsys.cpl, l’utilisateur peut sélectionner le format de flux qu’un périphérique de point de terminaison audio utilisera lorsqu’il fonctionne en mode partagé. Les étapes sont les suivantes :

1.  Pour exécuter Mmsys.cpl, ouvrez une fenêtre d’invite de commandes et entrez la commande suivante :

    **mmsys.cplde contrôle**

    Vous pouvez également exécuter Mmsys.cpl en cliquant avec le bouton droit sur l’icône de haut-parleur dans la zone de notification, située sur le côté droit de la barre des tâches, puis en sélectionnant **périphériques de lecture** ou **périphériques d’enregistrement**.

2.  Une fois la fenêtre de Mmsys.cpl ouverte, sélectionnez un appareil dans la liste des périphériques de lecture ou la liste des périphériques d’enregistrement, puis cliquez sur **Propriétés**.
3.  Lorsque la fenêtre Propriétés s’ouvre, cliquez sur **avancé**, puis sélectionnez un format dans la liste des formats disponibles dans la zone **format par défaut**.

Par exemple, supposons que l’utilisateur sélectionne le format par défaut suivant dans la liste des formats disponibles pour un périphérique de lecture :

**2 canaux, 16 bits, 44100 Hz (qualité du CD)**

Il s’agit du format que l’appareil utilisera par la suite lorsqu’il fonctionne en mode partagé. dans Windows Vista, le moteur audio utilise une version légèrement modifiée de ce format pour son traitement interne des flux en mode partagé. Le moteur audio utilise un format avec le même nombre de canaux (deux) et le même taux d’échantillonnage (44100 Hz), mais il convertit les exemples en nombres à virgule flottante avant de les traiter. Le moteur audio convertit les échantillons à virgule flottante dans la combinaison de sortie en entiers 16 bits avant de les relire via l’appareil.

Une application peut interroger la propriété [**\_ AudioEngine \_ DeviceFormat**](pkey-audioengine-deviceformat.md) de l’appareil de point de terminaison audio pour obtenir le format en mode partagé que l’utilisateur a sélectionné pour l’appareil. Pour plus d’informations sur l’interrogation des propriétés d’un appareil, consultez Propriétés de l' [appareil](device-properties.md).

Certaines applications peuvent trouver le format spécifié par la propriété **\_ AudioEngine \_ DeviceFormat** d’un appareil pour être un format approprié pour l’ouverture d’un flux en mode exclusif sur l’appareil. D’autres applications qui gèrent des flux en mode exclusif peuvent avoir des exigences supplémentaires qui exigent une négociation de format complexe avec l’appareil. En règle générale, l’une de ces applications construit une liste de formats appropriés, avec les formats préférés au début de la liste. L’application appelle ensuite de manière itérative **IsFormatSupported** avec chaque format successif de la liste, en commençant au début de la liste, jusqu’à ce qu’elle trouve un format pris en charge par l’appareil.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques de point de terminaison audio](audio-endpoint-devices.md)
</dt> </dl>

 

 



