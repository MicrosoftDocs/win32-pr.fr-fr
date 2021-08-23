---
title: Services VCR
description: Services VCR
ms.assetid: 140220f7-df7b-46e2-8374-e1200d873f3b
keywords:
- Carte de contrôle de système vidéo (VISCA)
- VISCA (Video System Control architecture)
- Pilote MCI MCI
- Pilote VISCA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0397e56c589c357edc9e0be1999b51d358f8caced60117af5c20c7954a1edb49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804519"
---
# <a name="vcr-services"></a>Services VCR

Windows fournit des services VCR via un pilote de périphérique basé sur la commande MCI définie pour les magnétoscopes. Cette section décrit le pilote VISCA Video System Control architecture (VISCA) MCI et explique comment l’utiliser pour contrôler un magnétoscope.

Le type d’appareil *VCR* contrôle les magnétoscopes. Pour obtenir la liste des commandes MCI reconnues par les périphériques VCR, consultez [jeu de commandes VCR](vcr-command-set.md).

## <a name="the-mci-visca-driver"></a>Le pilote MCI MCI

Le pilote MCI MCI contrôle les magnétoscopes compatibles avec la fonction VISCA de Sony, tels que le VDeck CVD-1000. Le pilote VISCA contrôle le transport de bande, les tuners de canal et les canaux d’entrée et de sortie VCR.

## <a name="searching-and-positioning-with-a-vcr"></a>Recherche et positionnement avec un magnétoscope

Le pilote VISCA utilise deux méthodes pour suivre le mouvement des cassettes vidéo dans le transport de bandes VCR : les *informations de code temporel* et les *compteurs de bande*. Les informations de code temporel sont des informations de minutage qui ont été enregistrées sur la bande vidéo. La plupart des magnétoscopes autorisent l’enregistrement des codes temporels sans détruire les pistes audio et vidéo. Les compteurs de bandes estiment la quantité de cassettes vidéo qui se déplace au-delà de la tête de bande vidéo pour obtenir une position.

Les informations de code temporel et les compteurs de bande augmentent à mesure que la bande vidéo se déplace du début à la fin. En raison de sa précision, l’utilisation d’informations de code temporel pour positionner une bande vidéo est presque toujours préférable à l’utilisation de compteurs de bande.

