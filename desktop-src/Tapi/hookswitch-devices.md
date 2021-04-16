---
description: Un appareil téléphonique peut avoir plusieurs appareils hookswitch.
ms.assetid: 39e3f24d-55d8-4830-8599-383954c8a107
title: Appareils hookswitch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69ad6f839ec9078831ffe0b04849be2a4393c9d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527603"
---
# <a name="hookswitch-devices"></a>Appareils hookswitch

Un appareil téléphonique peut avoir plusieurs appareils hookswitch. Un hookswitch est le commutateur qui connecte ou déconnecte un appareil de la ligne téléphonique. Sur un téléphone, par exemple, il s’agit du commutateur qui est automatiquement activé lorsqu’un utilisateur soulève le récepteur du socle pour obtenir une nouvelle tonalité. L’interface TAPI définit trois types d’appareils hookswitch pour un téléphone : combiné, haut-parleur et casque. Chaque appareil hookswitch possède un haut-parleur et un composant microphone, et fonctionne dans l’un des quatre modes hookswitch :

-   **OnHook** L’appareil hookswitch est OnHook, et le microphone et le haut-parleur sont désactivés.
-   **Microphone uniquement** L’appareil hookswitch est offhook, son microphone est activé et son haut-parleur est muet.
-   **Conférencier uniquement** L’appareil hookswitch est offhook, son microphone est muet et son haut-parleur est activé.
-   **Microphone et orateur** L’appareil hookswitch est offhook, et les microphones et les haut-parleurs sont activés.

La fonction [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) est utilisée pour définir le mode hookswitch d’un ou plusieurs des appareils hookswitch d’un appareil téléphonique ouvert. Par exemple, pour activer ou désactiver le micro ou le composant de l’orateur d’un appareil hookswitch, utilisez **phoneSetHookSwitch** avec le mode hookswitch approprié. La fonction [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) peut être utilisée pour interroger le mode hookswitch d’un appareil hookswitch sur un appareil téléphonique ouvert.

Lorsque le mode de l’appareil hookswitch d’un téléphone est modifié manuellement, par exemple en soulevant le téléphone de son socle, un message d' [**\_ État téléphonique**](phone-state.md) est envoyé à l’application pour notifier l’application de la modification de l’État. Les paramètres de ce message fournissent une indication de la modification.

Le volume du composant de haut-parleur d’un appareil hookswitch peut être défini avec [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume). Le paramètre de volume est différent de muet dans le fait qu’un haut-parleur est désactivé et que vous le désactiviez par la suite. La fonction [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) peut être utilisée pour retourner le paramètre de volume actuel du haut-parleur d’un appareil hookswitch sur un appareil téléphonique ouvert.

Le composant microphone d’un appareil hookswitch peut également être contrôlé. La valeur du paramètre gain est différente de celle de l’option muet en désactivant un microphone, puis en le désactivant, ce qui préserve le paramètre gain du microphone. Utilisez [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) pour définir le gain du microphone d’un appareil hookswitch d’un appareil téléphonique ouvert, et [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) pour retourner le paramètre de gain du microphone d’un appareil hookswitch d’un téléphone ouvert.

Lorsque le volume ou le gain de l’appareil hookswitch d’un téléphone est modifié, un message d’état de téléphone \_ est envoyé à la fonction d’application pour notifier l’application du changement d’État. Les paramètres de ce message fournissent une indication de la modification.

 

 



