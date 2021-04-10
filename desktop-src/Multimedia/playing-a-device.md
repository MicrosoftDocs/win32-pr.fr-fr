---
title: La diffusion d’un appareil
description: La diffusion d’un appareil
ms.assetid: 48d83e06-9e6e-498b-ad9b-0b66f235db25
keywords:
- Commande MCI_PLAY
- MCIAVI, fenêtre de lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73d8b6539e842a1ffa632ed1efae5c2c8d3cda1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940990"
---
# <a name="playing-a-device"></a>La diffusion d’un appareil

La commande [**Play**](play.md) ([**\_ lecture MCI**](mci-play.md)) démarre la lecture d’un appareil. Sans indicateurs, cette commande démarre à partir de la position actuelle et est lue jusqu’à ce que la commande soit interrompue ou jusqu’à ce que la fin du support ou du fichier soit atteinte. Après la lecture, la position actuelle est à la fin du média. Vous pouvez également utiliser la commande [**Seek**](seek.md) ([**MCI \_ Seek**](mci-seek.md)) pour modifier la position actuelle.

La plupart des appareils qui prennent en charge la commande de **lecture** prennent également en charge les indicateurs « from » (MCI \_ de) et « to » (MCI \_ à). Ces indicateurs indiquent la position à laquelle l’appareil doit démarrer et s’arrêter. Par exemple, la commande suivante lit un disque audio CD à partir du début de la première piste à l’aide de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :


