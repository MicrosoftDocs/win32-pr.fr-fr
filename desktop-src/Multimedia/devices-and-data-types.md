---
title: Appareils et types de données
description: Appareils et types de données
ms.assetid: 46247983-19c3-4c7a-a615-ba6cd8bd3289
keywords:
- sons Waveform, ouverture des périphériques de sortie
- Waveform-interface audio, ouverture des périphériques de sortie
- ouverture de périphériques de sortie Waveform-Audio
- audio Wave, interrogation des périphériques de sortie
- Waveform-interface audio, interrogation des périphériques de sortie
- interrogation des périphériques de sortie Waveform-Audio
- sons Waveform, handles d’appareil
- Waveform-interface audio, handles de l’appareil
- audio Wave, identificateurs d’appareil
- Waveform-interface audio, identificateurs de périphérique
- Wave audio, types de données de sortie
- Waveform-interface audio, types de données de sortie
- audio Wave, formats de données
- Waveform-interface audio, formats de données
- écriture de données Waveform-Audio
- sons Waveform, écriture de données
- Waveform-interface audio, écriture de données
- Waveform PCM-données audio
- audio Wave, données PCM
- Waveform-interface audio, données PCM
- sons Wave, fermeture des appareils de sortie
- Waveform-interface audio, fermeture des appareils de sortie
- fermeture des périphériques de sortie Waveform-Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2abe0c2c20c52f4498316fb619885d41f85e41d6
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120244"
---
# <a name="devices-and-data-types"></a>Appareils et types de données

Cette section décrit l’utilisation des périphériques audio Waveform et contient des informations sur l’ouverture, la fermeture et l’interrogation de leurs fonctionnalités. Elle explique également comment effectuer le suivi des appareils dans un système à l’aide de handles d’appareil et d’identificateurs de périphérique.

## <a name="opening-waveform-audio-output-devices"></a>Ouverture de Waveform-Audio périphériques de sortie

Utilisez la fonction [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) pour ouvrir un appareil de sortie Waveform-Audio en vue de la lecture. Cette fonction ouvre l’appareil associé à l’identificateur de périphérique spécifié et retourne un handle de l’appareil ouvert en écrivant le handle d’un emplacement de mémoire spécifié.

Certains ordinateurs multimédias possèdent plusieurs périphériques de sortie Waveform-Audio. À moins que vous ne souhaitiez ouvrir un périphérique de sortie Waveform-Audio spécifique dans un système, vous devez utiliser l' \_ indicateur Wave mapper pour l’identificateur de l’appareil lorsque vous ouvrez un appareil. La fonction **waveOutOpen** choisit l’appareil dans le système qui est le mieux capable de lire le format de données spécifié.

## <a name="querying-audio-devices"></a>Interrogation des périphériques audio

Windows fournit les fonctions suivantes pour déterminer le nombre d’appareils d’un certain type qui sont disponibles dans un système.



| Fonction                                       | Description                                                                  |
|------------------------------------------------|------------------------------------------------------------------------------|
| [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)         | Récupère le nombre d’appareils de sortie auxiliaire présents dans le système.      |
| [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)   | Récupère le nombre d’appareils d’entrée Waveform-Audio présents dans le système.  |
| [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) | Récupère le nombre d’appareils de sortie Waveform-Audio présents dans le système. |



 

Les périphériques audio sont identifiés par un identificateur de périphérique. L’identificateur d’appareil est déterminé implicitement à partir du nombre d’appareils présents dans un système. Les identificateurs d’appareil sont compris entre zéro et un nombre inférieur au nombre d’appareils présents. Par exemple, s’il existe deux périphériques de sortie Waveform-Audio dans un système, les identificateurs d’appareil valides sont 0 et 1.

Une fois que vous avez déterminé le nombre d’appareils d’un certain type présents dans un système, vous pouvez utiliser l’une des fonctions suivantes pour interroger les fonctionnalités de chaque appareil.



| Fonction                                       | Description                                                             |
|------------------------------------------------|-------------------------------------------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | Récupère les fonctionnalités d’un périphérique de sortie auxiliaire spécifié.      |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | Récupère les fonctionnalités d’un périphérique d’entrée audio Wave spécifié.  |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | Récupère les fonctionnalités d’un périphérique de sortie Waveform-Audio spécifié. |



 

Chacune de ces fonctions remplit une structure avec des informations sur les fonctionnalités d’un appareil spécifié. Le tableau suivant répertorie les structures qui correspondent à chacune de ces fonctions.



