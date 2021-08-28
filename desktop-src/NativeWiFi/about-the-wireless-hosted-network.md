---
description: À propos du réseau hébergé sans fil
ms.assetid: a6990759-9b84-4644-8f82-75aa63e8197b
title: À propos du réseau hébergé sans fil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88af34a1e0df2029c230b7b7800130d3b550dbf
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882767"
---
# <a name="about-the-wireless-hosted-network"></a>À propos du réseau hébergé sans fil

le réseau hébergé sans fil est une nouvelle fonctionnalité de réseau local sans fil prise en charge sur Windows 7 et sur Windows Server 2008 R2 avec le Service de réseau local sans fil installé. Cette fonctionnalité implémente deux fonctions principales :

-   La virtualisation d’un adaptateur sans fil physique dans plusieurs cartes sans fil virtuelles, parfois appelées « Wi-Fi virtuel ».
-   Un point d’accès sans fil (AP) basé sur des logiciels, parfois appelé SoftAP qui utilise un adaptateur sans fil virtuel désigné.

ces deux fonctions coexistent dans un système Windows ensemble. L’activation ou la désactivation du réseau hébergé sans fil active ou désactive à la fois Virtual Wi-Fi et SoftAP. Il n’est pas possible d’activer ou de désactiver ces deux fonctions séparément dans Windows.

grâce à cette fonctionnalité, un ordinateur Windows peut utiliser un seul adaptateur sans fil physique pour se connecter en tant que client à un point d’accès matériel, tout en faisant office de point de vue logiciel, ce qui permet à d’autres périphériques sans fil de s’y connecter. Cette fonctionnalité nécessite l’installation d’un adaptateur sans fil prenant en charge le réseau hébergé sur l’ordinateur local. le pilote de la carte sans fil doit implémenter le modèle de pilote de périphérique LAN sans fil défini par Microsoft pour une utilisation sur Windows 7. pour recevoir le logo Windows 7, un pilote sans fil doit implémenter la fonctionnalité de réseau hébergé sans fil.

Au plus un réseau hébergé sans fil est activé à tout moment sur l’ordinateur local et seul un adaptateur sans fil sera utilisé par le réseau hébergé sans fil. si plusieurs cartes sans fil peuvent être hébergées sur un réseau hébergé, Windows choisira un adaptateur à utiliser avec le réseau hébergé sans fil. Lorsque les API réseau hébergées sont utilisées, la carte sans fil à compatibilité réseau hébergée est virtualisée à 3 cartes logiques au maximum :

-   Un adaptateur de station (STA) pour une utilisation par des applications sans fil client ou ad hoc. L’adaptateur STA hérite de tous les paramètres de l’adaptateur sans fil physique d’origine et présente les mêmes comportements que la carte physique. D’un plan conceptuel, vous pouvez afficher l’adaptateur STA comme identique à l’adaptateur physique après la virtualisation. L’adaptateur STA est toujours dans le système tant que la carte physique sans fil correspondante est présente.
-   Un adaptateur AP utilisable par le réseau sans fil hébergé pour héberger SoftAP. l’adaptateur AP n’est présent dans le système de Windows qu’une fois que le réseau hébergé sans fil est appelé pour la première fois (lors du premier appel de la fonction [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing), [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)ou [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) ). Une fois créé, l’adaptateur AP reste dans le système jusqu’à ce que le réseau hébergé sans fil soit désactivé. Si le réseau hébergé sans fil est activé ultérieurement, l’adaptateur AP s’affichera à nouveau dans le système.
-   Un adaptateur de station virtuelle (VSTA) à utiliser par les fournisseurs de matériel pour étendre la fonctionnalité de réseau hébergé sans fil dans Windows. L’adaptateur VSTA est facultatif et peut être créé uniquement dans le système par le service IHV correspondant. contrairement à l’adaptateur AP, l’adaptateur VSTA n’existe dans le système Windows qu’à partir du moment où le service ihv initialise l’adaptateur jusqu’à ce que le service ihv libère l’adaptateur.