```C++
mciSendString("play cdaudio from 0", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Certains types d’appareils étendent cette commande pour exploiter les fonctionnalités d’un appareil particulier. Par exemple, la commande [**Play**](play.md) pour le type d’appareil **videodisc** comprend les indicateurs « Fast » (MCI \_ VD \_ Play Play \_ ), « Slow » (MCI \_ VD \_ Play \_ Slow) et « Scan » (MCI \_ VD \_ Play \_ Scan).

> [!Note]  
> Les unités affectées à la valeur de position dépendent du format d’heure utilisé par l’appareil. Chaque appareil a un format d’heure par défaut, mais vous devez spécifier le format d’heure à l’aide de la commande [**Set**](set.md) ([**MCI \_ Set**](mci-set.md)) avant d’émettre des commandes qui utilisent des valeurs de position.

 

## <a name="playing-an-avi-file"></a>Exécution d’un fichier AVI

Les fichiers vidéo dans Windows sont constitués d’au moins deux flux de données entrelacés : un flux vidéo (image) et un flux audio. Vous pouvez facilement lire ces fichiers AVI (Audio-Video entrelacés) à l’aide de commandes MCI. Les sections suivantes traitent de la diffusion de fichiers AVI.

## <a name="setting-up-an-mciavi-playback-window"></a>Configuration d’une fenêtre de lecture de MCIAVI

Votre application peut spécifier les options suivantes pour définir la fenêtre de lecture pour la lecture d’un fichier AVI :

-   Utilisez la fenêtre contextuelle par défaut du pilote MCIAVI.
-   Spécifiez une fenêtre parente et un style de fenêtre que le pilote MCIAVI peut utiliser pour créer la fenêtre de lecture.
-   Spécifiez une fenêtre de lecture pour le pilote MCIAVI à utiliser pour la lecture.
-   Lisez le fichier AVI dans un affichage plein écran.

Si votre application ne spécifie pas d’options de fenêtre, le pilote MCIAVI crée une fenêtre par défaut pour la séquence. Le pilote crée cette fenêtre de lecture pour la commande [**ouverte**](open.md) ([**MCI \_ Open**](mci-open.md)), mais elle n’affiche pas la fenêtre tant que votre application n’a pas envoyé de commande pour afficher la fenêtre ou lire le fichier. Cette fenêtre de lecture par défaut est une fenêtre indépendante avec une bordure de redimensionnement, une barre de titre, un cadre épais, un menu de **fenêtre** et un bouton réduire.

Votre application peut également spécifier un handle de fenêtre parente et un style de fenêtre lorsqu’elle émet la commande **ouvrir** . Dans ce cas, le pilote MCIAVI crée une fenêtre basée sur ces spécifications au lieu de la fenêtre contextuelle par défaut. Votre application peut spécifier n’importe quel style de fenêtre disponible pour la fonction [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) . Les styles qui requièrent une fenêtre parente, tels que WS \_ Child, doivent inclure un handle de fenêtre parente.

Votre application peut également créer sa propre fenêtre et fournir le descripteur au pilote MCIAVI à l’aide de la commande [**fenêtre**](window.md) ([**\_ fenêtre MCI**](mci-window.md)). Le pilote MCIAVI utilise cette fenêtre au lieu d’en créer un propre.

Lorsque le pilote MCIAVI crée la fenêtre de lecture ou obtient un handle de fenêtre à partir de votre application, il n’affiche pas la fenêtre tant que votre application n’a pas lu la séquence ou n’a pas envoyé de commande pour afficher la fenêtre. Votre application peut utiliser la commande **fenêtre** pour afficher la fenêtre sans exécuter la séquence. Par exemple, la commande suivante affiche la fenêtre à l’aide de [**mciSendString**](/previous-versions//dd757161(v=vs.85)):


```C++
mciSendString("window movie state show", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



Dans cet exemple, « Movie » est un alias pour le périphérique vidéo numérique.

Votre application peut également lire un fichier AVI plein écran. Pour lire en mode plein écran, modifiez la commande [**Play**](play.md) ([**\_ lecture MCI**](mci-play.md)) avec l’indicateur « fullscreen » (MCI \_ MCIAVI \_ Play \_ fullscreen). Lorsque votre application utilise cet indicateur, le pilote MCIAVI utilise un format plein écran 320 par 240 pixels pour la séquence. Par exemple, la commande suivante lit le fichier ouvert en plein écran (en utilisant « Movie » comme alias) :


```C++
mciSendString("play movie fullscreen", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



## <a name="changing-the-playback-state-for-an-avi-file"></a>Modification de l’état de lecture d’un fichier AVI

Votre application peut utiliser la commande [**Seek**](seek.md) ([**MCI \_ Seek**](mci-seek.md)) pour déplacer la position actuelle vers le début, la fin ou une position arbitraire dans un fichier avi. Il existe deux modes de recherche pour le pilote MCIAVI : exact et inexact. Votre application peut modifier le mode de recherche à l’aide de la commande [**Set**](set.md) ([**MCI \_ Set**](mci-set.md)). Quand vous utilisez **Set** « Seek exactly on », le pilote MCIAVI recherche exactement le frame que votre application spécifie. Cela peut entraîner un délai si le fichier est compressé de façon temporelle et que votre application ne spécifie pas d’image clé. Quand vous utilisez **Set** « Seek exact OFF », le pilote MCIAVI recherche le frame clé le plus proche dans un fichier compressé temporellement.

Certaines commandes MCI permettent à votre application de modifier la lecture d’un fichier AVI d’une autre manière. Par exemple, un fichier AVI, par défaut, est lu à sa vitesse normale, mais votre application peut augmenter ou diminuer cette vitesse en utilisant l’indicateur « Speed » avec la commande **Set** . Pour les fichiers AVI, une valeur de vitesse de 1000 est typique. Ainsi, pour lire un film à la moitié de sa vitesse habituelle, votre application peut utiliser le **jeu** de commandes « film Speed 500 ». une autre solution consiste à utiliser **Set** « movie Speed 2000 » pour jouer la séquence à deux fois la vitesse normale.

La commande [**SetAudio**](setaudio.md) ([**MCI \_ SetAudio**](mci-setaudio.md)) permet à votre application de contrôler la partie audio d’un fichier avi. Votre application peut désactiver le son lors de la lecture ou, dans le cas de plusieurs fichiers audio Stream, sélectionner le flux audio qui est lu.

Le pilote MCIAVI contient une boîte de dialogue qui permet de contrôler certaines de ses options de lecture. Parmi les options disponibles pour l’utilisateur, citons la sélection de la lecture de l’écran ou de la fenêtre, la sélection du mode de recherche et le zoom de l’image. Votre application peut avoir MCIAVI afficher cette boîte de dialogue à l’aide de la commande [**configurer**](configure.md) ([**MCI \_ configurer**](mci-configure.md)).

## <a name="stream-handlers"></a>Gestionnaires de flux

Les données d’un fichier AVI sont traitées comme une série de flux. Un fichier AVI contient généralement un flux audio et vidéo, et il peut également s’agir d’un flux personnalisé qui contient du texte ou d’autres données personnalisées. Le pilote MCIAVI peut utiliser différents gestionnaires pour ces flux de données. Pour plus d’informations sur les fichiers AVI personnalisés, consultez [gestionnaires de fichiers et de flux](custom-file-and-stream-handlers.md)de données personnalisés.

 

 