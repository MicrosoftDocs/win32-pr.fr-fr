---
description: À propos des codecs Windows Media
ms.assetid: C0B0265C-AD20-433B-A554-112AEB0208B9
title: À propos des codecs Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2240176de22682451814609abc94f33a52300563
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104211240"
---
# <a name="about-the-windows-media-codecs"></a>À propos des codecs Windows Media

-   [Codecs de Windows Media Audio](#windows-media-audio-codecs)
    -   [Windows Media Audio 9](#windows-media-audio-9)
    -   [Windows Media Audio 10 professionnel](#windows-media-audio-10-professional)
    -   [Windows Media Audio 9 sans perte](#windows-media-audio-9-lossless)
    -   [Voix Windows Media Audio 9](#windows-media-audio-9-voice)
    -   [Compatibilité](#compatibility)
-   [Codecs de la série Windows Media Video 9](#windows-media-video-9-series-codecs)
    -   [Windows Media Video 9](#windows-media-video-9-series-codecs)
    -   [Écran Windows Media Video 9](#windows-media-video-9-screen)
    -   [Image Windows Media Video 9 version 2](#windows-media-video-9-image-version-2)
    -   [VCM Windows Media Video 9](#windows-media-video-9-vcm)
    -   [Compatibilité](#compatibility)
-   [Rubriques connexes](#related-topics)

## <a name="windows-media-audio-codecs"></a>Codecs de Windows Media Audio

### <a name="windows-media-audio-9"></a>Windows Media Audio 9

Ce codec échantillonne l’audio à 44,1 ou 48 kilohertz (kHz) à l’aide de 16 bits, similaire à la norme CD actuelle, offrant une qualité de CD à des débits de données allant de 64 à 192 kilobits par seconde (Kbits/s). La qualité du son obtenue est de 20% meilleure que l’échantillonnage audio, avec Windows Media Audio 8, à des débits de données équivalents.

Le codec Windows Media Audio 9 (WMA 9) prend en charge le chiffrement à vitesse de transmission variable (VBR), ce qui permet une qualité audio encore supérieure aux tailles de fichier plus petites en faisant automatiquement varier la vitesse de transmission en fonction de la complexité des données audio. Avec VBR, le taux de bits de codage augmente pour capturer des sections de données complexes, puis diminue pour maximiser la compression des sections moins complexes, ce qui produit une compression compacte et de haute qualité.

WMA 9 offre une compatibilité descendante avec les décodeurs précédents compatibles Windows Media Audio, ce qui signifie que le contenu WMA 9 peut être lu avec les versions précédentes du lecteur Windows Media ou des appareils électroniques grand public plus anciens qui prennent en charge Windows Media. Comme avec tous les codecs Windows Media 9 Series, il prend en charge la plateforme de gestion des droits numériques Windows Media, qui est utilisée pour empaqueter et distribuer en toute sécurité des médias numériques protégés contre la copie.

### <a name="windows-media-audio-10-professional"></a>Windows Media Audio 10 professionnel

Windows Media Audio 10 Professional (WMA 10 Pro) est le codec audio Windows Media le plus flexible disponible. il prend en charge les profils qui incluent tout ce qui se passe du son audio 24 bits/96 kHz en stéréo, le canal 5,1, ou même le son de 7,1 canaux, à des capacités mobiles très performantes, passant de 24 Kbits/s à 96 Kbit/s pour 256 128 stéréo WMA 10 Pro offre une qualité incroyable aux consommateurs utilisant un matériel haute fidélité et des ordinateurs équipés de son surround 5,1 Channel, et pour les consommateurs qui lisent du contenu audio sur leurs appareils mobiles. WMA 10 Pro prend en charge la diffusion en continu, le téléchargement progressif ou la livraison de téléchargement et de lecture à 128 à 768 Kbps.

Lorsque vous utilisez un son audio surround 5,1 compressé à 384 kbps avec WMA 10 Pro, la plupart des écouteurs ne peuvent pas discerner les différences entre la musique compressée et les fichiers PCM (Pulse Code Modulation) d’origine. WMA Pro offre également un contrôle de plage dynamique à l’aide des amplitudes audio maximales et moyennes calculées au cours du processus d’encodage. À l’aide de la fonctionnalité de mode silencieux dans le lecteur Windows Media 9 et versions ultérieures, les utilisateurs peuvent écouter la plage dynamique complète, une plage de différence moyenne jusqu’à 12 décibels (dB) au-dessus de la moyenne, ou un petit nombre de différences jusqu’à 6 dB au-dessus de la moyenne.

Si un utilisateur tente de lire un fichier encodé à l’aide du canal 5,1, les capacités d’échantillonnage 24 bits, 96 kHz, mais ne disposent pas d’une carte système ou audio qui prend en charge les sons multicanaux ou haute résolution, plusieurs canaux sont combinés en audio stéréo (par exemple, un canal audio de 16 bits), ce qui garantit que les utilisateurs bénéficient de la meilleure expérience de lecture que leurs systèmes peuvent fournir.

Le tableau suivant compare WMA Pro à la technologie de compression concurrente.



| Données audio              | Compression du secteur\*        | Windows Media\*            | Économies de compression |
|-------------------------|-------------------------------|----------------------------|---------------------|
| 2 ch x 48 kHz x 16 bits | Dolby Digital 2,0 à 220 kbps | WMA 10 Pro à 128 Kbits/s     | 1.7:1               |
| 6 CH x 48 kHz x 20 bits | Dolby Digital 5,1 à 384 kbps | WMA 10 Pro à 192 – 256 kbits/s | 1.5 – 2:1             |
| 6 CH x 48 kHz x 24 bits | DTS 5,1 à 1 536 Kbps         | WMA 10 Pro à 768 Kbits/s     | 2:1                 |



 

\* Dépend du contenu

### <a name="windows-media-audio-9-lossless"></a>Windows Media Audio 9 sans perte

La qualité audio du contenu compressé à l’aide de ce codec est la meilleure solution pour tous les Windows Media Audio codecs. Il crée un doublon bit pour bit du fichier audio d’origine afin qu’aucune donnée ne soit perdue, ce qui en fait l’outil idéal pour l’archivage des maîtres de contenu.

En fonction de la complexité de l’original, le contenu sera compressé à un ratio 2:1 ou 3:1. Bien qu’il soit inférieur au ratio atteint avec les autres codecs de la série Windows Media Audio 9, il offre les mêmes avantages que la compression tout en laissant intactes les données.

Comme Windows Media Audio 9 professionnel, le codec Windows Media Audio 9 Lossless offre également un contrôle de plage dynamique à l’aide des amplitudes audio maximales et moyennes calculées au cours du processus d’encodage. À l’aide de la fonctionnalité mode silencieux dans le lecteur Windows Media 9 et versions ultérieures, les utilisateurs peuvent écouter la plage dynamique complète, une plage de différence moyenne jusqu’à 12 dB au-dessus de la moyenne, ou une petite plage de valeurs jusqu’à 6 dB au-dessus de la moyenne.

### <a name="windows-media-audio-9-voice"></a>Voix Windows Media Audio 9

Ce codec à faible débit est principalement destiné au contenu vocal, mais fonctionne très bien avec le contenu en mode mixte qui comprend à la fois la voix et la musique. En mode vocal, le codec tire parti de la plage de fréquences moins compliquée et plus étroite de la voix humaine pour maximiser la compression. En mode musique, le codec fonctionne comme le codec standard Windows Media Audio 9. Le contenu encodé peut être configuré pour basculer automatiquement entre les modes vocal et musical.

Le codec vocal Windows Media Audio 9 offre une qualité supérieure pour les scénarios de diffusion en continu à faible débit (moins de 20 Kbits/s), tels que les diffusions radioélectriques, la publicité, les livres électroniques, les podcasts et voiceovers. Le codec vocal peut également compresser le contenu sur un minimum de 4 kbit/s à 8 kHz.

### <a name="compatibility"></a>Compatibilité

Le tableau suivant décrit ce que votre public rencontrera lors de la lecture de contenu Windows Media Audio série 9 sur les systèmes d’exploitation Microsoft Windows antérieurs à Windows XP ou avec les versions antérieures du lecteur Windows Media. Ce tableau répertorie également la compatibilité pour les plateformes Apple Mac OS X et basées sur Windows CE.



| Codec                              | Fonctionnalité                                       | Compatibilité descendante du lecteur                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Audio 9              | Encodage à débit binaire constant (CBR)              | <dl> <dt>Lecteur Windows Media 6,4 ou version ultérieure sur les appareils non portables (à l’aide du transcodage en fonction des besoins)</dt> <dt>lecteur Windows Media 9 pour Mac OS X</dt> <dt>Windows Media Player 9 et Windows \* Media Player 9,1 pour Pocket PC</dt> <dt>Windows Media Player 9 et Windows \* Media Player 9,1 pour smartphone</dt> </dl> |
|                                    | Encodage VBR (variable-bit-rate)              | Windows Media Player 7 ou version ultérieure sur tous les appareils qui prennent en charge le lecteur (en utilisant le transcodage si nécessaire)                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Media Audio 9 professionnel | Général                                       | <dl> <dt>Windows Media Player 7 ou version ultérieure</dt> <dt>Windows Media player 9 pour Mac OS X</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | Lecture de canal discrète (par exemple, 5,1) | Requiert Windows Media Player 9 (ou SDK) ou version ultérieure, Windows XP et une carte audio multicanal.                                                                                                                                                                                                                                                                                                                                                                                                                         |
|                                    | Haute résolution audio (24 bits, 96 kHz)        | Requiert Windows Media Player 9 (ou SDK) ou version ultérieure, Windows XP et une carte audio haute résolution.                                                                                                                                                                                                                                                                                                                                                                                                                      |
|                                    | Contrôle de plage dynamique                         | Requiert Windows Media Player 9 (ou SDK) ou version ultérieure et Windows XP.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Windows Media Audio 9 sans perte     | Général                                       | <dl> <dt>Windows Media Player 7 ou version ultérieure</dt> <dt>Windows Media player 9 pour Mac OS X</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | Lecture de canal discrète (par exemple, 5,1) | Requiert Windows Media Player 9 (ou SDK) ou version ultérieure, Windows XP et une carte audio multicanal.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Voix Windows Media Audio 9        | Général                                       | <dl> Lecteur Windows Media <dt>6,4 ou version ultérieure</dt> <dt>Windows Media Player 9 pour Mac OS X</dt> <dt>Windows Media Player 9 et Windows Media Player 9,1 pour Pocket PC \* </dt> <dt>Windows Media Player 9 et Windows Media Player 9,1 pour smartphone \* </dt> </dl>                                                       |



 

> [!Note]  
> \* Toutes les versions de Windows Media Player pour Pocket PC et Smartphone sont fournies dans le cadre du système d’exploitation Microsoft Windows Mobile. Le lecteur Windows Media pour Pocket PC et le lecteur Windows Media pour Smartphone ne peuvent pas être téléchargés à partir de Microsoft.

 

## <a name="windows-media-video-9-series-codecs"></a>Codecs de la série Windows Media Video 9

En 2006, la société of Motion image and Television Engineers (SMPTE) publiait officiellement la spécification finale pour SMPTE 421M, également appelée VC-1. La normalisation formelle de VC-1 représente l’aboutissement d’années de surveillance technique par plus de 75 entreprises, conduisant à un codec bien documenté, extrêmement stable, facilement concédant à des licences et accepté par le secteur. VC-1 prend en charge trois profils : simple, principal et avancé. Les profils simples et principaux ont été exécutés depuis plusieurs années, et les implémentations existantes telles que WMV 9 ont longtemps pris en charge la création et la lecture de contenu à l’aide de ces profils, ainsi qu’une implémentation précoce du profil avancé. L’achèvement du profil avancé et de la standardisation de tous les profils dans VC-1 représente la dernière étape d’une spécification complète qui fournit du contenu haute définition (entrelacé ou progressif) sur tous les supports et tous les appareils compatibles.

### <a name="windows-media-video-9"></a>Windows Media Video 9

Windows Media Video 9 est l’implémentation Microsoft de la norme SMPTE VC-1. Il prend en charge des profils simples, principaux et avancés.

### <a name="simple-and-main-profiles"></a>Profils simples et principaux

Les profils simples et principaux de Windows Media Video 9 sont entièrement conformes à la norme SMPTE VC-1 et fournissent une vidéo de haute qualité pour la diffusion et le téléchargement. Ces profils prennent en charge un large éventail de vitesses de transmission, du contenu de haute définition à un demi jusqu’à un tiers de la vitesse de transmission de MPEG-2, à une vidéo Internet à faible débit fournie sur un modem d’accès à distance. Ce codec prend également en charge la vidéo téléchargeable de qualité professionnelle avec un encodage à deux passes et une vitesse de transmission variable (VBR). Windows Media Video 9 est déjà pris en charge par un large éventail de lecteurs et de périphériques.

### <a name="advanced-profile"></a>Profil avancé

Le profil avancé Windows Media Video 9 est entièrement conforme à la norme SMPTE VC-1, prend en charge le contenu entrelacé et est indépendant du transport. Les créateurs de contenu peuvent utiliser ce profil pour distribuer du contenu progressif ou entrelacé à des débits de données aussi bas qu’un tiers du codec MPEG-2, avec la même qualité que MPEG-2.

Dans le passé, le contenu vidéo entrelacé était toujours déentrelacé avant l’encodage avec le codec Windows Media Video. Désormais, l’encodage d’applications telles que Windows Media 9 Series et des solutions d’encodage tierces peut prendre en charge la compression de contenu entrelacé sans la convertir au contenu progressif. La conservation de l’entrelacement dans un fichier encodé est importante si le contenu est toujours rendu sur un écran entrelacé, tel qu’une télévision.

L’indépendance du transport permet également la distribution de Windows Media Video 9 profils avancés sur des systèmes qui ne sont pas basés sur Windows Media, tels que des infrastructures de diffusion basées sur des normes (par le biais de flux de transport MPEG-2 natifs), des infrastructures sans fil (à l’aide du protocole de transfert en temps réel \[ \] ), voire des DVD.

Le tableau suivant compare Windows Media Video 9 Advanced Profile à la technologie de compression concurrente.



| Données vidéo                                                  | Compression du secteur\* | Windows Media\*                                      | Économies de compression |
|-------------------------------------------------------------|------------------------|------------------------------------------------------|---------------------|
| 480/24p 720 x 480 pixels/image x 8 bits par canal x 24 fps  | MPEG-2 à 4 – 6 Mbits/s     | Profil avancé Windows Media Video 9 à 1,3 – 2 Mbits/s | 3                 |
| 480/30i 720 x 480 pixels/image x 8 bits par canal x 30 i/s  | MPEG-2 à 6 – 8 Mbits/s     | Profil avancé Windows Media Video 9 à 2 – 4 Mbits/s   | 2 – 3:1               |
| 720/24p 1280 x 720 pixels/image x 8 bits par canal x 24 fps | MPEG-2 à 19 Mbits/s      | Profil avancé Windows Media Video 9 à 5 – 8 Mbits/s   | 2.4 – 3.8:1           |



 

\*Dépend du contenu

### <a name="windows-media-video-9-screen"></a>Écran Windows Media Video 9

Le codec d’écran Windows Media Video 9 est optimisé pour compresser des captures d’écran séquentielles et des vidéos hautement statiques capturées à partir de l’affichage de l’ordinateur, ce qui en fait la solution idéale pour la diffusion de démonstrations ou la démonstration de l’utilisation des ordinateurs pour l’apprentissage. Le codec tire parti de la simplicité d’image classique et de l’absence de mouvement relative pour obtenir un taux de compression très élevé.

Pendant le processus d’encodage, le codec bascule automatiquement entre les modes d’encodage avec perte et sans perte, en fonction de la complexité des données vidéo. Pour les données complexes, le mode sans perte conserve une copie exacte des données. Pour les données moins complexes, le mode de perte ignore certaines données pour obtenir un taux de compression plus élevé. En basculant automatiquement entre ces deux modes, le codec conserve la qualité vidéo tout en maximisant la compression.

Globalement, le codec d’écran Windows Media Video 9 offre une meilleure gestion des images bitmap et des mouvements d’écran, même sur des processeurs relativement modestes. Il est également jusqu’à 100 fois plus efficace que l’encodage de longueur d’exécution couramment utilisé.

### <a name="windows-media-video-9-image-version-2"></a>Image Windows Media Video 9 version 2

Le codec d’image Windows Media Video 9 version 2 diffère des autres codecs vidéo. Au lieu de traiter une vidéo non compressée, elle transforme les images fixes en vidéo en utilisant des transitions de panoramique, de zoom et de fondu croisé entre les éléments pour créer un nombre illimité d’effets.

Les résultats peuvent ensuite être remis à des débits de données inférieurs à 20 kilobits par seconde (Kbits/s). Ces fichiers sont compressés à l’aide des modes vitesse binaire constante (CBR) ou vitesse de transmission variable à un passage (VBR).

> [!Note]  
> Le codec d’image Windows Media Video 9 version 2 n’est pas compatible avec le codec d’image Windows Media Video 9.

 

### <a name="windows-media-video-9-vcm"></a>VCM Windows Media Video 9

La version de la VCM (Video Compression Manager) du codec de la série Windows Media Video 9 permet aux versions antérieures de l’encodage et de la modification d’applications de prendre en charge le codec de la série Windows Media Video 9 dans des conteneurs de fichiers tels que Audio Video entrelacé (AVI). Ce package de codec permet également aux fichiers Windows Media Video (WMV) basés sur le format Windows Media 9 d’être lus dans le lecteur Windows Media 6,4, à la fois dans les conteneurs de fichiers ASF et AVI.

### <a name="compatibility"></a>Compatibilité

Le tableau suivant décrit ce que votre public rencontrera lors de la lecture de contenu Windows Media Video série 9 sur des systèmes d’exploitation Microsoft Windows antérieurs ou avec des versions antérieures du lecteur Windows Media. Ce tableau répertorie également la compatibilité pour les plateformes Apple Mac OS X et basées sur Windows CE.



| Codec                                  | Fonctionnalité             | Compatibilité descendante du lecteur                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Video 9                  | Général             | <dl> Lecteur Windows Media <dt>6,4 ou version ultérieure</dt> <dt>Windows Media Player 9 pour Mac OS X</dt> <dt>Windows Media Player 9 et Windows Media Player 9,1 pour Pocket PC \* </dt> <dt>Windows Media Player 9 et Windows Media Player 9,1 pour smartphone \* </dt> </dl> |
|                                        | Interpolation de frame | Requiert Windows Media Player 9 (ou kit de développement logiciel) ou version ultérieure et Windows XP.                                                                                                                                                                                                                                                                                                                                                                           |
| Profil avancé Windows Media Video 9 | Général             | Lecteur Windows Media 7 ou version ultérieure                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Écran Windows Media Video 9           | Général             | Lecteur Windows Media 7 ou version ultérieure                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Image Windows Media Video 9 version 2  | Général             | Lecteur Windows Media 7 ou version ultérieure                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

> [!Note]  
> \*Toutes les versions de Windows Media Player pour Pocket PC et Smartphone sont fournies dans le cadre du système d’exploitation Microsoft Windows Mobile. Le lecteur Windows Media pour Pocket PC et le lecteur Windows Media pour Smartphone ne peuvent pas être téléchargés à partir de Microsoft.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codecs Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



