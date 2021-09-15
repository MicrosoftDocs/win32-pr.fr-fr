---
title: Glossaire de l’accès aux appareils
description: Voici les termes utilisés dans la documentation de l’API d’accès aux appareils.
Robots: noindex, nofollow
ms.assetid: A6311538-D7CC-4A23-A145-14AF3BBFC4C4
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 8406c41a2666f9014bac27452572c6f88b84e6bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521796"
---
# <a name="device-access-glossary"></a>Glossaire de l’accès aux appareils

Voici les termes utilisés dans la documentation de l’API d’accès aux appareils.

<dl> <dt>

**Conteneur**
</dt> <dd>

Environnement d’exécution hautement restreint dans lequel un processus s’exécute avec un sous-ensemble réduit des privilèges de l’utilisateur. Un processus qui s’exécute dans un AppContainer est appelé « processus AppContainer ». Un processus AppContainer est isolé des autres processus AppContainer et du profil de l’utilisateur. Il dispose d’un accès limité à un très petit sous-ensemble de ressources système telles que les fichiers, les périphériques, les clés de Registre, les points de terminaison d’appel de procédure à distance (RPC) de communication entre processus (IPC) et les ressources réseau.

</dd> <dt>

**Binding**
</dt> <dd>

Association d’un objet d’accès d’appareil à une interface d’appareil particulière. si la liaison est réussie Windows, les applications du windows Store peuvent utiliser l’objet d’accès de l’appareil en tant que répartiteur pour communiquer avec le pilote de périphérique.

</dd> <dt>

**Service Broker**
</dt> <dd>

Composant qui fournit l’accès à une ressource qui n’est pas accordée par défaut.

</dd> <dt>

**Application privilégiée**
</dt> <dd>

Application identifiée dans les métadonnées d’un appareil particulier, comme associé à ce périphérique, afin qu’il puisse communiquer avec l’interface restreinte du pilote de périphérique. Un exemple d’une telle application peut être une application de lecture musicale propriétaire qui dispose d’une autorisation exclusive pour se synchroniser avec un lecteur de musique portable, lorsque les applications de concurrents ne le sont pas. Pour plus d’informations sur la façon de définir les métadonnées d’un appareil ou sur la façon de restreindre un pilote aux applications privilégiées, consultez [applications de l’appareil UWP pour les appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).

</dd> </dl>
