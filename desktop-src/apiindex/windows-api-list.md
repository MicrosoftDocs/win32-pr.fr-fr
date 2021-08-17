---
description: liste du contenu de référence pour l’API Windows.
ms.assetid: 9CA123F9-92F1-4761-9468-266DA422F70E
title: Index des API Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e61a3f738905e98ad9cd1db85dbaa1746d7c613b1cc5b628805bcc3ddbea74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737636"
---
# <a name="windows-api-index"></a>Index des API Windows

la liste suivante répertorie le contenu de référence pour l’interface de programmation d’applications (API) Windows pour les applications de bureau et serveur.

à l’aide de l’API Windows, vous pouvez développer des applications qui s’exécutent correctement sur toutes les versions de Windows tout en tirant parti des fonctionnalités et des fonctionnalités propres à chaque version. (Notez que l’API Win32 s’appelait auparavant. le nom Windows API reflète plus précisément ses racines en Windows 16 bits et sa prise en charge sur la Windows 64 bits.)

## <a name="user-interface"></a>Interface utilisateur

l’API d’interface utilisateur Windows créer et utiliser des fenêtres pour afficher la sortie, demander une entrée utilisateur et effectuer les autres tâches qui prennent en charge l’interaction avec l’utilisateur. La plupart des applications créent au moins une fenêtre.

