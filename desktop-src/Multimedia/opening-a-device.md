---
title: Ouverture d’un appareil
description: Ouverture d’un appareil
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- Commande MCI_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd975b0dd5004fb4b1209003568b7fd5901cfc4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416794"
---
# <a name="opening-a-device"></a>Ouverture d’un appareil

Avant d’utiliser un appareil, vous devez l’initialiser à l’aide de la commande [**ouvrir**](open.md) ([**MCI \_ Open**](mci-open.md)). Cette commande charge le pilote dans la mémoire (s’il n’est pas déjà chargé) et récupère l’identificateur d’appareil que vous allez utiliser pour identifier l’appareil dans les commandes MCI suivantes. Vous devez vérifier la valeur de retour de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) ou [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avant d’utiliser un nouvel identificateur d’appareil pour vous assurer que l’identificateur est valide. (Vous pouvez également récupérer un identificateur d’appareil à l’aide de la fonction [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) .)

Comme tous les messages de commande MCI, l' **\_ ouverture de MCI** a une structure associée. Ces structures sont parfois appelées des *blocs de paramètres*. La structure par défaut pour **MCI \_ ouverte** est [**MCI \_ Open \_ PARMS**](mci-open-parms.md). Certains appareils (tels que *la forme d’onde* et la *superposition*) ont des structures étendues (telles que les paramètres [**\_ \_ Open Wave \_ MCI**](mci-wave-open-parms.md) et les paramètres d' [**\_ \_ ouverture OVLY Open \_ parms**](mci-ovly-open-parms.md)) pour prendre en charge des paramètres facultatifs supplémentaires. À moins que vous n’ayez besoin d’utiliser ces paramètres supplémentaires, vous pouvez utiliser la structure **\_ Open \_ PARMS des MCI** avec n’importe quel périphérique MCI.

Le nombre d’appareils que vous pouvez ouvrir est limité uniquement par la quantité de mémoire disponible.

## <a name="using-an-alias"></a>Utilisation d’un alias

Lorsque vous ouvrez un appareil, vous pouvez utiliser l’indicateur « alias » pour spécifier un identificateur de périphérique pour l’appareil. Cet indicateur vous permet d’attribuer un identificateur d’appareil abrégé pour les appareils composés avec des noms de fichiers longs, et il vous permet d’ouvrir plusieurs instances du même fichier ou périphérique.

Par exemple, la commande suivante attribue l’identificateur d’appareil « birdcall » au nom de fichier de base C : \\ NABIRDS \\ Sounds \\ MOCKMTNG. WAV


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Dans l’interface de message de commande, vous spécifiez un alias à l’aide du membre **lpstrAlias** de la structure des [**\_ \_ PARMS Open PARMS**](mci-open-parms.md) .

## <a name="specifying-a-device-type"></a>Spécification d’un type d’appareil

Lorsque vous ouvrez un appareil, vous pouvez utiliser l’indicateur « type » pour faire référence à un type d’appareil, plutôt qu’à un pilote de périphérique spécifique. L’exemple suivant ouvre le fichier Waveform-Audio C : \\ Windows \\ carillon. WAV (à l’aide de l’indicateur « type » pour spécifier le type d’appareil **WaveAudio** ) et attribue l’alias « carillons » :


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Dans l’interface de message de commande, les fonctionnalités de l’indicateur « type » sont fournies par le membre **lpstrDeviceType** de la structure des fonctions [**\_ Open \_ PARMS de MCI**](mci-open-parms.md) .

## <a name="simple-and-compound-devices"></a>Appareils simples et composés

MCI classifie les pilotes de périphériques comme *composés* ou *simples*. Les pilotes pour les appareils composés nécessitent le nom d’un fichier de données pour la lecture. les pilotes pour les périphériques simples ne le sont pas.

Les appareils simples incluent des appareils **cdaudio** et **videodisc** . Il existe deux façons d’ouvrir des appareils simples :

-   Spécifiez un pointeur vers une chaîne se terminant par un caractère null qui contient le nom de l’appareil à partir du registre ou du fichier SYSTEM.INI.

    Par exemple, vous pouvez ouvrir un appareil **videodisc** à l’aide de la commande suivante :


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



Dans ce cas, « videodisc » est le nom de l’appareil à partir du registre ou \[ \] de la section mci de SYSTEM.INI.

-   Spécifiez le nom réel du pilote de périphérique. Toutefois, l’ouverture d’un appareil à l’aide du nom de fichier du pilote de périphérique rend l’application spécifique au périphérique et peut empêcher l’application de s’exécuter en cas de modification de la configuration du système. Si vous utilisez un nom de fichier, vous n’avez pas besoin de spécifier le chemin d’accès complet ou l’extension de nom de fichier ; MCI suppose que les pilotes se trouvent dans un répertoire système et ont le. Nom de l’extension de nom de fichier.