La Wi-Fi virtuelle mappe les cartes logiques aux ports NDIS. La liaison des adaptateurs STA, AP et VSTA à des ports NDIS spécifiques est décidée par Windows. L’adaptateur STA est toujours lié au port 0. L’adaptateur AP est lié au port NDIS disponible suivant lors du démarrage de la virtualisation, et la liaison reste la même jusqu’à ce que la virtualisation se termine lorsque le réseau hébergé sans fil est désactivé. L’adaptateur VSTA est lié au port NDIS disponible suivant lorsqu’il est initialisé par le service de fabricant de matériel correspondant et que la liaison reste la même jusqu’à ce qu’elle soit libérée par le service IHV.

Il est possible que l’adaptateur VSTA soit créé pour une utilisation par IHV sans créer l’adaptateur SoftAP.

Les combinaisons suivantes sont valides pour une carte physique avec virtualisation :

-   Adaptateur STA.
-   Adaptateurs STA et AP.
-   Adaptateurs STA et VSTA.
-   Adaptateurs STA, AP et VSTA.

À l’exception du cas de l’adaptateur STA, toutes les autres combinaisons sont valides uniquement lorsque le réseau hébergé sans fil est activé. Comme pour le cas de l’adaptateur STA unique, il s’agit de la carte physique si le réseau sans fil est désactivé. Si le réseau hébergé sans fil est activé, il s’agit de l’adaptateur STA lorsque le réseau sans fil hébergé n’a jamais été appelé dans le système.

Le pontage de couche 2 est interdit entre l’adaptateur AP et les autres adaptateurs du système. La même restriction s’applique à l’adaptateur VSTA lorsqu’il est présent dans le système.

la fonctionnalité de réseau hébergé sans fil dans Windows implémente un SoftAP. Toutefois, ce SoftAP n’est pas conçu pour remplacer les périphériques d’AP sans fil basés sur le matériel. En particulier, si le réseau hébergé sans fil est en cours d’exécution lorsque l’ordinateur passe en mode veille (veille), en veille prolongée ou avant le redémarrage de l’ordinateur, le réseau sans fil est arrêté. Le réseau hébergé sans fil ne redémarre pas automatiquement une fois que l’ordinateur sort du mode veille, veille prolongée ou redémarrage. En outre, SoftAP ne fournit pas la résolution DNS. Dans le cas où un serveur DNS externe n’est pas disponible à l’aide du partage de connexion Internet (voir la discussion sur ICS ci-dessous), la résolution du nom de domaine complet (FQDN) entre deux ordinateurs ou appareils connectés avec le SoftAP, y compris l’ordinateur hébergeant le SoftAP, fonctionne uniquement si les deux entités marquent le type de réseau du réseau SoftAP comme privé (accueil ou travail dans la fenêtre contextuelle catégorie réseau). Étant donné que l’ordinateur hébergeant le SoftAP marque toujours le type de réseau SoftAP comme privé, seuls les ordinateurs ou les périphériques connectés à SoftAP doivent marquer le type de réseau SoftAP comme privé pour que la résolution du nom de domaine complet fonctionne.

SoftAP et la mise en réseau ad hoc s’excluent mutuellement sur la même carte physique. Si SoftAP est en cours d’exécution sur l’adaptateur AP et qu’un utilisateur ou une application démarre la mise en réseau ad hoc sur l’adaptateur STA, SoftAP est arrêté. La mise en réseau ad hoc IIF s’exécute sur l’adaptateur STA. une tentative de démarrage de SoftAP sur l’adaptateur AP échouera.