Les indicateurs de commande MCI pour spécifier les informations de positionnement sont exprimés en tant que dépendances de temps : « format d’heure », « durée », « de », « à » et « recherche ». (En outre, la commande « position » de l' [**État**](status.md) retourne sa valeur d’heure au format d’heure actuel.)

Le pilote VISCA utilise la commande [**Set**](set.md) « Time Mode » pour sélectionner le type de positionnement à utiliser avec une bande vidéo. Lorsque le mode Time est défini sur « Timecode », les commandes « position » et « format d’heure **» de l'** **État** utilisent le code temporel sur la bande vidéo. Lorsque le mode Time est défini sur « Counter », les commandes « position » et « format d’heure » d' **État** **utilisent des compteurs** .

Une application peut définir le mode de temps sur « détecter » s’il n’est pas important qu’il y ait deux sources d’informations de position. En mode de détection, le pilote VISCA utilise des informations de code temporel pour le positionnement lorsque l’une des conditions suivantes se produit :

-   Les informations de code temporel sont présentes lors de l’ouverture du pilote.
-   Vous modifiez une bande vidéo avec la commande « capot ouvert » **définie** et les informations du code temporel sont présentes sur la bande vidéo.
-   La commande [**Set**](set.md) « Time mode » est réémise.

Si les informations de code d’horaire sont introuvables, le pilote utilise les compteurs de bande.

Pour déterminer la méthode de positionnement en cours, émettez la commande « Time type » de l' [**État**](status.md) , qui retourne soit « code temporel », soit « compteur ». Vous pouvez également identifier le mode de positionnement actuel à l’aide de la commande **Status** « Time Mode », qui retourne « code temporel », « compteur » ou « détecter ».

La commande « Counter » de l' **État** récupère la valeur actuelle du compteur de bande, quelle que soit la méthode de positionnement en cours. Toutefois, vous pouvez utiliser ce compteur en lisant uniquement avec la commande « Counter » [**définie**](set.md) .

Le pilote VISCA peut récupérer le format de code temporel natif enregistré sur une bande vidéo en utilisant les commandes d' **État** « **type de code** temporel » et « fréquence d’images » d’État ensemble. Par exemple, si le type de code temporel est « SMPTE » et que la fréquence d’images est de 25, le format du code temporel natif enregistré sur la bande vidéo est SMPTE 25.

Le pilote VISCA peut également récupérer la résolution des compteurs **à l’aide de la commande** « Counter Resolution », qui retourne « seconds » ou « frames ». Le format de compteur peut toujours être défini sur SMPTE 30, mais la valeur de retour retourne uniquement une trame de 0. Si le type d’heure actuel est Counter, cette résolution s’applique également à la valeur retournée par l' **État** « position ».

## <a name="capturing-frames"></a>Capturer des frames

Les commandes de capture de trames fournissent des images fixes pour un *appareil de capture de trames*. Un périphérique de capture de trames est un élément matériel distinct pouvant lire et stocker l’image vidéo. Le pilote VISCA prend en charge la commande [**Freeze**](freeze.md) ([**\_ blocage de MCI**](mci-freeze.md)) pour stabiliser une image continue pour la capture. En outre, vous pouvez utiliser la commande [**dégeler (libérer le mode**](unfreeze.md) [**MCI \_**](mci-unfreeze.md)) pour redémarrer le transport de bande à la suite d’une commande **Freeze** .

La commande **Freeze** fournit une image de haute qualité, stabilisée, de base temporelle, corrigée pour un appareil de capture de trames. Cette commande existe, car un appareil peut ne pas toujours fournir son image de sortie de qualité maximale pendant la lecture ou en pause ; une image vidéo de ce type n’est pas adaptée à la capture.

La commande **dégeler** déverrouille le transport de bande et reprend le mode de transport en vigueur avant la commande **Freeze** .

Lorsque votre application doit enregistrer une image vidéo sur le magnétoscope, utilisez la commande **figer** l’entrée ou la commande de [**signal**](cue.md) ([**MCI \_ )**](mci-cue.md)pour enregistrer l’image.

## <a name="selecting-inputs"></a>Sélection des entrées

Le pilote VISCA prend en charge trois types d’entrée : vidéo, audio et code temporel. Les entrées vidéo incluent deux canaux standard (lignes 1 et 2), un canal SVideo, un canal auxiliaire et un canal à partir d’un tuner interne. Les entrées audio incluent deux canaux standard (lignes 1 et 2) et un canal d’un tuner interne. L’entrée du code temporel est interne au magnétoscope.

Les sorties normales comportent les entrées actuellement sélectionnées lorsque le magnétoscope est enregistré ou lorsque le transport de bande est arrêté, et ils transportent le contenu de la bande vidéo lorsque le transport de bande est en cours de diffusion ou en pause. Les sorties analysées comportent les mêmes informations que les sorties normales, ainsi que les informations actuelles sur le code temporel et le canal.

En supposant que les entrées externes appropriées sont connectées à votre magnétoscope et que vous avez choisi ce que vous souhaitez enregistrer, vous pouvez sélectionner les entrées à enregistrer. Par exemple, pour enregistrer ou afficher à partir de la vidéo « SVIDEO » et des entrées audio « ligne 1 », vous devez utiliser les commandes [**setvideo**](setvideo.md) ([**MCI \_ setvideo**](mci-setvideo.md)) et [**SetAudio**](setaudio.md) ([**MCI \_ SetAudio**](mci-setaudio.md)) pour sélectionner ces sources d’entrée. Vous pouvez vérifier ces sélections à l’aide de la commande [**Status**](status.md) ([**\_ État MCI**](mci-status.md)).

Par défaut, le moniteur affiche exactement ce qui apparaît comme sortie. Toutefois, il peut arriver que vous souhaitiez afficher une source lors de l’enregistrement à partir d’une autre. Il s’agit d’une pratique courante utilisant le tuner. Par exemple, vous souhaiterez peut-être regarder Channel 4 pendant que vous enregistrez Channel 7. Dans ce cas, vous avez deux entrées de tuner logique. Vous pouvez configurer le magnétoscope à l’aide des commandes suivantes :

## <a name="to-review-one-source-while-recording-from-another"></a>Pour examiner une source lors de l’enregistrement à partir d’une autre

1.  Utilisez la commande [**settuner**](settuner.md) ([**MCI \_ settuner**](mci-settuner.md)) pour sélectionner les canaux à regarder et à enregistrer.
2.  Utilisez la commande **setvideo** pour sélectionner la source d’enregistrement vidéo.
3.  Utilisez la commande [**SetAudio**](setaudio.md) pour sélectionner la source d’enregistrement audio.
4.  Utilisez la commande [**setvideo**](setvideo.md) pour acheminer l’entrée vidéo de canal 4 vers la sortie surveillée afin de l’afficher à l’écran.
5.  Utilisez la commande [**SetAudio**](setaudio.md) pour acheminer l’entrée audio Channel 4 vers la sortie surveillée afin de lire l’audio.
6.  Vérifiez vos sélections à l’aide de la commande [**Status**](status.md) .

Le pilote VISCA prend également en charge un type d’entrée spécial pour l’audio et la vidéo, appelé *muet*. L’option muet permet de sélectionner « aucune entrée », ce qui est utile lors de l’enregistrement d’un signal vide.

## <a name="selecting-recording-tracks"></a>Sélection des pistes d’enregistrement

Il existe trois types de pistes d’enregistrement sur une bande vidéo : vidéo, audio et code temporel. Vous n’avez qu’une seule piste vidéo ou timecode, mais vous pouvez utiliser plusieurs pistes audio. Dans ce cas, faites suivre 1 la piste audio principale.

Le pilote VISCA prend en charge deux modes d’opération : assembler et insérer. En *mode assemblage*, toutes les pistes sont sélectionnées pour être enregistrées. En *mode insertion*, les pistes peuvent être sélectionnées indépendamment pour l’enregistrement. La plupart des magnétoscopes sont en mode assemblage par défaut. Utilisez la commande [**Set**](set.md) ([**\_ jeu de MCI**](mci-set.md)) pour modifier ces modes.

## <a name="recording-and-editing"></a>Enregistrement et modification

La commande [**Record**](record.md) ([**\_ enregistrement MCI**](mci-record.md)) fournit un enregistrement simple et est précise à environ 1 seconde de la position de départ. Pour un enregistrement plus précis ou si vous prévoyez de modifier le contenu vidéo tout en opérant simultanément sur plusieurs jeux, vous devez utiliser la commande de [**pile**](cue.md) ([**MCI \_ CUE**](mci-cue.md)).

La commande **CUE** prépare l’appareil pour l’enregistrement ou la diffusion. Utilisez la commande « Input » de la **pile** pour préparer l’appareil à l’enregistrement. La commande **CUE** est requise, car une application doit savoir quand l’appareil est prêt à exécuter la commande (et parce qu’il peut prendre plusieurs minutes pour préparer une [**lecture**](play.md) ([**\_ lecture MCI**](mci-play.md)) ou une commande d' **enregistrement** ).

Le magnétoscope se prépare à l’enregistrement ou à la diffusion en recherchant le *point d'* interrogation, qui correspond à la position actuelle ou à la position spécifiée à l’aide de la commande « from » de la **pile** . Toutefois, si l’indicateur « preroll » est spécifié à l’aide de la commande **CUE** , le magnétoscope se positionne lui-même la distance de préroll à partir du point d’interrogation. L’indicateur « préroll » indique également que le magnétoscope utilise un mode de modification applicable. il est donc important que vous utilisiez le « préroll », en particulier lorsque vous souhaitez un enregistrement plus précis. (Utilisez la commande [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) avec l’indicateur « peut préroll » pour vérifier si le mode préroll est pris en charge.)

> [!Note]  
> Lorsque vous enregistrez à l’aide de positions « from » et « to », la position « from » est incluse dans la modification et la position « to » n’est pas.

 

Pour plus d’informations sur l’enregistrement, consultez [enregistrement](recording.md).

## <a name="using-the-clock-while-editing"></a>Utilisation de l’horloge pendant la modification

Lors de la modification, vous souhaiterez peut-être enregistrer des segments d’un magnétoscope à un autre. Vous pouvez commencer l’enregistrement à une heure et à une position spécifiques sur un magnétoscope, tout en spécifiant une action (lecture ou enregistrement), une position et une heure pour chaque magnétoscope.

Les deux magnétoscopes doivent utiliser la même horloge pour ce type de modification ; l’horloge permet de synchroniser les deux appareils. Vous pouvez déterminer si deux magnétoscopes partagent la même horloge à l’aide de la commande [**Status**](status.md) ([**\_ État MCI**](mci-status.md)) avec l’indicateur « Clock ID » pour interroger chaque magnétoscope. Si les numéros d’identification retournés par la commande **Status** sont identiques, les appareils utilisent la même horloge. En tant que ressource partagée, l’horloge peut être connectée à plusieurs magnétoscopes. Le pilote VISCA ne prend en charge qu’une seule horloge partagée.

Vous pouvez également **déterminer la résolution de l’horloge** à l’aide de la commande « taux d’incréments d’horloge ». Cette commande retourne le nombre d’incréments pris en charge par seconde par l’horloge. Par exemple, si l’horloge est mise à jour toutes les millisecondes, la commande retourne 1000 comme taux d’incrément d’horloge. L’avantage de l’utilisation de la vitesse d’incrémentation est que le taux est exprimé sous la forme d’un entier. dans le cas contraire, l’incrément est une valeur à virgule flottante (simple ou double précision). En tant qu’entier, la manipulation du taux d’incrément est une opération simple et n’est pas susceptible d’arrondir les erreurs. Vous pouvez réinitialiser l’horloge à l’aide de la commande [**Set**](set.md) ([**MCI \_ Set**](mci-set.md)) avec l’indicateur « Clock 0 » (zéro).

Lorsque vous émettez une commande [**Play**](play.md) ([**\_ lecture MCI**](mci-play.md)), [**Record**](record.md) ([**\_ enregistrement MCI**](mci-record.md)) ou [**Seek**](seek.md) ([**MCI \_ Seek**](mci-seek.md)), vous pouvez spécifier à quel moment la commande doit être exécutée. Les caractéristiques des magnétoscopes utilisés déterminent à quel moment démarrer chaque magnétoscope. Le minutage doit tenir compte de la quantité de préroll requise par chaque appareil et de la durée nécessaire à l’exécution des commandes MCI utilisées pour configurer la session d’édition. Pour ce faire, récupérez l’heure de l’horloge et ajoutez un intervalle d’attente de 5 à 10 secondes. (L’intervalle d’attente doit être suffisamment long pour permettre au préroll et aux commandes MCI en suspens de terminer l’exécution.)

Pour vous assurer que la période d’attente est suffisamment longue, placez la commande d' **enregistrement** en dernier dans votre application et vérifiez l’heure immédiatement avant celle-ci. Si l’intervalle est trop faible, redémarrez la commande de **lecture** . Vous pouvez également vérifier l’heure juste après la dernière commande du script afin de vérifier qu’il y a suffisamment de temps pour envoyer et terminer toutes les commandes.

 

 




