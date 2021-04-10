---
description: Exemples de SDK qui utilisent les API audio principales
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: Exemples de SDK qui utilisent les API audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15eb05da5fefc22eaa0987d9996f0ddb48702158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950674"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a>Exemples de SDK qui utilisent les API audio principales

Le SDK Windows comprend les exemples de code suivants qui illustrent l’utilisation des API audio de base. Les exemples suivants se trouvent dans le répertoire% MSSdk% \\ Samples \\ Multimedia \\ audio, où% MSSdk% est le répertoire racine de l’installation SDK Windows sur votre ordinateur.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Exemple</th>
<th>Deascription</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="aecmicarray.md">AECMicArray</a></td>
<td>Cet exemple utilise les API MMDevice, WASAPI, DeviceTopology et EndpointVolume pour capturer un flux vocal de haute qualité. L’exemple prend en charge l’annulation de l’écho acoustique (AEC) et le traitement du tableau de microphone à l’aide de l’AEC DMO également appelé le DSP de capture vocale fourni par Microsoft.</td>
</tr>
<tr class="even">
<td><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></td>
<td>Cet exemple d’application utilise les API audio de base pour capturer des données audio à partir d’un périphérique d’entrée, spécifié par l’utilisateur et les écrit dans un nom unique. Fichier WAV dans le répertoire actif. Cet exemple illustre la mise en mémoire tampon pilotée par les événements.</td>
</tr>
<tr class="odd">
<td><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></td>
<td>Cet exemple d’application utilise les API audio de base pour capturer des données audio à partir d’un périphérique d’entrée, spécifié par l’utilisateur et les écrit dans un nom unique. Fichier WAV dans le répertoire actif. Cet exemple illustre la mise en mémoire tampon pilotée par une minuterie.</td>
</tr>
<tr class="even">
<td><a href="duckingcapturesample.md">DuckingCaptureSample</a></td>
<td>Cet exemple d’application montre l’ouverture et la fermeture de flux de communication et la mise en place d’événements de canard qu’une application peut atteindre pour implémenter l’atténuation du flux. Cette application implémente un client de conversation qui utilise des API audio de base pour lire les données audio à partir d’un périphérique de communication et les lire sur le périphérique de sortie.</td>
</tr>
<tr class="odd">
<td><a href="endpointvolume.md">EndpointVolume</a></td>
<td>Cet exemple d’application utilise les API audio de base pour modifier le volume de l’appareil, spécifié par l’utilisateur.</td>
</tr>
<tr class="even">
<td><a href="osd.md">DÉPLOIEMENT</a></td>
<td>Cet exemple utilise les API MMDevice et EndpointVolume pour implémenter un affichage à l’écran qui affiche les modifications de volume du flux de sortie qui s’exécutent par le biais du périphérique de point de terminaison de rendu audio par défaut. L’affichage à l’écran s’affiche lorsque l’utilisateur ajuste le niveau de volume dans le programme de contrôle de volume Windows, Sndvol.exe, et disparaît une fois que le volume reste inchangé pendant une brève période.</td>
</tr>
<tr class="odd">
<td><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></td>
<td>Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur. Cet exemple illustre la mise en mémoire tampon pilotée par les événements pour un client de rendu en mode exclusif. Pour un flux en mode exclusif, le client partage la mémoire tampon du point de terminaison avec le périphérique audio.</td>
</tr>
<tr class="even">
<td><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></td>
<td>Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur. Cet exemple illustre la mise en mémoire tampon pilotée par minuterie pour un client de rendu en mode exclusif. Pour un flux en mode exclusif, le client partage la mémoire tampon du point de terminaison avec le périphérique audio.</td>
</tr>
<tr class="odd">
<td><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></td>
<td>Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur. Cet exemple illustre la mise en mémoire tampon pilotée par les événements pour un client de rendu en mode partagé. Pour un flux en mode partagé, le client partage la mémoire tampon du point de terminaison avec le moteur audio.</td>
</tr>
<tr class="even">
<td><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></td>
<td>Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur. Cet exemple illustre la mise en mémoire tampon pilotée par minuterie pour un client de rendu en mode partagé. Pour un flux en mode partagé, le client partage la mémoire tampon du point de terminaison avec le moteur audio.</td>
</tr>
<tr class="odd">
<td>WinAudio</td>
<td>Cet exemple utilise l’API MMDevice et WASAPI pour lire et capturer des flux audio. L’interface utilisateur de cet exemple d’application permet aux utilisateurs de sélectionner des appareils de point de terminaison audio, de modifier le niveau de volume de la session audio locale et de lire les fichiers. wav et l’entrée du microphone.
<blockquote>
[!Note]<br />
Cet exemple est déconseillé dans Windows 7.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Vous pouvez télécharger le SDK Windows à partir du site Web du [Centre de téléchargement Microsoft Windows SDK](https://developer.microsoft.com/windows/downloads/sdk-archive/) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des API audio Windows Core](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