Pour assurer la protection des communications sans fil entre l’ordinateur hébergeant SoftAP et les appareils qui se connectent au SoftAP, le réseau sans fil hébergé exige que tous les appareils connectés utilisent la suite de chiffrement WPA2-PSK/AES. la clé partagée est une valeur de 63 caractères générée par Windows lorsque le réseau sans fil hébergé est appelé pour la première fois (lors du premier appel de la fonction [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing), [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)ou [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) ). Un utilisateur ou une application ne peut pas modifier la valeur de cette clé partagée, mais une application peut demander au système d’exploitation de régénérer une nouvelle clé en appelant la fonction [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings) ou un utilisateur peut demander au système d’exploitation de régénérer une nouvelle clé à l’aide des commandes **netsh wlan** . Cette clé partagée est appelée clé primaire ou clé système pour le réseau hébergé sans fil et est persistante au démarrage et à l’arrêt du réseau hébergé sans fil. Cette clé primaire est appelée « clé de sécurité système » dans les commandes **netsh wlan** .

Pour faciliter l’utilisation, le réseau sans fil hébergé prend également en charge le concept de clé de sécurité secondaire ou utilisateur qui est plus convivial, mais qui peut être moins sécurisé. Cette clé secondaire est appelée « clé de sécurité utilisateur » dans les commandes **netsh wlan** . La clé secondaire n’est pas générée par Windows. L’utilisateur doit fournir la valeur de cette clé. Un utilisateur ou une application peut définir ou modifier la valeur de clé en appelant la fonction [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey) ou en utilisant les commandes **netsh wlan** . La clé secondaire peut être définie pour être persistante ou temporaire. Pour une clé temporaire, si le réseau sans fil hébergé est déjà en cours d’exécution, la clé secondaire est valide jusqu’à ce que le réseau hébergé sans fil s’arrête. Pour une clé temporaire, si le réseau sans fil hébergé n’est pas en cours d’exécution, il n’est valide que lors du démarrage et de l’arrêt du réseau hébergé sans fil suivant.

Il y a exactement une clé primaire et au plus une clé secondaire pour les Hetwork hébergés sans fil sur n’importe quel ordinateur. Tout appareil approvisionné par le biais d’une installation Wi-Fi protégée (WPS) recevra la clé primaire. D’autres appareils configurés manuellement peuvent utiliser l’une ou l’autre clé. Chaque fois qu’une clé est modifiée, tout appareil avec l’ancienne valeur de clé ne sera pas en mesure de se connecter au réseau hébergé sans fil sans être remis à nouveau avec la nouvelle clé. Toutefois, les appareils avec l’autre clé inchangée continueront à être en mesure de se connecter au réseau hébergé sans fil.

Une application peut s’inscrire pour les notifications de réseau hébergé sans fil. une notification WLAN est donc envoyée au rappel d’application lorsque les propriétés changent sur le réseau hébergé sans fil. Une application s’inscrit pour les notifications de réseau hébergé sans fil en appelant [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification) avec le paramètre *dwNotifSource* défini sur include the WLAN \_ notification \_ source \_ HNWK bit.

Windows offre deux moyens permettant aux administrateurs informatiques de gérer la fonctionnalité de réseau hébergé sans fil. Pour les ordinateurs membres d’un domaine, les administrateurs peuvent utiliser la stratégie de groupe pour interdire le réseau hébergé sans fil. À l’aide des commandes **netsh wlan** , un administrateur peut activer ou désactiver le réseau hébergé sans fil localement sur l’ordinateur.

## <a name="supported-scenarios-for-wireless-hosted-network"></a>Scénarios pris en charge pour le réseau hébergé sans fil

le réseau hébergé sans fil permet deux scénarios majeurs pour Windows ordinateurs :

• La possibilité de fournir un réseau personnel sans fil pour une utilisation avec différents autres périphériques sans fil.

• Partage de connexion réseau utilisable par d’autres ordinateurs et périphériques.

Le PAN sans fil est le principal scénario activé par le réseau sans fil hébergé. Une fois que le réseau hébergé sans fil est démarré sur un ordinateur, tous les périphériques sans fil prenant en charge WPA2-PSK/AES sont en mesure de se connecter au softAP comme s’il se connecte à un point d’accès matériel standard. les appareils connectés au réseau sans fil sont dotés d’un PAN sans fil, où ils peuvent échanger des informations avec l’ordinateur Windows hébergeant le SoftAP et entre eux.