-   [Accessibilité](../winauto/windows-accessibility-features-reference.md)
-   [Gestionnaire de fenêtrage (DWM)](../dwm/reference.md)
-   [Services de globalisation](../intl/globalization-services.md)
-   [Haute résolution](../hidpi/high-dpi-reference.md)
-   [interface utilisateur multilingue (MUI)](../intl/multilingual-user-interface-reference.md)
-   [National Language Support (NLS)](../intl/national-language-support-reference.md)
-   [Éléments de l’interface utilisateur](../devnotes/user-interface.md):

    -   [Boutons](../controls/bumper-button-button-control-reference.md)
    -   [Signes](../menurc/caret-functions.md)
    -   [Zones de liste modifiable](../controls/bumper-combobox-combobox-control-reference.md)
    -   [Boîtes de dialogue communes](../dlgbox/common-dialog-box-reference.md)
    -   [Contrôles communs](../controls/individual-control-info.md)
    -   [Curseurs](../menurc/cursor-reference.md)
    -   [Boîtes de dialogue](../dlgbox/dialog-box-reference.md)
    -   [Contrôles d’édition](../controls/bumper-edit-control-edit-control-reference.md)
    -   [Contrôles Header](../controls/bumper-header-control-header-control-reference.md)
    -   [Icônes](../menurc/icon-reference.md)
    -   [Raccourcis clavier](../menurc/keyboard-accelerator-reference.md)
    -   [Zones de liste](../controls/bumper-list-box-list-box-control-reference.md)
    -   [Contrôles de liste](../controls/bumper-list-view-list-view-control-reference.md)
    -   [Menus](../menurc/menu-reference.md)
    -   [Barres de progression](../controls/bumper-progress-bar-progress-bar-control-reference.md)
    -   [Feuilles de propriétés](../controls/bumper-property-sheet-property-sheets-reference.md)
    -   [Contrôles RichEdit](../controls/bumper-rich-edit-rich-edit-control-reference.md)
    -   [Barres de défilement](../controls/bumper-scroll-bar-scroll-bars-reference.md)
    -   [Contrôles statiques](../controls/bumper-static-control-static-control-reference.md)
    -   [Chaînes](../menurc/string-reference.md)
    -   [Barres d'outils](../controls/bumper-toolbar-toolbar-control-reference.md)
    -   [Info-bulles](../controls/bumper-tooltip-tooltip-control-reference.md)
    -   [Trackbars](../controls/bumper-trackbar-trackbar-control-reference.md)
    -   [Contrôles d’arborescence](../controls/bumper-tree-view-tree-view-control-reference.md)

-   [Windows Gestionnaire d’animations](../uianimation/windows-animation-reference.md)
-   [Windows Infrastructure du ruban](../windowsribbon/windowsribbon-reference-entry.md)

## <a name="windows-environment-shell"></a>environnement d’Windows (Shell)

-   [Windows Système de propriétés](../properties/property-system-reference.md)
-   [Windows Shell](/previous-versions/windows/desktop/legacy/ff521731(v=vs.85))
-   [Windows Search](../search/-search-reference-entry-page.md)
-   [Consoles](/windows/console/console-reference)

## <a name="user-input-and-messaging"></a>Entrée d’utilisateur et messagerie

-   [Interaction de l’utilisateur](../user-interaction.md)
    -   [Manipulation directe](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)
    -   [Entrée d’encre](/previous-versions/windows/desktop/input_ink/input-ink-portal)
    -   [Configuration des commentaires en entrée](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
    -   [Contexte d’interaction](/previous-versions/windows/desktop/input_intcontext/interaction-context-portal)
    -   [Pile d’entrée du périphérique pointeur](/previous-versions/windows/desktop/input_pointerdevice/pointer-device-stack-portal)
    -   [Messages d’entrée de pointeur et notifications](/previous-versions/windows/desktop/inputmsg/messages-and-notifications)
    -   [Entrée du contrôleur radial](/previous-versions/windows/desktop/input_radial/radialcontroller-portal)
    -   [Text Services Framework](../tsf/text-services-framework.md)
    -   [Test d’atteinte tactile](/previous-versions/windows/desktop/input_touchhittest/touch-hit-testing-portal)
    -   [Injection tactile](/previous-versions/windows/desktop/input_touchinjection/touch-injection-portal)
-   [Interaction de l’utilisateur hérité](../legacy-user-interaction-features.md)
    -   [Entrée tactile](../wintouch/windows-touch-portal.md)
    -   [Entrée au clavier](../inputdev/keyboard-input.md)
    -   [Entrée de la souris](../inputdev/mouse-input.md)
    -   [Entrée brute](../inputdev/raw-input.md)
-   [Windows et Messages](../winmsg/windowing.md):

    -   [Messages et files d’attente de messages](../winmsg/message-and-message-queue-reference.md)
    -   [Windows](../winmsg/window-reference.md)
    -   [classes de fenêtre](../winmsg/window-class-reference.md)
    -   [Procédures de fenêtre](../winmsg/window-procedure-reference.md)
    -   [Minuteurs](../winmsg/timer-reference.md)
    -   [Propriétés de la fenêtre](../winmsg/window-property-reference.md)
    -   [Hooks](../winmsg/hook-reference.md)

## <a name="data-access-and-storage"></a>Accès aux données et stockage

-   [Service de transfert intelligent en arrière-plan (BITS)](../bits/bits-reference.md)
-   [Sauvegarde des données](../backup/backup.md)
    -   [Sauvegarde](../backup/backup-reference.md)
    -   [Déduplication des données](/previous-versions/windows/desktop/dedup/data-deduplication-api-reference)
    -   [Cliché instantané des volumes](../vss/volume-shadow-copy-reference.md)
    -   [Sauvegarde Windows Server](/previous-versions/windows/desktop/wsb/windows-server-backup-api-interfaces)
-   [Exchange de données](../dataxchg/data-exchange.md):

    -   [Presse-papiers](../dataxchg/clipboard-reference.md)
    -   [échange dynamique de données (DDE)](../dataxchg/dynamic-data-exchange-reference.md)
    -   [gestion des échange dynamique de données (DDEML)](../dataxchg/dynamic-data-exchange-management-library-reference.md)

-   [Gestion de répertoires](../fileio/directory-management-reference.md)
-   [Gestion des disques](../fileio/disk-management-reference.md)
-   [Système de fichiers DFS](/previous-versions/windows/desktop/dfs/distributed-file-system-reference)
-   [Réplication du système de fichiers DFS](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes)
-   [moteur de Stockage Extensible](../extensible-storage-engine/extensible-storage-engine-reference.md)
-   [Fichiers et e/s (système de fichiers local)](../fileio/file-management-reference.md)
-   [API de la bibliothèque de découverte iSCSI](/previous-versions/windows/desktop/iscsidisc/iscsi-discovery-library-reference)
-   [Fichiers hors connexion](/previous-versions/windows/desktop/offlinefiles/offline-files-reference)
-   [Packaging](/previous-versions/windows/desktop/opc/packaging-programming-reference)
-   [Compression différentielle à distance](/previous-versions/windows/desktop/rdc/remote-differential-compression-reference)
-   [NTFS transactionnel](../fileio/transactional-ntfs-reference.md)
-   [Gestion des volumes](../fileio/volume-management-reference.md)
-   [Disque dur virtuel (VHD)](/previous-versions/windows/desktop/legacy/dd323700(v=vs.85))
-   [Gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Windows Data Access Components](/previous-versions/windows/desktop/legacy/aa968814(v=vs.85))
    -   [Microsoft ODBC (Open Database Connectivity)](/sql/odbc/reference/syntax/odbc-reference)
    -   [Microsoft OLE DB](/previous-versions/windows/desktop/ms718050(v=vs.85))
    -   [Microsoft ActiveX Data Objects (ADO)](/sql/ado/reference/ado-programmer-s-reference)

## <a name="diagnostics"></a>Diagnostics

L’API [Diagnostics](/previous-versions//bb648685(v=vs.85)) vous permet de résoudre les problèmes liés aux applications ou au système et de surveiller les performances.

-   [Récupération et redémarrage d’application](../recovery/application-recovery-and-restart-reference.md)
-   [Débogage](../debug/debugging-reference.md)
-   [Gestion des erreurs](../debug/error-handling-reference.md)
-   [Journalisation des événements](../eventlog/event-logging-reference.md)
-   [Suivi d’événements](../etw/event-tracing-reference.md)
-   [Profilage des compteurs matériels (HCP)](/previous-versions/windows/desktop/hcp/hcp-reference)
-   [Network Diagnostics Framework (NDF)](../ndf/ndf-reference.md)
-   [Moniteur réseau](../netmon2/reference.md)
-   [Compteurs de performance](../perfctrs/performance-counters-reference.md)
-   [Journaux et alertes de performance (PLA)](/previous-versions/windows/desktop/pla/performance-logs-and-alerts-reference)
-   [Capture d’instantanés de processus](/previous-versions/windows/desktop/proc_snap/process-snapshotting-reference)
-   [État du processus (PSAPI)](../psapi/psapi-reference.md)
-   [Gestion structurée des exceptions](../debug/structured-exception-handling-reference.md)
-   [Moniteur système](../sysmon/system-monitor-reference.md)
-   [Wait Chain Traversal](../debug/wait-chain-traversal.md)
-   [Rapport d’erreurs Windows](../wer/wer-reference.md)
-   [Journal des événements Windows](../wes/windows-event-log-reference.md)
-   [Plateforme de résolution des problèmes Windows](/previous-versions/windows/desktop/wintt/windows-troubleshooting-reference)

## <a name="graphics-and-multimedia"></a>Graphisme et multimédia

Les API [Graphics, Multimedia,](/previous-versions//aa969176(v=vs.85)) [audio et Video](../audio-and-video.md) permettent aux applications d’incorporer du texte mis en forme, des graphiques, de l’audio et des vidéos.

-   [Audio principal](../coreaudio/programming-reference.md)
-   [Direct2D](../direct2d/reference.md)
-   [DirectComposition](../directcomp/reference.md)
-   [DirectShow](../directshow/directshow-reference.md)
-   [DirectWrite](../directwrite/reference.md)
-   [DirectX](../directx-sdk--august-2009-.md)
-   [Graphics Device Interface (GDI)](../gdi/windows-gdi.md)
-   [GDI+](../gdiplus/-gdiplus-class-gdi-reference.md)
-   [Diffusion multimédia en continu](../mediastreaming/media-streaming-api-portal.md)
-   [Microsoft Media Foundation](../medfound/media-foundation-programming-reference.md)
-   [Technologies Microsoft TV](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-application-interface)
-   [Technologie](../opengl/opengl-reference.md)
-   [Configuration de l’analyse](../monitor/monitor-configuration-reference.md)
-   [Moniteurs multiples](../gdi/multiple-display-monitors-reference.md)
-   [Acquisition d’images](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [Système de couleurs Windows](../wcs/reference.md)
-   [Composant Imagerie Windows (WIC)](../wic/-wic-codec-reference.md)
-   [Windows Codec audio et vidéo multimédia et DSP](/previous-versions//dd443208(v=vs.85))
-   [Windows Media Center](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [Format Windows Media](../wmformat/programming-reference.md)
-   [Windows Services de partage de la bibliothèque multimédia](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal)
-   [Lecteur Windows Media](../wmp/windows-media-player-object-model-reference.md)
-   [Services Windows Media](/previous-versions/windows/desktop/dd893580(v=vs.85))
-   [Windows Movie Maker](/previous-versions/windows/desktop/wmmdvdm/windows-movie-maker-apis)
-   [Windows Media](../multimedia/multimedia-reference.md)

## <a name="devices"></a>Appareils

-   [AllJoyn](/previous-versions/windows/desktop/alljoyn/alljoyn-api-portal)
-   [Ressources de communication](../devio/communications-reference.md)
-   [Accès de l’appareil](/previous-versions/windows/desktop/deviceaccess/device-access-api-c---programming-reference)
-   [Gestion des appareils](../devio/device-management-reference.md)
-   [Stockage étendu](/previous-versions/windows/desktop/enstor/enhanced-storage-reference)
-   [Détection de fonction](/previous-versions/windows/desktop/fundisc/function-discovery-reference)
-   [Mastérisation des images](../imapi/imapi-reference.md)
-   [Lieu](../locationapi/windows-location-programming-reference.md)
-   [Base de données d’association PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x-association-database-reference)
-   [Impression](/windows-hardware/drivers/print/introduction-to-printing)
    -   [Spouleur d’impression](../printdocs/printing-and-print-spooler-reference.md)
    -   [Imprimer le package de document](../printdocs/tailored-app-printing-api.md)
    -   [Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
    -   [Imprimer le ticket](../printdocs/print-ticket-api.md)
    -   [Impression XPS](../printdocs/xpsprint-api.md)
-   [Détecteurs](../sensorsapi/sensor-api-programming-reference.md)
-   [Service de notification d’événements système (SENS)](../sens/sens-reference.md)
-   [Aide sur l’outil](../toolhelp/tool-help-reference.md)
-   [UPnP](../upnp/universal-plug-and-play-start-page.md)
-   [Services Web sur les appareils](../wsdapi/web-services-for-devices-reference.md)
-   [Acquisition d’image Windows (WIA)](../wia/-wia-reference.md)
-   [Windows Gestionnaire de périphériques de média](../wmdm/programming-reference.md)
-   [Windows Appareils mobiles](../wpd_sdk/programming-reference.md)

## <a name="system-services"></a>Services système

Les API des [services système](/previous-versions//aa969179(v=vs.85)) permettent aux applications d’accéder aux ressources de l’ordinateur et aux fonctionnalités du système d’exploitation sous-jacent, telles que la mémoire, les systèmes de fichiers, les périphériques, les processus et les threads.

-   [COM](../com/reference.md)
-   [COM+](../cossdk/com--reference.md)
-   [API de compression](../cmpapi/-compression-portal.md)
-   [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms686108(v=vs.85))
-   [Bibliothèques de liens dynamiques (dll)](../dlls/dynamic-link-library-functions.md)
-   [Aide API](/previous-versions/windows/desktop/helpapi/help-api-reference)
-   [Communications entre processus](../ipc/interprocess-communications.md):
    -   [Boîtes](../ipc/mailslot-functions.md)
    -   [Canaux](../ipc/pipe-functions.md)
-   [Gestionnaire de transactions KTM (Kernel Transaction Manager)](../ktm/ktm-reference.md)
-   [Gestion de la mémoire](../memory/memory-management-reference.md)
-   [Enregistreur d’opérations](/previous-versions/windows/desktop/oprec/-operation-portal)
-   [Gestion de l’alimentation](../power/power-management-reference.md)
-   [Services Bureau à distance](../termserv/terminal-services-reference.md)
-   [Processus](../procthread/process-and-thread-reference.md)
-   [Services](../services/service-reference.md)
-   [Synchronisation](../sync/synchronization-reference.md)
-   [Threads](../procthread/process-and-thread-reference.md)
-   [Windows Partage de bureau](/previous-versions/windows/desktop/rdp/windows-desktop-sharing-reference)
-   [Windows System Information](../sysinfo/windows-system-information.md)
    -   [Handle et objets](../sysinfo/handle-and-object-functions.md)
    -   [Registre](../sysinfo/registry-reference.md)
    -   [Time](../sysinfo/time-reference.md)
    -   [Fournisseur de temps](../sysinfo/time-provider-reference.md)

## <a name="security-and-identity"></a>Sécurité et identité

Les API de [sécurité et d’identité](../devnotes/security.md) permettent l’authentification par mot de passe à l’ouverture de session, la protection discrétionnaire pour tous les objets système partageables, le contrôle d’accès privilégié, la gestion des droits et l’audit de sécurité.

-   [Authentification](../secauthn/authentication-reference.md)
-   [Autorisation](../secauthz/authorization-reference.md)
-   [Inscription de certificats](../seccertenroll/certificate-enrollment-api-reference.md)
-   [Cryptographie](../seccrypto/cryptography-reference.md)
-   [CNG (Cryptography Next Generation)](../seccng/cng-reference.md)
-   [Services d'annuaire](/previous-versions//ms682458(v=vs.85))
    -   [Services de domaine Active Directory](../ad/active-directory-domain-services-reference.md)
    -   [Interfaces de service Active Directory (ADSI)](../adsi/adsi-reference.md)
-   [Protocole EAP (Extensible Authentication Protocol)](../eap/extensible-authentication-protocol-reference.md)
-   [Hôte de protocole d’authentification extensible (EAPHost)](../eaphost/about-eap-host.md)
-   [Gestion des mots de passe MS-CHAP](/previous-versions/windows/desktop/mschap/ms-chap-password-management-reference)
-   [Protection d’accès réseau (NAP)](../nap/nap-reference.md)
-   [Extensions serveur NPS (Network Policy Server)](../nps/ias-internet-authentication-service-reference.md)
-   [Contrôle parental](../parcon/parental-controls-reference.md)
-   [Fournisseurs WMI de sécurité](../secprov/security-wmi-providers-reference.md)
-   [Services de base du module de plateforme sécurisée (TBS)](../tbs/tbs-reference.md)
-   [Windows Biometric Framework](../secbiomet/biometric-service-api-reference.md)

## <a name="application-installation-and-servicing"></a>Installation d’application et maintenance

-   [Explorateur des jeux](/previous-versions/windows/desktop/legacy/ee415251(v=vs.85))
-   [Assemblys côte à côte](../sbscs/side-by-side-assemblies-reference.md)
-   [API d’empaquetage, de déploiement et de requête](../appxpkg/api-reference.md
)
-   [Licence de développeur](../devlic/developer-license-apis.md)
-   [Gestionnaire de redémarrage](../rstmgr/restart-manager-reference.md)
-   [Windows Installer](../msi/windows-installer-portal.md)

## <a name="system-admin-and-management"></a>Administration système et gestion

Les interfaces d' [administration système](../srvnodes/system-administration.md) vous permettent d’installer, de configurer et de traiter des applications ou des systèmes.

-   [Fournisseur WMI Données de configuration de démarrage (BCD)](/previous-versions/windows/desktop/bcd/bcd-reference)
-   [Clusters de basculement](/previous-versions/windows/desktop/mscs/failover-cluster-apis-portal)
-   [Gestionnaire de ressources du serveur de fichiers](/previous-versions/windows/desktop/fsrm/fsrm-reference)
-   [Stratégie de groupe](/previous-versions/windows/desktop/Policy/group-policy-reference)
-   [Microsoft Management Console (MMC) 2,0](/previous-versions/windows/desktop/mmc/mmc-reference)
-   [NetShell](/previous-versions/windows/desktop/netshell/netshell-reference)
-   [Paramètres Infrastructure de gestion](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [Journalisation de l’inventaire logiciel](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
-   [Gestion des licences des logiciels](/previous-versions/windows/desktop/secslapi/software-licensing-api-reference)
-   [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md)
-   [Paramètres Infrastructure de gestion](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [Restauration du système](../sr/system-restore-portal.md)
-   [Arrêt du système](../shutdown/system-shutdown.md)
-   [Planificateur de tâches](../taskschd/task-scheduler-start-page.md)
-   [Journalisation des accès utilisateur](/previous-versions/windows/desktop/ual/user-access-logging-reference)
-   [Windows Virtual PC](../vpc/virtual-pc-reference.md)
-   [Microsoft Virtual Server](/previous-versions/windows/desktop/msvs/microsoft-virtual-server-reference)
-   [Fournisseur d’équilibrage de charge réseau](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-reference)
-   [Windows Defender WMI v2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
-   [Windows Services de déploiement](../wds/windows-deployment-services-portal.md)
-   [Windows Genuine Advantage](/previous-versions/windows/desktop/wingen/windows-genuine-advantage-api-functions)
-   [Windows Infrastructure de gestion](/previous-versions/windows/desktop/wmi_v2/wmi-reference)
-   [Windows Management Instrumentation (WMI)](../wmisdk/wmi-reference.md)
-   [Gestion à distance de Windows](../winrm/portal.md)
-   [Windows Protection des ressources](../wfp/windows-resource-protection-portal.md)
-   [Windows Server Update Services](/previous-versions/windows/desktop/ms744624(v=vs.85))
-   [Windows Outil d’évaluation du système](../winsat/winsat-reference.md)
-   [Agent Windows Update](../wua_sdk/portal-client.md)

## <a name="networking-and-internet"></a>Mise en réseau et Internet

Les API de [mise en réseau](../devnotes/networking.md) permettent la communication entre les applications sur un réseau. Vous pouvez également créer et gérer l’accès à des ressources partagées, telles que des répertoires et des imprimantes réseau.

-   [DNS (Domain Name System)](../dns/dns-reference.md)
-   [Protocole DHCP (Dynamic Host Configuration Protocol)](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
-   [Service de télécopie](/previous-versions/windows/desktop/fax/-mfax-fax-service-reference)
-   [Assistant Connexion Internet](/previous-versions/windows/desktop/get_connected/get-connected-wizard-api-reference)
-   [Serveur HTTP](../http/http-server-api-reference.md)
-   [Partage et pare-feu de connexion Internet](/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference)
-   [Assistance IP](../iphlp/ip-helper-function-reference.md)
-   [Pare-feu de connexion Internet IPv6](/previous-versions/windows/desktop/ics/ipv6-firewall-configuration-reference)
-   [Base d’informations de gestion](/previous-versions/windows/desktop/mib/management-information-base-reference)
-   [Message Queuing (MSMQ)](/previous-versions/windows/desktop/legacy/ms700112(v=vs.85))
-   [Protocole MADCAP (Multicast Address Dynamic Client Allocation Protocol)](/previous-versions/windows/desktop/madcap/madcap-reference)
-   [Traduction d’adresses réseau (NAT)](/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference)
-   [Gestionnaire de listes de réseaux (NLM)](../nla/network-list-manager-api-reference.md)
-   [Gestion du réseau](../netmgmt/network-management-reference.md)
-   [Gestion du partage réseau](../netshare/network-share-management-reference.md)
-   [Pair à pair](../p2psdk/portal.md)
-   [Qualité de service (QOS)](/previous-versions/windows/desktop/qos/qos-reference)
-   [Appel de procédure distante](../rpc/reference.md)
-   [Service de routage et d’accès à distance (RAS)](../rras/portal.md)
-   [Simple Network Management Protocol (SNMP)](../snmp/snmp-reference.md)
-   [Gestion SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)
-   [Interfaces de programmation d’applications de téléphonie (TAPI)](../tapi/telephony-application-programming-interfaces.md)
-   [WebDAV](../webdav/webdav-api-reference.md)
-   [Composant du protocole WebSocket](../websock/web-socket-protocol-component-api-portal.md)
-   Mise en réseau sans fil :
    -   [Bluetooth](../bluetooth/bluetooth-reference.md)
    -   [IrDA](/previous-versions/windows/desktop/irda/irda-and-windows-sockets-reference)
    -   [Haut débit mobile](../mbn/mobile-broadband-networks-api-reference.md)
    -   [WiFi natif](../nativewifi/native-wifi-reference.md)
    -   [Windows Connect Now](../wcn/windows-connect-now-reference.md)
    -   [Gestionnaire de connexions Windows](../wcm/windows-connection-manager-reference.md)
-   [Plateforme de filtrage Windows](../fwp/fwp-reference.md)
-   [Pare-feu Windows avec fonctions avancées de sécurité](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference)
-   [Windows Services HTTP (WinHTTP)](../winhttp/winhttp-reference.md)
-   [Windows Internet (WinINet)](../wininet/wininet-reference.md)
-   [Windows Mise en réseau (WNet)](../wnet/windows-networking-reference.md)
-   [Windows Virtualisation de réseau](/previous-versions/windows/desktop/wnv/windows-network-virtualization-portal)
-   [Windows Plateforme RSS](/previous-versions/windows/desktop/ms684702(v=vs.85))
-   [Windows Sockets (Winsock)](../winsock/winsock-reference.md)
-   [Windows Services Web](../wsw/windows-web-services-reference.md)
-   [Requête étendue HTTP XML](/previous-versions/windows/desktop/ixhr2/ixmlhttprequest2-portal)

## <a name="deprecated-or-legacy-apis"></a>API déconseillées ou héritées

voici les technologies et les api qui sont obsolètes ou qui ont été remplacées ou déconseillées dans les systèmes d’exploitation client et serveur de Windows.

-   [DirectMusic](/previous-versions/ms807133(v=msdn.10))
-   [DirectSound](/previous-versions/windows/desktop/ee416975(v=vs.85))
-   Le [Kit de développement logiciel (SDK) Microsoft UDDI](/previous-versions/windows/desktop/aa966237(v=bts.10)) est désormais fourni avec [Microsoft BizTalk Server](/previous-versions/bb905520(v=msdn.10)).
-   [échange dynamique de données réseau (DDE)](../ipc/network-dde-reference.md)
-   [Service d’Installation à distance](/previous-versions/windows/it-pro/windows-server-2003/cc786442(v=ws.10)): utilisez à la place des [Services de déploiement Windows](../wds/windows-deployment-services-portal.md) .
-   [Service de disque virtuel (VDS)](../vds/vds-reference.md): utilisez à la place [Windows gestion Stockage](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal) .
-   Services Terminal Server : utilisez [services Bureau à distance](../termserv/terminal-services-reference.md).
-   [Windows Media Rights Manager](/previous-versions//bb614742(v=vs.85))
-   [messagerie Windows (mapi)](/previous-versions/windows/desktop/windowsmapi/mapi-stub-library-and-simple-mapi): utilisez à la place [Office mapi](/previous-versions/office/developer/office-2007/cc765775(v=office.12)) .
-   [Windows Gadget Platform](/previous-versions/windows/desktop/gadgetplatform/windows-gadget-platform-portal): créez des applications UWP à la place.
-   [Windows Sidebar](/previous-versions/windows/desktop/sidebar/-sidebar-ref-entry): créer des applications UWP à la place.
-   [Windows SideShow](/previous-versions//ms744179(v=vs.85)): aucun remplacement.
-   [Effets bitmap WPF](/previous-versions/windows/desktop/wibe/-wibe-about-bitmapeffects)
