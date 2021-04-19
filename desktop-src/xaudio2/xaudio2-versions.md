---
description: XAudio2 est une API multiplateforme qui a été fournie pour une utilisation sur Xbox 360, ainsi que sur les versions de Windows, notamment Windows XP, Windows Vista, Windows 7 et Windows 8.
ms.assetid: 875b44c4-30d6-8a6e-0cfc-9beb8c46f1b4
title: Versions de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c9facfe357c323bd8f7b607460a8f59bd062fe
ms.sourcegitcommit: 010f524cd6098a5941de77907d4d6ae7871f8af1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "106538234"
---
# <a name="xaudio2-versions"></a>Versions de XAudio2

XAudio2 est une API multiplateforme qui a été fournie pour une utilisation sur Xbox 360, ainsi que sur les versions de Windows, notamment Windows XP, Windows Vista, Windows 7 et Windows 8. Sur Xbox 360, XAudio2 est fourni sous la forme d’une bibliothèque statique qui est compilée dans l’exécutable principal du jeu. Sur Windows, XAudio2 est fourni sous la forme d’une bibliothèque de liens dynamiques (DLL) installée dans les dossiers système du système d’exploitation.

## <a name="xaudio-29-windows-10-and-redistributable-for-windows-7-and-windows-8x"></a>XAudio 2,9 (Windows 10 et redistribuable pour Windows 7 et Windows 8. x)

XAudio2 version 2,9 est fournie dans le cadre de Windows 10, XAUDIO2 \_9.DLL, à côté de XAudio 2,8 pour prendre en charge des applications plus anciennes. Une [version redistribuable de XAudio 2,9](xaudio2-redistributable.md) est également disponible pour Windows 7 SP1, Windows 8 et Windows 8.1.

XAudio 2.9 a été mis à jour avec les modifications suivantes :

-   Nouveaux indicateurs de création : \_ moteur de débogage XAUDIO2 \_ , \_ moteur XAUDIO2 stop \_ \_ en cas d' \_ inactivité, XAUDIO2 \_ 1024 \_ Quantum
-   la prise en charge de xWMA est disponible dans cette version de XAudio2.
-   La fonction [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) est prise en charge dans la version Windows 10 de xaudio 2,9.
-   [**XAUDIO2FX \_ Les \_ paramètres de réverbération**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) incluent désormais la valeur *SideDelay* pour les systèmes 7,1.
-   La fonction [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative) comprend maintenant le paramètre booléen *sevenDotOneReverb* qui active la réverbération 7,1.

## <a name="xaudio-28-windows-8x"></a>XAudio 2,8 (Windows 8. x)

XAudio2 version 2,8 est fournie aujourd’hui en tant que composant système dans Windows 8, XAUDIO2 \_8.DLL. Elle est disponible dans la « boîte de réception » et ne nécessite pas de redistribution avec une application. Nous vous recommandons d’utiliser le kit de développement logiciel (SDK) Windows pour Windows 8 pour développer sur XAudio2 ; le SDK Windows pour Windows 8 contient l’en-tête et la bibliothèque d’importation nécessaires à la liaison statique avec XAUDIO2 \_8.DLL.

XAudio2 2,8 a été mis à jour avec les modifications suivantes :

-   Cette version prend en charge le développement d’applications du Windows Store. l’API XAudio2 peut être utilisée dans les applications du Windows Store C++/DirectX.
-   [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) est un appel d’API Win32 plat et ne crée plus de CLSID XAudio2. La prise en charge de l’instanciation de XAudio2 par CoCreateInstance a été supprimée.
-   La fonction Initialize est maintenant appelée implicitement par le processus de création et a été supprimée de l’interface [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .
-   La fonctionnalité d’énumération des appareils a été supprimée de XAudio2 ; les fonctions GetDeviceDetails et GetDeviceCount ont été supprimées de l’interface [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) . Les applications qui souhaitent effectuer un rendu sur d’autres périphériques audio sur le système doivent transmettre une chaîne d’identificateur de périphérique à [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) au lieu d’un index d’appareil. Le périphérique de rendu audio par défaut peut toujours être créé sans énumération.
-   [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) a une fonction ajoutée [**IXAudio2MasteringVoice :: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) pour qui retourne le masque de canal pour le périphérique de sortie de destination.
-   Les bibliothèques [X3DAudio](x3daudio.md) et [XAPOFX](xapofx-overview.md) sont fusionnées dans XAudio2. Le code d’application utilise toujours des en-têtes distincts, X3DAUDIO. H et XPOFX. Mais maintenant, il est lié à une bibliothèque d’importation unique, XAUDIO2 \_ 8. lib.
-   la prise en charge de xWMA n’est pas disponible dans cette version de XAudio2 ; xWMA ne sera pas pris en charge en tant que format de mémoire tampon audio lors de l’appel de CreateSourceVoice. Nous recommandons maintenant l’Media Foundation objet lecteur source pour le décodage d’un grand nombre de formats multimédias dans des mémoires tampons PCM en mémoire.
-   [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) prend désormais quatre paramètres au lieu de deux. Les paramètres les plus récents spécifient les données initiales dans le cadre de la création de [XAPOFX](xapofx-overview.md) .

## <a name="xaudio-27-and-earlier-windows-7"></a>XAudio 2,7 et versions antérieures (Windows 7)

Toutes les versions précédentes de XAudio2 pour une utilisation dans les applications sont fournies en tant que dll redistribuables dans le kit de développement logiciel (SDK) DirectX. La première version de XAudio2, XAudio2 2,0, est fournie dans la version de mars 2008 du SDK DirectX. La dernière version à envoyer dans le kit de développement logiciel (SDK) DirectX était XAudio2 2,7, disponible dans la dernière version du kit de développement logiciel (SDK) DirectX en juin 2010.

Le SDK DirectX hérité n’est plus disponible sur les téléchargements Microsoft en raison de la mise hors service de tous les contenus signés SHA-1. Le 2010 juin était la version de fin de vie.

Les versions précédentes de XAudio2 ne peuvent pas être utilisées pour générer des applications du Windows Store pour Windows 8.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main](getting-started.md)
</dt> <dt>

[Concepts clés de XAudio2](xaudio2-key-concepts.md)
</dt> </dl>

[Guide du développeur pour la version redistribuable de XAudio 2.9](xaudio2-redistributable.md)
</dt> </dl>
 

 