Le partage de connexion réseau utilisé par d’autres ordinateurs et périphériques requiert l’utilisation du partage de connexion Internet (ICS). Dans ce scénario, l’interface publique de l’ICS est la connexion partagée, tandis que l’interface privée est la carte virtuelle qui héberge le SoftAP. La connexion partagée peut être une connexion Ethernet, un réseau local sans fil ou une connexion de réseau étendu sans fil. Dans le cas d’une connexion de réseau local sans fil, l’interface publique de l’ICS peut être soit à partir d’une autre carte réseau sans fil, soit à partir de la carte virtuelle de la station sur le même adaptateur sans fil physique qui héberge le SoftAP. L’utilisation la plus courante du partage réseau est le partage d’une connexion Internet, où le réseau de l’interface publique de l’ICS a accès à Internet.

le réseau hébergé sans fil interagit avec Wi-Fi installation protégée (WPS), une autre nouvelle fonctionnalité importante de Windows 7 et Windows Server 2008 R2 avec le Service de réseau local sans fil installé. Le réseau hébergé sans fil et WPS prennent en charge un scénario qui configure un appareil compatible WPS pour un point d’accès matériel compatible avec WPS. dans ce cas, le SoftAP hébergé sur Windows est appelé en arrière-plan pour envoyer le profil d’AP matériel sur le périphérique basé sur WPS.

## <a name="user-and-application-access-to-wireless-hosted-network"></a>Accès des utilisateurs et des applications au réseau hébergé sans fil

les utilisateurs finaux interagissent avec la fonctionnalité de réseau hébergé sans fil dans Windows à l’aide d’applications tierces ou de commandes **netsh** . il n’existe actuellement aucune interface utilisateur native pour la configuration ou la gestion du réseau hébergé sans fil sur Windows 7 ou sur Windows Server 2008 R2 avec le Service de réseau local sans fil installé.

Les applications tierces et les commandes **netsh** sont basées sur l’utilisation des fonctions de réseau public sans fil hébergées. cet ensemble de fonctions fournit un ensemble complet de fonctionnalités permettant de gérer le réseau hébergé sans fil sur Windows 7 et sur Windows Server 2008 R2 avec le Service de réseau local sans fil installé.

La liste suivante répertorie les fonctions de réseau hébergé sans fil et les actions courantes du point de vue de l’utilisateur final que la fonction à utiliser pour :



| Fonctions utilisées                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Description                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WlanHostedNetworkForceStart_____WlanHostedNetworkStartUsing"></span><span id="wlanhostednetworkforcestart_____wlanhostednetworkstartusing"></span><span id="WLANHOSTEDNETWORKFORCESTART_____WLANHOSTEDNETWORKSTARTUSING"></span>[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart), [ **WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)<br/>                                                                                                                                                                                                                                                       | Démarrez le réseau hébergé sans fil.<br/>                                                                                                                 |
| <span id="WlanHostedNetworkForceStop__WlanHostedNetworkStopUsing"></span><span id="wlanhostednetworkforcestop__wlanhostednetworkstopusing"></span><span id="WLANHOSTEDNETWORKFORCESTOP__WLANHOSTEDNETWORKSTOPUSING"></span>[**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop), [ **WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)<br/>                                                                                                                                                                                                                                                                          | Arrêtez le réseau hébergé sans fil.<br/>                                                                                                                  |
| <span id="WlanHostedNetworkInitSettings__WlanHostedNetworkSetSecondaryKey__WlanHostedNetworkRefreshSecuritySettings"></span><span id="wlanhostednetworkinitsettings__wlanhostednetworksetsecondarykey__wlanhostednetworkrefreshsecuritysettings"></span><span id="WLANHOSTEDNETWORKINITSETTINGS__WLANHOSTEDNETWORKSETSECONDARYKEY__WLANHOSTEDNETWORKREFRESHSECURITYSETTINGS"></span>[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings), [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey), [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)<br/> | Configurez les paramètres de réseau hébergé sans fil (modifiez le SSID, modifiez la clé secondaire ou demandez la régénération de la clé primaire).<br/>            |
| <span id="WlanHostedNetworkQueryStatus__WlanHostedNetworkQuerySecondaryKey__WlanHostedNetworkQueryProperty"></span><span id="wlanhostednetworkquerystatus__wlanhostednetworkquerysecondarykey__wlanhostednetworkqueryproperty"></span><span id="WLANHOSTEDNETWORKQUERYSTATUS__WLANHOSTEDNETWORKQUERYSECONDARYKEY__WLANHOSTEDNETWORKQUERYPROPERTY"></span>[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus), [**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey), [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)<br/>                                              | Interrogez les paramètres et les informations du réseau hébergé sans fil (Status, SSID, clé secondaire, clé primaire ou une liste des appareils actuellement connectés).<br/> |



 