|  Fonction                                              |  Structure                                  |
|------------------------------------------------|------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)         |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)   |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) |



 

Les formats standard sont répertoriés dans le membre **dwFormats** de la structure **WAVEOUTCAPS** . Les périphériques Wave-audio peuvent prendre en charge des formats non standard. Pour déterminer si un format particulier (standard ou non standard) est pris en charge par un appareil, vous pouvez appeler la fonction [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) avec \_ l' \_ indicateur de requête format Wave. Cet indicateur n’ouvre pas l’appareil. Vous spécifiez le format en question dans la structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) vers laquelle pointe le paramètre *Pwfx* passé à **waveOutOpen**.

Les périphériques de sortie Waveform-Audio varient en fonction des fonctionnalités qu’ils prennent en charge. Le membre **dwSupport** de la structure [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) indique si un appareil prend en charge des fonctionnalités telles que les modifications de volume et de tangage.

## <a name="device-handles-and-device-identifiers"></a>Handles d’appareil et identificateurs de périphérique

Chaque fonction qui ouvre un périphérique audio spécifie un identificateur de périphérique, un pointeur vers un emplacement de mémoire et certains paramètres qui sont propres à chaque type d’appareil. L’emplacement de la mémoire est rempli avec un handle d’appareil. Utilisez ce handle d’appareil pour identifier le périphérique audio ouvert lors de l’appel d’autres fonctions audio.

La différence entre les identificateurs et les descripteurs pour les périphériques audio est subtile mais importante :

-   Les identificateurs d’appareil sont déterminés implicitement à partir du nombre d’appareils présents dans un système. Ce nombre est obtenu à l’aide de la fonction [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)ou [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) .
-   Des descripteurs d’appareil sont retournés lorsque les pilotes de périphérique sont ouverts à l’aide de la fonction [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) ou [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .

Il n’existe aucune fonction qui ouvre ou ferme des périphériques audio auxiliaires. Les périphériques audio auxiliaires n’ont pas besoin d’être ouverts et fermés comme des périphériques audio Waveform, car aucun transfert de données continu n’est associé. Toutes les fonctions audio auxiliaires utilisent des identificateurs d’appareil pour identifier les appareils.

## <a name="waveform-audio-output-data-types"></a>Types de données de sortie Waveform-Audio

Les types de données suivants sont définis pour les fonctions de sortie Waveform-Audio.



| Type                                 | Description                                                                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEOUT**                         | Handle vers un périphérique de sortie Waveform-Audio ouvert.                                                                                                               |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Structure qui spécifie les formats de données pris en charge par un périphérique d’entrée Waveform-Audio particulier. Cette structure est également des périphériques d’entrée Waveform-Audio usedfor. |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Structure utilisée comme en-tête d’un bloc de données d’entrée Waveform Audio. Cette structure est également utilisée pour les périphériques d’entrée Waveform-Audio.                            |
| [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)   | Structure utilisée pour interroger les fonctionnalités d’un périphérique de sortie Waveform-Audio particulier.                                                                        |



 

## <a name="specifying-waveform-audio-data-formats"></a>Spécification des formats de données Waveform-Audio

Quand vous appelez la fonction [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) pour ouvrir un pilote de périphérique pour la lecture ou pour demander si le pilote prend en charge un format de données particulier, utilisez le paramètre *pwfx* pour spécifier un pointeur vers une structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) contenant le format de données Waveform-Audio demandé. **WAVEFORMATEX** remplace les structures [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) et [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) .

Pour les données audio qui sont séparées en plus de deux canaux ou dont la taille n’est pas un multiple de 8, vous devez utiliser [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible). Cette structure configure simplement les octets supplémentaires pointés par le membre **cbSize** de **WAVEFORMATEX** pour fournir des informations supplémentaires sur le format. **WAVEFORMATEXTENSIBLE** peut être casté en **WAVEFORMATEX**.

Il existe également deux formats de presse-papiers que vous pouvez utiliser pour représenter des données audio : CF \_ Wave et CF \_ riff. Utilisez le \_ format CF Wave pour représenter les données dans l’un des formats standard, par exemple, 11 kHz ou 22 kHz PCM. Utilisez le \_ format CF riff pour représenter des formats de données plus complexes qui ne peuvent pas être représentés sous forme de fichiers audio Waveform standard.

## <a name="writing-waveform-audio-data"></a>Écriture de données Waveform-Audio

