---
description: Illustre l’utilisation de fonctions de réseau hébergé sans fil.
ms.assetid: 3da903c2-bdfa-4c1f-92e7-962551f0e08e
title: Exemple de réseau hébergé sans fil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc91dad883242876d7b0ddf1ec66fb92b18a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514642"
---
# <a name="wireless-hosted-network-sample"></a>Exemple de réseau hébergé sans fil

Un exemple de réseau hébergé sans fil illustrant l’utilisation de fonctions de réseau hébergé sans fil est inclus dans le kit de développement logiciel (SDK) Microsoft Windows. La dernière version du SDK Windows est disponible à partir du [Centre de téléchargement](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).

Par défaut, le code source de l’exemple de réseau hébergé sans fil est installé dans le répertoire suivant :

**C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ NetDs \\ WLAN**

L’exemple de réseau hébergé sans fil se trouve dans le dossier suivant :

**WirelessHostedNetwork**

L’exemple de réseau hébergé sans fil peut être compilé sur le SDK Windows pour Windows 7. L’exemple de réseau hébergé sans fil peut être exécuté sur Windows 7 et sur Windows Server 2008 R2 avec le service de réseau local sans fil installé.

Sur Windows 7 et sur Windows Server 2008 R2 avec le service de réseau local sans fil installé, le système d’exploitation installe un appareil virtuel si une carte sans fil pouvant être hébergée sur un réseau hébergé est présente sur l’ordinateur. Cet appareil virtuel s’affiche normalement dans le « dossier Connexions réseau » en tant que « connexion réseau sans fil 2 » avec le nom d’appareil « carte miniport Microsoft Virtual WiFi » si l’ordinateur possède une seule carte réseau sans fil. Cet appareil virtuel est utilisé exclusivement pour effectuer des connexions de point d’accès logiciel (SoftAP). La durée de vie de cet appareil virtuel est liée à la carte sans fil physique. Si la carte sans fil physique est désactivée, cet appareil virtuel est également supprimé.

Les fonctions de réseau hébergé sans fil permettent de démarrer et d’arrêter le réseau hébergé sans fil, de configurer ou de modifier les paramètres ou de demander des informations.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du réseau hébergé sans fil](about-the-wireless-hosted-network.md)
</dt> <dt>

[Utilisation du partage de connexion Internet et du réseau hébergé](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[**WlanRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 