Les appareils composés comprennent les **WaveAudio** et les appareils **Sequencer** . Les données d’un appareil composé sont parfois appelées *éléments d’appareil*. Toutefois, ce document fait généralement référence à ces données sous la forme d’un fichier, même si, dans certains cas, les données peuvent ne pas être stockées sous forme de fichier.

Il existe trois façons d’ouvrir un appareil composé :

-   Spécifiez uniquement le nom de l’appareil. Cela vous permet d’ouvrir un appareil composé sans associer de nom de fichier. La plupart des appareils composés traitent uniquement les commandes de [**capacité**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) et de [**fermeture**](close.md) ([**MCI \_ Close**](mci-close.md)) lorsqu’ils sont ouverts de cette manière.
-   Spécifiez uniquement le nom de fichier. Le nom de l’appareil est déterminé à partir des associations du Registre.
-   Spécifiez le nom du fichier et le nom de l’appareil. MCI ignore les entrées dans le registre et ouvre le nom de périphérique spécifié.

Pour associer un fichier de données à un appareil particulier, vous pouvez spécifier le nom de fichier et le nom de l’appareil. Par exemple, la commande suivante ouvre l’appareil **WaveAudio** avec le nom de fichier MYVOICE. SND


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Dans l’interface de chaîne de commande, vous pouvez également abréger la spécification de nom de périphérique à l’aide du format de point d’exclamation alternatif, comme indiqué dans la commande [**ouvrir**](open.md) .

## <a name="opening-a-device-using-the-filename-extension"></a>Ouverture d’un appareil à l’aide de l’extension de nom de fichier

Si la commande [**ouvrir**](open.md) ([**MCI \_ Open**](mci-open.md)) spécifie uniquement le nom de fichier, MCI utilise l’extension de nom de fichier pour sélectionner l’appareil approprié dans la liste du registre ou dans la \[ \] section des extensions MCI du fichier SYSTEM.INI. Les entrées de la \[ section des extensions MCI \] utilisent la forme suivante :

nom du périphérique d' *\_ extension de nom de fichier*  =  *\_*

MCI utilise implicitement *le \_ nom* de l’appareil si l’extension est trouvée et si un nom de périphérique n’a pas été spécifié dans la commande **ouvrir** .

L’exemple suivant montre une \[ section d’extensions MCI standard \] :


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



À l’aide de ces définitions, MCI ouvre l’appareil **WaveAudio** si la commande suivante est émise :


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a>Nouveaux fichiers de données

Pour créer un nouveau fichier de données, spécifiez simplement un nom de fichier vide. MCI n’enregistre pas un nouveau fichier tant que vous ne l’avez pas enregistré à l’aide de la commande [**Enregistrer**](save.md) ([**\_ enregistrement MCI**](mci-save.md)). Lorsque vous créez un fichier, vous devez inclure un alias d’appareil avec la commande [**ouvrir**](open.md) ([**MCI \_ Open**](mci-open.md)).

L’exemple suivant ouvre un nouveau fichier **WaveAudio** , démarre et arrête l’enregistrement, puis enregistre et ferme le fichier :


```C++
mciSendString("open new type waveaudio alias capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("record capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("stop capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("save capture orca.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="sharable-devices"></a>Appareils partageables

L’indicateur « partageable » (MCI \_ Open \_ Shared) de la commande [**ouverte**](open.md) ([**MCI \_ Open**](mci-open.md)) permet à plusieurs applications d’accéder simultanément au même appareil (ou fichier) et à l’instance d’appareil. Si votre application ouvre un appareil ou un fichier comme partageable, d’autres applications peuvent également y accéder en l’ouvrant comme partageable. L’appareil ou le fichier partagé donne à chaque application la possibilité de modifier les paramètres régissant son état d’exécution. Chaque fois qu’un appareil ou un fichier est ouvert en tant que partageable, MCI retourne un identificateur d’appareil unique, même si les identificateurs font référence à la même instance.

Si votre application ouvre un appareil ou un fichier sans spécifier qu’elle est partageable, aucune autre application ne peut y accéder jusqu’à ce que votre application la ferme. En outre, si un appareil ne prend en charge qu’une seule instance ouverte, la commande **Open** échoue si vous spécifiez l’indicateur partageable.

Si votre application ouvre un appareil et spécifie qu’il peut être partagé, votre application ne doit pas faire d’hypothèses concernant l’état de cet appareil. Votre application peut avoir besoin de compenser les modifications apportées par d’autres applications qui accèdent à l’appareil.

La plupart des fichiers composés ne peuvent pas être partagés ; Toutefois, vous pouvez ouvrir plusieurs fichiers, ou vous pouvez ouvrir un seul fichier à la fois. Si vous ouvrez un seul fichier à plusieurs moments, MCI crée une instance indépendante pour chaque instance, chaque instance ayant un état de fonctionnement unique.

Si vous ouvrez plusieurs instances d’un fichier, vous devez assigner un identificateur d’appareil unique à chacun d’eux. Vous pouvez utiliser un alias, comme décrit dans la section suivante, pour attribuer un nom unique à chaque fichier.

 

 