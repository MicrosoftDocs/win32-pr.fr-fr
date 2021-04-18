---
description: Illustre l’utilisation des fonctions de base de gestion de réseau sans fil.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Exemple d’API WiFi Native
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ac72000363fcb91f013c3f55d4686335c0a59e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519093"
---
# <a name="native-wifi-api-sample"></a>Exemple d’API WiFi Native

Un exemple d’API WiFi native qui illustre l’utilisation des fonctions de gestion de réseau sans fil de base est inclus dans le kit de développement logiciel (SDK) Microsoft Windows. La dernière version du SDK Windows est disponible à partir du [Centre de téléchargement](https://developer.microsoft.com/windows/downloads).

Par défaut, l’exemple de code source wifi natif est installé dans le répertoire suivant :

**C : \\ Program Files \\ Microsoft SDK \\ \\ <version number> \\ exemples Windows \\ NetDs \\ WLAN**

L’exemple d’API WiFi Native se trouve dans le dossier suivant :

**autoconfig**

L’exemple WiFi natif peut être compilé et exécuté sur Windows Vista et versions ultérieures, Windows XP avec Service Pack 3 (SP3) et l’API de réseau local sans fil pour Windows XP avec Service Pack 2 (SP2). Certaines fonctionnalités de l’exemple ne sont pas prises en charge sur Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2. Pour obtenir la liste des fonctions prises en charge par Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2, consultez [prise en charge de l’API WiFi native sur Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).

L’exemple WiFi natif montre comment effectuer les tâches suivantes :

-   Énumérer les interfaces sans fil. Consultez [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).
-   Obtient les fonctionnalités d’une interface. Consultez [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).

    * * Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 : * * cette fonctionnalité n’est pas prise en charge.

-   Interrogez une interface. Consultez [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).
-   Définissez les paramètres d’une interface réseau. Consultez [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface). Cette fonction peut être utilisée pour activer et désactiver la radio sans fil (et, par conséquent, activer ou désactiver la connectivité de réseau sans fil).
-   Recherchez les réseaux sans fil disponibles. Consultez [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).
-   Obtient la liste des réseaux sans fil disponibles ou visibles. Consultez [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).
-   Obtenir, enregistrer ou supprimer un profil. Consultez [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)et [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).
-   Se connecter ou se déconnecter d’un réseau sans fil. Consultez [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) et [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la WiFi Native](using-native-wifi.md)
</dt> <dt>

[Forum du kit de développement logiciel sans fil Windows Vista](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

[Résolution des problèmes de connexions sans fil Windows Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))
</dt> </dl>

 

 
