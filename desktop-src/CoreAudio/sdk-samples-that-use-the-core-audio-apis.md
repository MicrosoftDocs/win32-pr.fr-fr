---
description: Exemples de SDK qui utilisent les API audio principales
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: Exemples de SDK qui utilisent les API audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f875095579b40c6646d89e31328c148c5724c309
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114761"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a>Exemples de SDK qui utilisent les API audio principales

le SDK Windows comprend les exemples de code suivants qui illustrent l’utilisation des api Audio de base. les exemples suivants se trouvent dans le répertoire% MSSdk% \\ samples \\ multimedia \\ audio, où% MSSdk% est le répertoire racine de l’installation SDK Windows sur votre ordinateur.




| Exemple | Deascription | 
|--------|--------------|
| <a href="aecmicarray.md">AECMicArray</a> | Cet exemple utilise les API MMDevice, WASAPI, DeviceTopology et EndpointVolume pour capturer un flux vocal de haute qualité. l’exemple prend en charge l’annulation de l’écho acoustique (aec) et le traitement du tableau de microphone à l’aide de l’DMO AEC également appelé DSP de capture vocale fourni par Microsoft. | 
| <a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a> | Cet exemple d’application utilise les API audio de base pour capturer des données audio à partir d’un périphérique d’entrée, spécifié par l’utilisateur et les écrit dans un nom unique. Fichier WAV dans le répertoire actif. Cet exemple illustre la mise en mémoire tampon pilotée par les événements. | 
| <a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a> | Cet exemple d’application utilise les API audio de base pour capturer des données audio à partir d’un périphérique d’entrée, spécifié par l’utilisateur et les écrit dans un nom unique. Fichier WAV dans le répertoire actif. Cet exemple illustre la mise en mémoire tampon pilotée par une minuterie. | 
| <a href="duckingcapturesample.md">DuckingCaptureSample</a> | Cet exemple d’application montre l’ouverture et la fermeture de flux de communication et la mise en place d’événements de canard qu’une application peut atteindre pour implémenter l’atténuation du flux. Cette application implémente un client de conversation qui utilise des API audio de base pour lire les données audio à partir d’un périphérique de communication et les lire sur le périphérique de sortie. | 
| <a href="endpointvolume.md">EndpointVolume</a> | Cet exemple d’application utilise les API audio de base pour modifier le volume de l’appareil, spécifié par l’utilisateur. | 
| <a href="osd.md">DÉPLOIEMENT</a> | Cet exemple utilise les API MMDevice et EndpointVolume pour implémenter un affichage à l’écran qui affiche les modifications de volume du flux de sortie qui s’exécutent par le biais du périphérique de point de terminaison de rendu audio par défaut. l’affichage à l’écran s’affiche lorsque l’utilisateur ajuste le niveau de volume dans le programme de contrôle de volume Windows, Sndvol.exe et disparaît une fois que le niveau de volume reste inchangé pendant une brève période. | 
| <a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a> | Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur. Cet exemple illustre la mise en mémoire tampon pilotée par les événements pour un client de rendu en mode exclusif. Pour un flux en mode exclusif, le client partage la mémoire tampon du point de terminaison avec le périphérique audio. | 
| <a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a> | Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur. Cet exemple illustre la mise en mémoire tampon pilotée par minuterie pour un client de rendu en mode exclusif. Pour un flux en mode exclusif, le client partage la mémoire tampon du point de terminaison avec le périphérique audio. | 
| <a href="rendersharedeventdriven.md">RenderSharedEventDriven</a> | Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur. Cet exemple illustre la mise en mémoire tampon pilotée par les événements pour un client de rendu en mode partagé. Pour un flux en mode partagé, le client partage la mémoire tampon du point de terminaison avec le moteur audio. | 
| <a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a> | Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur. Cet exemple illustre la mise en mémoire tampon pilotée par minuterie pour un client de rendu en mode partagé. Pour un flux en mode partagé, le client partage la mémoire tampon du point de terminaison avec le moteur audio. | 
| WinAudio | Cet exemple utilise l’API MMDevice et WASAPI pour lire et capturer des flux audio. L’interface utilisateur de cet exemple d’application permet aux utilisateurs de sélectionner des appareils de point de terminaison audio, de modifier le niveau de volume de la session audio locale et de lire les fichiers. wav et l’entrée du microphone.<blockquote>[!Note]<br />cet exemple est déconseillé dans Windows 7.</blockquote><br /> | 




 

vous pouvez télécharger le SDK Windows à partir du site web du [centre de téléchargement Microsoft Windows SDK](https://developer.microsoft.com/windows/downloads/sdk-archive/) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[à propos des api Audio Windows Core](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




