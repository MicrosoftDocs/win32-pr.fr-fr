---
description: Guide du développeur pour la version redistribuable de XAudio 2.9
ms.assetid: ''
title: Guide du développeur pour la version redistribuable de XAudio 2.9
ms.topic: article
ms.date: 10/17/2019
ms.openlocfilehash: a73ebd01d599446dc96e1e6735d8af572203a23b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262591"
---
# <a name="developer-guide-for-redistributable-version-of-xaudio-29"></a>Guide du développeur pour la version redistribuable de XAudio 2.9

Une version de XAudio 2,9 est disponible sous forme de [package NuGet](/nuget/what-is-nuget). Les développeurs peuvent redistribuer cette version de XAudio 2,9 avec leurs applications. Cela permet à une application d’utiliser XAudio 2,9 sur des versions antérieures de Windows qui n’incluent pas XAudio 2,9 dans le cadre de l’image du système d’exploitation. L’utilisation de ce package redistribuable est préférable à la redistribution de XAudio 2,7 à partir du kit de développement logiciel (SDK) DirectX, car XAudio 2,7 n’a pas été mis à jour depuis 2010.

Veillez à consulter la [page d’accueil de DirectX](https://devblogs.microsoft.com/directx/landing-page/) pour obtenir d’autres ressources pour les développeurs DirectX.

## <a name="supported-platforms"></a>Plateformes prises en charge

Le package NuGet XAudio 2,9 (*Microsoft. XAudio2. Redist. \* . nupkg*) comprend une version 32 bits et une version 64 bits d’une dll qui implémente l’API XAudio 2,9. La DLL est appelée XAUDIO2 \_9REDIST.DLL. Cette DLL fonctionnera sur Windows 7 SP1, Windows 8, Windows 8.1 et Windows 10.

Lorsque la DLL est utilisée sur un système Windows 10, elle vérifie le numéro de version de la \_9.DLL XAUDIO2 qui fait partie du système d’exploitation, et si le système d’exploitation est plus récent, elle délègue tous les appels d’API à XAUDIO2 \_9.DLL dans le système d’exploitation. Cela garantit que les applications utilisent toujours la dernière version de XAudio 2,9 qui est disponible sur la plateforme actuelle.

La DLL n’est pas destinée à Xbox One. S’il est utilisé sur Xbox 1, la DLL délègue toujours tous les appels d’API à XAUDIO2 \_9.DLL dans le système d’exploitation Xbox One.

La DLL n’est pas destinée aux applications UWP. Les applications UWP doivent utiliser le \_9.DLL XAUDIO2 qui fait partie du système d’exploitation.

## <a name="installing-the-nuget-package"></a>Installation du package Nuget

Le moyen le plus simple d’installer le package NuGet consiste à utiliser le [Gestionnaire de package NuGet](/nuget/consume-packages/install-use-packages-visual-studio) dans Microsoft Visual Studio. Dans ce cas, votre fichier projet Visual Studio est automatiquement mis à jour pour inclure *Microsoft. XAudio2. Redist. targets*. Le fichier *. targets* ajoute le dossier include avec les fichiers d’en-tête pour le XAudio2 à votre collection de chemins d’accès Include de projet. Le fichier *. targets* rend également votre .DLL ou .EXE lier avec XAUDIO2REDIST. LIB et XAPOBASEREDIST. LIB.

Bibliothèque XAPOBASEREDIST. LIB n’est nécessaire que si vous envisagez de impement un objet de traitement XAudio personnalisé (XAPO) et vous pouvez le supprimer de *Microsoft. XAudio2. Redist. targets* s’il n’est pas utilisé.

Vous pouvez également utiliser d’autres outils pour extraire le contenu du package NuGet, ou même renommer l’extension de fichier pour .zip et extraire les fichiers avec n’importe quel outil ZIP Extractor.

> Un port est également ``xaudio2redist`` disponible pour le [Gestionnaire de Package VC + +](https://github.com/microsoft/vcpkg).

## <a name="compiling-your-app"></a>Compilation de votre application

### <a name="choosing-which-headers-to-include"></a>Choix des en-têtes à inclure

Le package NuGet XAudio 2,9 inclut les mêmes fichiers d’en-tête XAudio2 que ceux inclus dans le kit de développement logiciel (SDK) Windows 10. Toutefois, les fichiers d’en-tête ont subi des ajustements pour s’assurer que vous pouvez les utiliser tout en ciblant explicitement toutes les [plateformes prises en charge](#supported-platforms), y compris les versions antérieures de Windows.

Si vous [Installez le package NuGet](#installing-the-nuget-package) à l’aide du gestionnaire de package nuget dans Microsoft Visual Studio, le chemin d’accès aux fichiers d’en-tête est placé devant le chemin d’accès aux fichiers d’en-tête SDK Windows. Cela signifie que si le code de votre projet comprend XAUDIO2. En-tête H, il récupère l’en-tête multiplateforme du package NuGet. Il s’agit normalement du comportement souhaité.

Vous devez être prudent si vous ajoutez manuellement le chemin d’accès aux en-têtes include dans le projet, comme si vous les spécifiez dans le mauvais ordre, vous risquez d’avoir des XAUDIO2 spécifiques à la version du système d’exploitation [. H](/windows/win32/api/xaudio2/) à inclure à partir de la SDK Windows, plutôt que la version multiplateforme de XAUDIO2. H.

Pour que l’inclusion des en-têtes soit moins sujette aux erreurs, le package NuGet contient une version de chaque en-tête avec « Redist » ajouté. Par exemple, en plus de XAUDIO2. H, le package NuGet comprend également XAUDIO2REDIST. H. Si vous préférez, votre code peut inclure directement XAUDIO2REDIST. H pour éliminer toute ambiguïté relative au fichier d’en-tête utilisé. Lors de l’inclusion du Redist. Version H d’un fichier d’en-tête, l’ordre dans lequel les répertoires de fichiers include sont répertoriés dans le fichier projet n’a pas d’importance.

Notez que si votre application est également en cours de compilation pour Xbox One, vous devez continuer à inclure XAUDIO2. H lors de la compilation pour Xbox One, comme certaines API de Xbox One spécifiques sont exclues de XAUDIO2REDIST. H. Ce package NuGet n’est pas destiné à Xbox One.

### <a name="loading-the-dll"></a>Chargement de la DLL

Nous vous recommandons de lier votre application à XAUDIO2REDIST. LIB et installent XAUDIO2 \_9REDIST.DLL dans le même dossier que le fichier exécutable de votre application. Cela entraîne le \_ chargement de XAUDIO29REDIST.DLL dès le lancement de votre fichier exécutable. Toutefois, si vous préférez, vous pouvez utiliser [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw) et [**GETPROCADDRESS**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour charger XAUDIO2 \_9REDIST.DLL à la demande. Il s’agit d’une bonne solution si votre application n’a pas toujours besoin d’utiliser les API XAudio2. Toutefois, si vous procédez ainsi, vous devez garder le XAUDIO2 \_9REDIST.DLL chargé jusqu’à ce que l’application se termine, car la tentative de déchargement de la dll peut provoquer un blocage si un thread d’arrière-plan exécute toujours du code dans la dll.

Contrairement à l’ancien XAudio 2,7, il n’est pas possible d’utiliser CoCreateInstance pour charger la DLL.

### <a name="verifying-the-dll-signature"></a>Vérification de la signature de la DLL

Le XAUDIO2 \_9REDIST.DLL binaire est signé par Microsoft à l’aide d’une signature SHA-2. Tout code qui tente de valider la signature, par exemple, les modules anti-triche pour les jeux, doit donc prendre en charge SHA-2. Notez que Windows 7 SP1 n’a pas pris en charge SHA-2 à l’origine et requiert une mise à jour pour ajouter cette fonctionnalité. La mise à jour est disponible en tant que [KB4474419](https://support.microsoft.com/help/4474419/sha-2-code-signing-support-update).

## <a name="testing"></a>Test

### <a name="spatial-sound-in-newer-versions-of-windows-10"></a>Son spatial dans les versions plus récentes de Windows 10

À compter de la mise à jour Windows 10 1903, XAudio 2,9 utilise automatiquement le [son Surround virtuel](#spatial-sound-and-virtual-surround), si certaines conditions sont satisfaites. Nous vous recommandons de tester les jeux qui génèrent du son multicanal sur Windows 10 1903 (ou une version ultérieure) pour vérifier que le jeu semble comme prévu.

#### <a name="enabling-spatial-sound"></a>Activation du son spatial

L’utilisateur peut activer un format de son spatial en cliquant avec le bouton droit sur l’icône de haut-parleur dans la barre d’état système Windows. 

XAudio 2,9 utilise uniquement le format de son spatial sélectionné si le processus qui utilise l’API XAudio2 est reconnu en tant que jeu par la barre de jeux Windows. Pendant le développement, il est possible que le processus ne soit pas encore reconnu en tant que jeu par la barre de jeux. Pour modifier cette valeur, utilisez le raccourci clavier Win + G pour afficher la barre de jeux pendant que le jeu est en cours d’exécution. Cliquez ensuite sur l’icône « Paramètres », puis cochez la case « n’oubliez pas qu’il s’agit d’un jeu ».

#### <a name="opting-out-from-spatial-sound"></a>Désactivation du son spatial

Il existe un moyen de refuser à XAudio2 d’utiliser l’encodeur de son spatial en spécifiant certaines valeurs pour le paramètre [**AUDIO_STREAM_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) dans [**IXAudio2 :: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice). 

Le son spatial est activé pour les catégories suivantes :

* AudioCategory_ForegroundOnlyMedia
* AudioCategory_GameEffects
* AudioCategory_GameMedia
* AudioCategory_Movie
* AudioCategory_Media

Le son spatial n’est pas activé si l’une des catégories suivantes est spécifiée :

* AudioCategory_Other
* AudioCategory_Communications
* AudioCategory_Alerts
* AudioCategory_SoundEffects
* AudioCategory_GameChat
* AudioCategory_Speech

### <a name="error-handling"></a>Gestion des erreurs

Il est important de vérifier que le jeu peut traiter une modification du périphérique audio, par exemple lorsque les écouteurs sont branchés ou débranchés. Ce test doit être testé avec un casque qui prend uniquement en charge le taux d’échantillonnage de 44,1 kHz. De nombreux casques et casques USB de bas de gamme prennent uniquement en charge 44,1 kHz. La transition entre le taux d’échantillonnage de 48 kHz et le taux d’échantillonnage de 44,1 kHz peut provoquer une erreur même lorsque la fonctionnalité de [point de terminaison audio virtuel](#virtual-audio-endpoint) est utilisée. L’erreur ne se produira pas si le casque prend également en charge 48 kHz. Notez que la fonctionnalité de point de terminaison audio virtuel n’est pas disponible sur Windows 7 SP1.

Le code d’erreur retourné par XAudio 2,9 lorsqu’il ne peut pas récupérer automatiquement à partir d’une modification du point de terminaison audio est le [ \_ périphérique XAUDIO2 E \_ \_ invalidée](xaudio2-error-codes.md). Toutefois, nous recommandons que les applications ne codent pas de façon irréversible une dépendance sur le code d’erreur ayant une valeur spécifique.

Pour être informé de l’erreur, l’application doit implémenter l’interface [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) et fournir un pointeur vers cette interface en appelant la méthode [**IXAudio2 :: RegisterForCallbacks**](xaudio2-callbacks.md) . L’implémentation de l’application de [**IXAudio2EngineCallback :: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) sera appelée par l’API XAudio2 si une erreur se produit pendant la lecture.

Notez que [**IXAudio2EngineCallback :: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) n’est pas nécessairement appelé si le pipeline audio est suspendu. Par exemple, si l’utilisateur minimise l’application ou si l’application est interrompue pour une raison quelconque, la lecture audio peut être suspendue. Si la modification du périphérique audio se produit pendant cette période, l’erreur est renvoyée uniquement quand l’application appelle [**IXAudio2 :: StartEngine**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-startengine) et/ou appelle [**IXAudio2SourceVoice :: Start**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start). Si la lecture peut être interrompue avec votre application, vous devez tester la modification du périphérique audio pendant que la lecture est suspendue, afin de vérifier que l’application peut toujours effectuer une récupération à partir de cette situation.

## <a name="xaudio-29-api-differences-compared-to-xaudio-27"></a>Différences de l’API XAudio 2,9 par rapport à XAudio 2,7

Cette section fournit un résumé de certaines des différences d’API entre XAudio 2,7 et la version redistribuable de XAudio 2,9.

### <a name="supported-formats"></a>Formats pris en charge

XAudio 2,9 prend en charge ces formats d’entrée sur le PC :

* PCM 16 bits linéaire
* PCM linéaire 32 bits
* ADPCM 16 bits
* xWMA

Le format XMA est pris en charge uniquement sur Xbox One.

### <a name="preferred-cpu-core"></a>Noyau de processeur préféré

Il est possible de spécifier le noyau de processeur XAudio 2,9 à utiliser pour son thread de traitement audio. Toutefois, il est généralement préférable de laisser XAudio 2,9 choisir cette valeur seule. Pour ce faire, définissez le paramètre **XAudio2Processor** dans l’appel à [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) sur XAUDIO2 \_ utiliser \_ le \_ processeur par défaut. 

XAudio 2,9 choisit un cœur de processeur différent sur le Xbox d’un ordinateur. La méthode IXAudio2Extension :: GetProcessor peut être utilisée pour déterminer le cœur de processeur XAudio2 choisi.

### <a name="virtual-audio-endpoint"></a>Point de terminaison audio virtuel

XAudio 2,9 utilise un point de terminaison audio virtuel par défaut lorsqu’il s’exécute sur Windows 8 ou version ultérieure. Cela signifie que si le point de terminaison audio par défaut change alors que XAudio 2,9 est utilisé, il tentera de basculer automatiquement vers le nouveau point de terminaison audio. C’est le cas, par exemple, lorsque le point de terminaison audio par défaut est une paire de casques connectés sur USB, puis que l’utilisateur déconnecte le casque. Les intervenants sont alors le nouveau point de terminaison audio par défaut.

Si l’application spécifie un format audio spécifique lors de l’appel de [**IXAudio2 :: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice), il est possible que xaudio 2,9 exécute ce commutateur. Par exemple, si l’application a spécifié que la voix de mastérisation utilise un taux d’échantillonnage de 48 kHz et que le nouveau périphérique audio ne prend en charge que 44,1 kHz, le commutateur automatique échoue et XAudio 2,9 signale l’erreur d' [ \_ \_ \_ invalidation de l’appareil XAUDIO2 E](xaudio2-error-codes.md) .

L’application peut refuser l’utilisation du point de terminaison audio virtuel en passant l’indicateur [**XAUDIO2 \_ aucun \_ \_ \_ client audio virtuel**](xaudio2-boundary-values-and-flags.md) à [**IXAudio2 :: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

Les points de terminaison audio virtuels ne sont pas disponibles sur Windows 7 SP1. L' **indicateur \_ XAUDIO2 \_ aucun \_ \_ client audio virtuel** n’a aucun effet sur Windows 7 SP1.

### <a name="audio-categories"></a>Catégories audio

L’application doit spécifier une catégorie pour son flux audio. Pour ce faire, vous fournissez une valeur de l’énumération AudioCategory lors de l’appel de la méthode [**IXAudio2 :: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) . Par exemple, AudioCategory_GameEffects. La catégorie audio peut affecter la façon dont Windows traite le son ou la manière dont il représente le flux audio dans le panneau de contrôle du volume. La catégorie audio affecte également si le [son Surround virtuel](#spatial-sound-and-virtual-surround) est automatiquement activé.

### <a name="duration-of-audio-processing-quantum"></a>Durée du quantum de traitement audio

Sur la plupart des PC, XAudio 2,9 traite les données audio en segments de 10 millisecondes. C’est ce que l’on appelle le quantum de traitement. Toutefois, la durée de ce Quantum peut être différente de 10 millisecondes sur un matériel. Les applications qui doivent connaître le quantum exact peuvent appeler la méthode IXAudio2Extension :: GetProcessingQuantum pour récupérer la valeur.

### <a name="spatial-sound-and-virtual-surround"></a>Son spatial et son Surround virtuel

À compter de la mise à jour Windows 10 1903, XAudio 2,9 utilise automatiquement le son Surround virtuel, si certaines conditions sont satisfaites. Nous vous recommandons de tester les jeux qui génèrent du son multicanal sur Windows 10 1903 (ou une version ultérieure) pour vérifier que le jeu semble comme prévu. Pour plus d’informations sur la façon de tester cette fonctionnalité, consultez la section [test du son spatial](#spatial-sound-in-newer-versions-of-windows-10) .

Normalement, XAudio 2,9 effectue un repli sur tout l’audio multicanal pour qu’il corresponde au nombre « physique » de canaux audio pris en charge par le point de terminaison audio. Par exemple, si le jeu fournit une source audio de canal 7,1, mais que le son est joué sur un casque, XAudio 2,9 replie le canal audio 7,1 en stéréo, à l’aide d’une matrice de pliage standard de l’industrie. Si le PC est connecté à un point de terminaison Audio HDMI, le canal audio 7,1 est transmis tel quel via la connexion HDMI.

Windows 10 ajoute la prise en charge de l’audio spatial, à l’aide d’un encodeur centralisé qui encode le contenu audio dans un format de [son spatial](../coreaudio/spatial-sound.md) sélectionné par l’utilisateur. Windows 10 est fourni avec un format de son spatial appelé Windows Sonic. D’autres formats, tels que Dolby Atmos pour casque, peuvent être téléchargés à partir du Microsoft Store. Certains des formats de son spatial, tels que Windows Sonic et Dolby Atmos pour casque, sont conçus pour être utilisés sur des points de terminaison audio stéréo. Ces formats pliez le bruit surround au stéréo à l’aide d’algorithmes propriétaires qui obtiennent un effet sonore surround « virtuel ». En d’autres termes, l’écouteur peut percevoir un son à partir de différentes positions dans l’espace 3D, même quand il ne s’agit que de porter un casque ou d’écouter sur une seule paire de haut-parleurs stéréo.

Des effets similaires peuvent être obtenus à l’aide des API [X3DAudio](x3daudio.md) incluses avec xaudio 2,9. La principale différence réside dans le fait que X3DAudio exige que le développeur de l’application le programme de manière explicite pour le son 3D, alors que le son Surround virtuel est appliqué automatiquement à toute source de son basée sur un canal tradional.

Sur Windows 10 1903 et versions ultérieures, les jeux qui utilisent XAudio 2,9 utilisent le format de son spatial à l’ensemble du système que l’utilisateur a activé sur le point de terminaison audio, le cas échéant. Cela signifie que XAudio 2,9 n’effectuera pas le repli habituel du son surround en stéréo. Au lieu de cela, le signal sonore surround est remis à l’encodeur de son spatial (par exemple, Windows Sonic) pour obtenir un effet sonore surround virtuel.

### <a name="createhrtfapo"></a>CreateHrtfApo

La fonction [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) est disponible uniquement sur Windows 10. Elle n’est pas implémentée dans le package redistribuable XAudio 2,9.
