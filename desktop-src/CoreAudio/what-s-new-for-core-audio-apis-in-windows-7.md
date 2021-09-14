---
description: les api audio de base ont été introduites dans Windows Vista, qui a fourni un nouvel ensemble de composants audio en mode utilisateur qu’une application cliente peut utiliser pour afficher ou capturer des flux audio avec des fonctionnalités audio améliorées.
ms.assetid: eb99c266-16d2-4a14-bc1d-059a0a94db13
title: nouveautés des api Audio principales dans Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6160b275512a7efbd3b795e263f2ce8ae01be965
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114706"
---
# <a name="whats-new-for-core-audio-apis-in-windows-7"></a>nouveautés des api Audio principales dans Windows 7

les api audio de base ont été introduites dans Windows Vista, qui a fourni un nouvel ensemble de composants audio en mode utilisateur qu’une application cliente peut utiliser pour afficher ou capturer des flux audio avec des fonctionnalités audio améliorées. pour obtenir une vue d’ensemble générale de cet ensemble d’api, consultez [à propos des api Audio Windows Core](about-the-windows-core-audio-apis.md).

les api Audio principales ont été améliorées dans Windows 7. Le tableau suivant récapitule les nouvelles fonctionnalités et les améliorations apportées aux API audio principales :




| Fonctionnalité | Description | 
|---------|-------------|
| Améliorations génériques | les fonctionnalités suivantes ont été améliorées dans Windows 7 :<ul><li>dans Windows 7, les flux en mode de partage s’exécutent en <em>mode faible latence</em>. Le moteur audio s’exécute en mode par extraction avec une réduction significative de la latence. Cela est très utile pour les applications de communication qui nécessitent une faible latence de flux audio pour accélérer la diffusion en continu.</li><li>Windows 7 offre une meilleure détection des rôles d’appareils lorsqu’un nouvel appareil est ajouté au système. Pour plus d’informations, consultez <a href="device-roles-in-windows-vista.md">utilisation des rôles d’appareil</a>.</li><li>dans Windows 7, vous pouvez écouter de la musique à partir de votre lecteur multimédia portable via les haut-parleurs de votre ordinateur. Vous pouvez utiliser cette fonctionnalité de moniteur de capture en branchant un lecteur multimédia portable sur votre ordinateur à l’aide d’un câble audio analogique. Dans le passé, certains OEM ont fourni cette fonctionnalité dans le pilote audio à l’aide d’une boucle matérielle. dans Windows 7, cette fonctionnalité a été ajoutée au système d’exploitation. Comme il s’agit du système et non du pilote, vous pouvez l’utiliser pour tout autre appareil connecté au système, tel qu’un casque USB.</li><li>l’audio HDMI a été amélioré dans Windows 7, qui prend en charge le format de débit élevé. Avec cette amélioration, vous pouvez prendre en charge l’audio multicanal et les formats audio compressés sur un connecteur HDMI sur un récepteur audio.</li><li>dans Windows Vista, Lecteur Windows Media ne lit la musique que par le biais du périphérique audio par défaut, qui ne peut pas être modifié par l’utilisateur. pour que Lecteur Windows Media restitue l’audio sur un appareil particulier, l’appareil par défaut doit être modifié dans le panneau de configuration <strong>sons</strong> . dans Windows 7, Lecteur Windows Media fournit des api qui permettent à une application d’effectuer un rendu sur n’importe quel appareil sélectionné par l’utilisateur et pas seulement l’appareil par défaut.</li><li>dans Windows Vista, si un ordinateur qui lit des données audio bascule en mode d’économie d’énergie, l’ordinateur est verrouillé et, si l’utilisateur souhaite interrompre la lecture, l’utilisateur doit ouvrir une session et appuyer sur la touche arrêter pour arrêter la lecture. dans Windows 7, si l’ordinateur est verrouillé, vous pouvez toujours contrôler la lecture à l’aide du contrôle HID sur le clavier.</li><li>Windows 7 réduit la consommation d’énergie pour toute application qui utilise DirectSound et DirectShow pour le rendu des médias. En outre, le service Planificateur de classes multimédias active le son résistant aux problèmes et utilise moins d’énergie pendant la génération des échantillons audio.</li></ul> | 
| Appareil de communication (nouveau) | Dans cette version, un nouveau type d’appareil a été ajouté au panneau de configuration <strong>sons</strong> : appareil de <strong>communication</strong> . Cet appareil est principalement utilisé pour les communications, c’est-à-dire pour placer ou recevoir des appels téléphoniques sur l’ordinateur. Une application de communication peut utiliser des composants audio fondamentaux pour obtenir une référence au point de terminaison du périphérique de communication par défaut et afficher des flux audio à des fins de communication. Le système d’exploitation considère le flux ouvert sur un appareil de communication comme un flux de communication. Les opérations WASAPI sur un flux de communication sont similaires à tout autre flux audio. Pour plus d’informations, consultez <a href="device-roles-in-windows-vista.md">utilisation des rôles d’appareil</a>. | 
| Atténuation de flux ou enchaînement audio (nouveauté) | l’atténuation automatique ou l' <a href="stream-attenuation.md">atténuation du flux</a> est une nouvelle fonctionnalité de Windows 7 qui est destinée aux applications VoIP et de Communication unifiée. Par défaut, le système d’exploitation réduit l’intensité d’un flux audio lorsqu’un flux de communication, tel qu’un appel téléphonique, est reçu sur le périphérique de communication sur l’ordinateur. Les options de volume sont définies par l’utilisateur dans le panneau de configuration du <strong>son</strong> . de nouvelles api ont été ajoutées dans le SDK Windows qui permettent aux applications de remplacer le comportement de l’entourage par défaut. Pour plus d’informations sur l’implémentation d’une fonctionnalité de canard personnalisée, consultez <a href="providing-a-custom-ducking-experience.md">fourniture d’un comportement de canard personnalisé</a>. <br /> | 
| Routage de flux (nouveau) | dans Windows 7, les api audio principales ont été améliorées pour transférer un flux audio en toute transparence d’un appareil existant vers un nouveau point de terminaison audio par défaut. Les ensembles d’API audio de haut niveau qui utilisent des API audio de base, telles que Media Foundation, DirectSound et les API WAVE, implémentent la fonctionnalité de routage de flux. Les applications multimédias qui utilisent ces ensembles d’API pour lire ou capturer un flux utilisent l’implémentation par défaut et n’ont pas besoin de modifier l’application. Toutefois, si votre application multimédia utilise directement des API audio principales, l’application doit fournir l’implémentation du routage de flux. Pour ce faire, l’application doit gérer les nouveaux événements qui ont été ajoutés qui notifient un client WASAPI lorsque l’appareil par défaut est connecté ou supprimé. Pour plus d’informations sur cette fonctionnalité, consultez <a href="stream-routing.md">routage de flux</a>. | 
| PUMA (Protected user mode audio) (amélioré) | PUMA a été mis à jour pour Windows 7 afin de fournir les fonctionnalités suivantes :<ul><li>Définition des bits SCMS (Serial Copy Management System) sur les points de terminaison S/PDIF et les bits de protection du contenu numérique à bande passante élevée (HDCP) sur les points de terminaison HDMI (High-Definition Multimedia Interface).</li><li>Activation des contrôles de protection SCMS et HDMI en dehors d’un environnement protégé (PE).</li></ul>Pour plus d’informations sur les améliorations apportées, consultez <a href="protected-user-mode-audio--puma-.md">Puma (Protected user mode audio)</a>.<br /> | 
| La structure <strong>WAVEFORMATEXTENSIBLE</strong> a été étendue à la structure <strong>WAVEFORMATEXTENSIBLE_IEC61937</strong> (nouveauté) | dans Windows 7, une nouvelle structure a été ajoutée pour prendre en charge les transmissions IEC 61937. <strong>WAVEFORMATEXTENSIBLE_IEC61937</strong> étend la structure <strong>WAVEFORMATEXTENSIBLE</strong> pour stocker deux jeux de caractéristiques de flux audio : le format audio encodé avant la transmission et les caractéristiques du flux audio après qu’il a été décodé. La nouvelle structure spécifie explicitement le nombre effectif de canaux, la taille de l’échantillon et le débit de données d’un format non-PCM. Avec ces informations, une application peut déduire le niveau de qualité du flux non-PCM après sa décompression et sa lecture. Pour plus d’informations, consultez <a href="representing-formats-for-iec-61937-transmissions.md">représentation des formats des transmissions IEC 61937</a>.<br /> | 
| <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient :: Initialize</strong></a> (amélioré) | La méthode <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient :: Initialize</strong></a> a été améliorée pour indiquer des erreurs spécifiques qui peuvent se produire lors de l’ouverture d’un flux audio. Les nouveaux codes d’erreur sont les suivants :<ul><li>AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED</li><li>AUDCLNT_E_BUFFER_SIZE_ERROR</li><li>AUDCLNT_E_INVALID_DEVICE_PERIOD</li></ul>Pour plus d’informations sur ces erreurs, consultez la section valeur de retour dans <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient :: Initialize</strong></a>.<br /> | 
| <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient :: GetBuffer</strong></a> et <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient :: GetBuffer</strong></a> (amélioration) | Les méthodes <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient :: GetBuffer</strong></a> et <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient :: GetBuffer</strong></a> ont été améliorées pour retourner le AUDCLNT_E_BUFFER_ERROR code d’erreur qui indique que la mémoire tampon du point de terminaison en mode exclusif n’a pas été récupérée. Pour plus d’informations, consultez la section Notes dans <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient :: GetBuffer</strong></a> et <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient :: GetBuffer</strong></a>. | 
| Capacité de détection des jacks (améliorée) | une nouvelle interface dans Windows 7, <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2"><strong>IKsJackDescription2</strong></a>, étend <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription"><strong>IKsJackDescription</strong></a>. À l’aide de la nouvelle interface, la pile audio ou une application peut obtenir des informations supplémentaires sur le Jack. Cela inclut la fonctionnalité de détection du Jack et indique si le format de l’appareil a été modifié de manière dynamique. | 
| Windows Exemples (nouveau) | de nouveaux exemples ont été ajoutés au SDK Windows qui illustrent l’utilisation des api Audio de base. Pour plus d’informations, consultez <a href="sdk-samples-that-use-the-core-audio-apis.md">les exemples du kit de développement logiciel (SDK) qui utilisent les API audio principales</a>. | 




 

## <a name="major-new-interfaces"></a>Nouvelles interfaces majeures

les interfaces suivantes sont nouvelles pour Windows 7 :

-   [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)
-   [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)
-   [**IAudioEndpointVolumeEx**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)
-   [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)
-   [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)
-   [**IAudioSessionEnumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)
-   [**IAudioSessionNotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)
-   [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)
-   [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)
-   [**IKsJackSinkInformation**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[à propos des api Audio Windows Core](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