Les commandes **netsh** sont destinées à être utilisées par des utilisateurs ou administrateurs avancés.

*Netsh.exe* possède de nombreuses sous-commandes pour le réseau local sans fil. La liste complète des options pour **netsh** et le réseau local sans fil est disponible à partir de l’invite de commandes en tapant ce qui suit :

**netsh wlan/ ?**

La documentation sur toutes les commandes netsh pour réseau local sans fil est également disponible en ligne sur TechNet. Pour plus d’informations, consultez [commandes netsh pour réseau local sans fil (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

Voici quelques-unes des commandes **netsh** couramment utilisées avec pour le réseau local sans fil et le réseau hébergé sans fil, bien que d’autres combinaisons de commandes soient prises en charge :



| Commande                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Description                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="netsh_wlan_start_hostednetwork"></span><span id="NETSH_WLAN_START_HOSTEDNETWORK"></span>**netsh wlan Start hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                     | Démarrez le réseau hébergé sans fil.<br/>              |
| <span id="netsh_wlan_stop_hostednetwork"></span><span id="NETSH_WLAN_STOP_HOSTEDNETWORK"></span>**netsh wlan Stop hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                        | Arrêtez le réseau hébergé sans fil.<br/>               |
| <span id="netsh_wlan_set_hostednetwork__mode__allow_disallow"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__MODE__ALLOW_DISALLOW"></span>**netsh wlan set hostednetwork \[ mode = \] autoriser l' \| interdiction**<br/>                                                                                                                                                                                                                                                                      | Activez ou désactivez le réseau hébergé sans fil.<br/>  |
| <span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyUsage__persistent_temporary_"></span><span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyusage__persistent_temporary_"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__SSID___SSID___KEY___PASSPHRASE___KEYUSAGE__PERSISTENT_TEMPORARY_"></span>**netsh wlan set hostednetwork \[ SSID = \] &lt; SSID &gt; \[ clé = \] &lt; phrase secrète &gt; \[ utilisation = \] persistante \| temporaire** <br/> | Configurez les paramètres de réseau hébergé sans fil.<br/> |
| <span id="netsh_wlan_refresh_hostednetwork___data___key"></span><span id="NETSH_WLAN_REFRESH_HOSTEDNETWORK___DATA___KEY"></span>**netsh wlan Refresh hostednetwork \[ Data = \] clé**<br/>                                                                                                                                                                                                                                                                                       | Actualisez la clé de réseau hébergé sans fil.<br/>        |
| <span id="netsh_wlan_show_hostednetwork___setting__security_"></span><span id="NETSH_WLAN_SHOW_HOSTEDNETWORK___SETTING__SECURITY_"></span>**netsh wlan Show hostednetwork \[ \[ paramètre = \] sécurité\]**<br/>                                                                                                                                                                                                                                                                     | Affichez les informations sur le réseau hébergé sans fil.<br/>    |
| <span id="netsh_wlan_show_settings"></span><span id="NETSH_WLAN_SHOW_SETTINGS"></span>**paramètres netsh wlan Show**<br/>                                                                                                                                                                                                                                                                                                                                                       | Affichez les paramètres globaux du réseau local sans fil.<br/>           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du partage de connexion Internet et d’un réseau hébergé sans fil](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[Exemple de réseau hébergé sans fil](wireless-hosted-network-sample.md)
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

 

 