Après avoir ouvert un pilote de périphérique de sortie Waveform-Audio, vous pouvez commencer à émettre un son. Windows fournit la fonction [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) pour envoyer des blocs de données à des périphériques de sortie Waveform-Audio.

Utilisez la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) pour spécifier le bloc de données Waveform-Audio que vous envoyez à l’aide de **waveOutWrite**. Cette structure contient un pointeur vers un bloc de données verrouillé, la longueur du bloc de données et certains indicateurs. Ce bloc de données doit être préparé avant de l’utiliser. Pour plus d’informations sur la préparation d’un bloc de données, consultez [blocs de données audio](audio-data-blocks.md).

Après avoir envoyé un bloc de données à un périphérique de sortie à l’aide de **waveOutWrite**, vous devez attendre que le pilote de périphérique se termine avec le bloc de données avant de le libérer. Si vous envoyez plusieurs blocs de données, vous devez surveiller l’achèvement des blocs de données pour savoir quand envoyer des blocs supplémentaires. Pour plus d’informations sur les blocs de données, consultez [blocs de données audio](audio-data-blocks.md).

## <a name="pcm-waveform-audio-data-format"></a>Format de données PCM Waveform-Audio

Le membre **lpData** de la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) pointsetts aux exemples de données Waveform-Audio. Pour les données PCM 8 bits, chaque échantillon est représenté par un seul octet de données non signé. Pour les données PCM 16 bits, chaque échantillon est représenté par une valeur signée 16 bits. Le tableau suivant récapitule les valeurs maximales, minimales et maximales des données PCM Waveform-Audio.



| Format de données | Valeur maximale   | Valeur minimale    | Valeur de milieu |
|-------------|-----------------|------------------|----------------|
| PCM 8 bits   | 255 (0xFF)      | 0                | 128 (0x80)     |
| PCM 16 bits  | 32 767 (0x7FFF) | – 32 768 (0x8000) | 0              |



 

## <a name="pcm-data-packing"></a>Compression de données PCM

L’ordre des octets de données varie selon les formats 8 bits et 16 bits et entre les formats mono et stéréo. La liste suivante décrit la compression des données pour les différents formats de données Waveform PCM-audio.



| Waveform PCM-format audio | Description                                                                                                                                                                                                                                                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mono 8 bits                | Chaque échantillon est 1 octet qui correspond à un canal audio unique. L’exemple 1 est suivi des exemples 2, 3, 4, et ainsi de suite.                                                                                                                                                                                                                           |
| stéréo 8 bits              | Chaque échantillon est de 2 octets. L’exemple 1 est suivi des exemples 2, 3, 4, et ainsi de suite. Pour chaque exemple, le premier octet est le canal 0 (le canal de gauche) et le deuxième octet est le canal 1 (le canal de droite).                                                                                                                                               |
| mono 16 bits               | Chaque échantillon est de 2 octets. L’exemple 1 est suivi des exemples 2, 3, 4, et ainsi de suite. Pour chaque exemple, le premier octet est l’octet de poids faible du canal 0 et le deuxième octet est l’octet de poids fort du canal 0.                                                                                                                                         |
| stéréo 16 bits             | Chaque échantillon est de 4 octets. L’exemple 1 est suivi des exemples 2, 3, 4, et ainsi de suite. Pour chaque exemple, le premier octet est l’octet de poids faible du canal 0 (canal gauche); le deuxième octet est l’octet de poids fort du canal 0 ; le troisième octet est l’octet de poids faible du canal 1 (canal de droite); et le quatrième octet est l’octet de poids fort du canal 1. |
| Autres                    | Chaque échantillon est contenu dans un bloc qui est un multiple de 4 octets, mais les exemples peuvent être alignés sur un octet. La disposition des canaux est spécifiée par un masque. Pour plus d’informations, consultez [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible).                                                                                                 |



 

## <a name="closing-waveform-audio-output-devices"></a>Fermeture des appareils de sortie Waveform-Audio

Une fois la lecture de la forme d’onde-audio terminée, appelez [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) pour fermer le périphérique de sortie. Si **waveOutClose** est appelé pendant la lecture d’un fichier Waveform-Audio, l’opération de fermeture échoue et la fonction retourne un code d’erreur indiquant que l’appareil n’a pas été fermé. Si vous ne souhaitez pas attendre la fin de la lecture avant de fermer l’appareil, appelez la fonction [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) avant de fermer. Cela termine la lecture et permet la fermeture de l’appareil. Veillez à utiliser la fonction [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) pour nettoyer la préparation sur tous les blocs de données avant de fermer l’appareil.

 

 