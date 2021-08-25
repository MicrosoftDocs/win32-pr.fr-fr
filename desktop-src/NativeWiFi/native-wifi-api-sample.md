---
description: Illustre l’utilisation des fonctions de base de gestion de réseau sans fil.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Exemple d’API WiFi Native
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed28fadcd73eb4b3e632702078280ddba55d683c66decfdf03bc948182c52d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801059"
---
# <a name="native-wifi-api-sample"></a>Exemple d’API WiFi Native

un exemple d’API Wifi Native qui illustre l’utilisation des fonctions de gestion de réseau sans fil de base est inclus dans le kit de développement logiciel (SDK) de Microsoft Windows. la dernière version du SDK Windows est disponible à partir du [centre de téléchargement](https://developer.microsoft.com/windows/downloads).

Par défaut, l’exemple de code source wifi natif est installé dans le répertoire suivant :

**C : \\ Program Files \\ Microsoft sdk \\ Windows \\ <version number> \\ exemples \\ NetDs \\ Wlan**

L’exemple d’API WiFi Native se trouve dans le dossier suivant :

**autoconfig**

l’exemple Wifi natif peut être compilé et exécuté sur Windows Vista et versions ultérieures, Windows xp avec service pack 3 (SP3) et l’API de réseau local sans fil pour Windows XP avec service pack 2 (SP2). certaines fonctionnalités de l’exemple ne sont pas prises en charge sur Windows xp avec SP3 et l’API LAN sans fil pour Windows XP avec SP2. pour obtenir la liste des fonctions prises en charge par Windows xp avec SP3 et l’api de réseau local sans fil pour Windows XP avec SP2, consultez [prise en charge de l’api Wifi Native sur Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).

L’exemple WiFi natif montre comment effectuer les tâches suivantes :

-   Énumérer les interfaces sans fil. Consultez [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).
-   Obtient les fonctionnalités d’une interface. Consultez [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).

    * * Windows xp avec SP3 et l’API LAN sans fil pour Windows XP avec SP2 : * * cette fonctionnalité n’est pas prise en charge.

-   Interrogez une interface. Consultez [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).
-   Définissez les paramètres d’une interface réseau. Consultez [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface). Cette fonction peut être utilisée pour activer et désactiver la radio sans fil (et, par conséquent, activer ou désactiver la connectivité de réseau sans fil).
-   Recherchez les réseaux sans fil disponibles. Consultez [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).
-   Obtient la liste des réseaux sans fil disponibles ou visibles. Consultez [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).
-   Obtenir, enregistrer ou supprimer un profil. Consultez [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)et [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).
-   Connecter ou se déconnecter d’un réseau sans fil. Consultez [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) et [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la WiFi Native](using-native-wifi.md)
</dt> <dt>

[Windows Forum du kit de développement logiciel sans fil Vista](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

[résolution des problèmes Windows les connexions sans fil Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))
</dt> </dl>

 

 
