---
description: À compter de Windows Vista, les éléments du panneau de configuration inclus avec Windows reçoivent un nom canonique qui peut être utilisé dans un appel d’API ou une instruction de ligne de commande pour lancer par programmation cet élément.
ms.assetid: A02DFC9F-646D-40d8-901C-7239A820DE2C
title: Noms canoniques des éléments du panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55fc360b0d3db0f85a057977d1898c59d09d5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951021"
---
# <a name="canonical-names-of-control-panel-items"></a>Noms canoniques des éléments du panneau de configuration

À compter de Windows Vista, les éléments du panneau de configuration inclus avec Windows reçoivent un nom canonique qui peut être utilisé dans un [appel d’API ou une instruction de ligne de commande](executing-control-panel-items.md) pour lancer par programmation cet élément. À compter de Windows 7 et de Windows Server 2008 R2, les noms canoniques peuvent être utilisés dans une stratégie de groupe pour masquer des éléments spécifiques du panneau de configuration. Cette rubrique fournit des détails sur chaque élément du panneau de configuration : le nom canonique, le GUID, le nom du module et les versions de système d’exploitation qui reconnaissent le nom canonique.

> [!Note]  
> Les noms canoniques des éléments du panneau de configuration ne sont pas pris en charge avant Windows Vista.

 

-   [Noms canoniques du panneau de configuration](#control-panel-canonical-names)
-   [Noms canoniques du panneau de configuration déconseillés](#deprecated-control-panel-canonical-names)
-   [Utilisation de noms canoniques dans les stratégie de groupe](#using-canonical-names-in-local-group-policy)
-   [Remarques](#remarks)

## <a name="control-panel-canonical-names"></a>Noms canoniques du panneau de configuration

Points à retenir lors de l’utilisation de ces valeurs :

-   Par définition, les noms canoniques ne changent pas en fonction de la langue du système. ils sont toujours en anglais, même si la langue du système ne l’est pas.
-   Tous les éléments du panneau de configuration ne sont pas présents dans toutes les variétés de Windows.
-   Certains éléments du panneau de configuration ne s’affichent que si le matériel approprié est détecté sur le système.
-   Les tiers peuvent également ajouter des éléments du panneau de configuration. Les noms canoniques répertoriés ici ne concernent que les éléments du panneau de configuration qui sont inclus avec Windows.

Voici les éléments du panneau de configuration disponibles dans Windows 8.1 :

-   [Centre de maintenance](#action-center)
-   [Outils d’administration](#administrative-tools)
-   [Exécution automatique](#autoplay)
-   [Périphériques biométriques](#biometric-devices)
-   [Chiffrement de lecteur BitLocker](#bitlocker-drive-encryption)
-   [Gestion des couleurs](#color-management)
-   [Gestionnaire d’informations d’identification](#credential-manager)
-   [Date et heure](#date-and-time)
-   [Programmes par défaut](#default-programs)
-   [Gestionnaire de périphériques](#device-manager)
-   [Périphériques et imprimantes](#devices-and-printers)
-   [Affichage](#display)
-   [Options d’ergonomie](#ease-of-access-center)
-   [Contrôle parental](#family-safety)
-   [Historique des fichiers](#file-history)
-   [Options des dossiers](#folder-options)
-   [Polices](#fonts)
-   [HomeGroup](#homegroup)
-   [Options d’indexation](#indexing-options)
-   [Infrarouge](#infrared)
-   [Options Internet](#internet-options)
-   [Initiateur iSCSI](#iscsi-initiator)
-   [Serveur iSNS](#isns-server)
-   [Clavier](#keyboard)
-   [Paramètres d’emplacement](#location-settings)
-   [Souris](#mouse)
-   [MPIOConfiguration](#mpioconfiguration)
-   [Centre Réseau et partage](#network-and-sharing-center)
-   [Icônes de la zone de notification](#notification-area-icons)
-   [Pen et Touch](#pen-and-touch)
-   [Personnalisation](#personalization)
-   [Téléphone et modem](#phone-and-modem)
-   [Options d’alimentation](#power-options)
-   [Programmes et fonctionnalités](#programs-and-features)
-   [Récupération](#recovery)
-   [Région](#region)
-   [Connexions aux programmes RemoteApp et aux services Bureau à distance](#remoteapp-and-desktop-connections)
-   [Son](#sound)
-   [Reconnaissance vocale](#speech-recognition)
-   [Espaces de stockage](#storage-spaces)
-   [Centre de synchronisation](#sync-center)
-   [Système](#system)
-   [Paramètres du Tablet PC](#tablet-pc-settings)
-   [Barre des tâches et navigation](#taskbar-and-navigation)
-   [Dépannage](#troubleshooting)
-   [TSAppInstall](#tsappinstall)
-   [Comptes d’utilisateur](#user-accounts)
-   [Mise à niveau express](#windows-anytime-upgrade)
-   [Windows Defender](#windows-defender)
-   [Pare-feu Windows](#windows-firewall)
-   [Centre de mobilité Windows](#windows-mobility-center)
-   [Windows To Go](#windows-to-go)
-   [Windows Update](#windows-update)
-   [Dossiers de travail](#work-folders)

### <a name="action-center"></a>Centre de maintenance

-   **Nom canonique**: Microsoft. ActionCenter
-   **GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\ActionCenterCPL.dll,-1
-   **Pages**

    | Nom de la page           | Opens                      |
    |---------------------|----------------------------|
    | MaintenanceSettings | Maintenance automatique      |
    | pageProblems        | Rapports de problèmes            |
    | pageReliabilityView | Moniteur de fiabilité        |
    | pageResponseArchive | Messages archivés          |
    | pageSettings        | Paramètres de signalement de problèmes |

    

     

### <a name="administrative-tools"></a>Outils d'administration

-   **Nom canonique**: Microsoft. AdministrativeTools
-   **GUID**: {D20EA4E1-3957-11D2-A40B-0C5020524153}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\shell32.dll,-22982

### <a name="autoplay"></a>Lecture automatique

-   **Nom canonique**: Microsoft. AutoPlay
-   **GUID**: {9C60DE1E-E5FC-40F4-A487-460851A8D915}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\autoplay.dll,-1

### <a name="biometric-devices"></a>Périphériques biométriques

-   **Nom canonique**: Microsoft. BiometricDevices
-   **GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\biocpl.dll,-1

### <a name="bitlocker-drive-encryption"></a>Chiffrement de lecteur BitLocker

-   **Nom canonique**: Microsoft. BitLockerDriveEncryption
-   **GUID**: {D9EF8727-CaC2-4e60-809e-86F80A666C91}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\fvecpl.dll,-1

### <a name="color-management"></a>Gestion des couleurs

-   **Nom canonique**: Microsoft. colormanagement
-   **GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\colorcpl.exe,-6

### <a name="credential-manager"></a>Gestionnaire d’informations d’identification

-   **Nom canonique**: Microsoft. CredentialManager
-   **GUID**: {1206F5F1-0569-412c-8FEC-3204630DFB70}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\Vault.dll,-1
-   **Pages**

    | Nom de la page                   | Opens               |
    |-----------------------------|---------------------|
    | ? SelectedVault = CredmanVault | Informations d’identification Windows |

    

     

### <a name="date-and-time"></a>Date et heure

-   **Nom canonique**: Microsoft. DateAndTime
-   **GUID**: {E2E7934B-DCE5-43c4-9576-7FE4F75E7480}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\timedate.cpl,-51
-   **Pages**

    | Nom de la page | Opens             |
    |-----------|-------------------|
    | 1         | Horloges supplémentaires |

    

     

### <a name="default-programs"></a>Programmes par défaut

-   **Nom canonique**: Microsoft. DefaultPrograms
-   **GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\sud.dll,-1
-   **Pages**

    | Nom de la page          | Opens                |
    |--------------------|----------------------|
    | pageDefaultProgram | Définir les programmes par défaut |
    | pageFileAssoc      | Définir des associations     |

    

     

### <a name="device-manager"></a>Gestionnaire de périphériques

-   **Nom canonique**: Microsoft. DeviceManager
-   **GUID**: {74246bfc-4C96-11D0-ABEF-0020af6b0b7a}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\devmgr.dll,-4

### <a name="devices-and-printers"></a>Périphériques et imprimantes

-   **Nom canonique**: Microsoft. DevicesAndPrinters
-   **GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\DeviceCenter.dll,-1000

### <a name="display"></a>Afficher

-   **Nom canonique**: Microsoft. Display
-   **GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\Display.dll,-1
-   **Pages**

    | Nom de la page | Opens             |
    |-----------|-------------------|
    | Paramètres  | Résolution d’écran |

    

     

### <a name="ease-of-access-center"></a>Options d’ergonomie

-   **Nom canonique**: Microsoft. EaseOfAccessCenter
-   **GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\accessibilitycpl.dll,-10
-   **Pages**

    | Nom de la page               | Opens                                                               |
    |-------------------------|---------------------------------------------------------------------|
    | pageEasierToClick       | Faciliter l’utilisation de la souris                                        |
    | pageEasierToSee         | Rendre l’ordinateur plus facile à voir                                     |
    | pageEasierWithSounds    | Utiliser du texte ou des alternatives visuelles pour les sons                          |
    | pageFilterKeysSettings  | Configurer des clés de filtre                                                  |
    | pageKeyboardEasierToUse | Faciliter l’utilisation du clavier                                     |
    | pageNoMouseOrKeyboard   | Utiliser l’ordinateur sans clavier ni souris                        |
    | pageNoVisual            | Utiliser l’ordinateur sans affichage                                  |
    | pageQuestionsCognitive  | Recevez des recommandations pour faciliter l’utilisation de votre ordinateur (cognitive) |
    | pageQuestionsEyesight   | Recevoir des recommandations pour faciliter l’utilisation de votre ordinateur (vue)  |

    

     

### <a name="family-safety"></a>Contrôle parental

-   **Nom canonique**: Microsoft. parentalcontrols
-   **GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\wpccpl.dll,-100
-   **Pages**

    | Nom de la page   | Opens                                  |
    |-------------|----------------------------------------|
    | pageUserHub | Choisir un utilisateur et configurer la sécurité de la famille |

    

     

### <a name="file-history"></a>Historique des fichiers

-   **Nom canonique**: Microsoft. FileHistory
-   **GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}
-   **Système d’exploitation pris en charge**: Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\fhcpl.dll,-52
-   L’historique des fichiers comprend une version plus récente de l’élément de sauvegarde et de restauration, mais ce nom canonique de l’ancien élément n’est pas remappé à l’historique des fichiers.

### <a name="folder-options"></a>Options des dossiers

-   **Nom canonique**: Microsoft. FolderOptions
-   **GUID**: {6DFD7C5C-2451-11D3-A299-00C04F8EF6AF}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\shell32.dll,-22985

### <a name="fonts"></a>Polices

-   **Nom canonique**: Microsoft. fonts
-   **GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\FontExt.dll,-8007

### <a name="homegroup"></a>Groupement résidentiel

-   **Nom canonique**: Microsoft. groupe résidentiel
-   **GUID**: {67CA7650-96E6-4FDD-BB43-A8E774F73A57}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\hgcpl.dll,-1

### <a name="indexing-options"></a>Options d’indexation

-   **Nom canonique**: Microsoft. IndexingOptions
-   **GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\srchadmin.dll,-601

### <a name="infrared"></a>Infrarouge

-   **Nom canonique**: Microsoft. infrarouge
-   **GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\irprops.cpl,-1

### <a name="internet-options"></a>Options Internet

-   **Nom canonique**: Microsoft. InternetOptions
-   **GUID**: {A3DD4F92-658A-410f-84FD-6FBBBEF2FFFE}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @C: \\ Windows \\ system32 \\inetcpl.cpl,-4312
-   **Pages**

    | Nom de la page | Opens       |
    |-----------|-------------|
    | 1         | Sécurité    |
    | 2         | Confidentialité     |
    | 3         | Content     |
    | 4         | Connexions |
    | 5         | Programmes    |
    | 6         | Avancé    |

    

     

### <a name="iscsi-initiator"></a>Initiateur iSCSI

-   **Nom canonique**: Microsoft. iSCSIInitiator
-   **GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\iscsicpl.dll,-5001

### <a name="isns-server"></a>Serveur iSNS

-   **Nom canonique**: Microsoft. iSNSServer
-   **GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\isnssrv.dll,-5005
-   Cet élément du panneau de configuration est visible uniquement dans les versions serveur de Windows.

### <a name="keyboard"></a>Clavier

-   **Nom canonique**: Microsoft. Keyboard
-   **GUID**: {725BE8F7-668E-4C7B-8F90-46BDB0936430}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\main.cpl,-102

### <a name="location-settings"></a>Paramètres d’emplacement

-   **Nom canonique**: Microsoft. LocationSettings
-   **GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}
-   **Système d’exploitation pris en charge**: Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\SensorsCpl.dll,-1

### <a name="mouse"></a>Souris

-   **Nom canonique**: Microsoft. Mouse
-   **GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\main.cpl,-100
-   **Pages**

    | Nom de la page | Opens           |
    |-----------|-----------------|
    | 1         | Pointeurs        |
    | 2         | Options du pointeur |
    | 3         | Roulette           |
    | 4         | Matériel        |

    

     

### <a name="mpioconfiguration"></a>MPIOConfiguration

-   **Nom canonique**: Microsoft. MPIOConfiguration
-   **GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\mpiocpl.dll,-1000
-   Cet élément du panneau de configuration est visible uniquement dans les versions serveur de Windows.

### <a name="network-and-sharing-center"></a>Centre Réseau et partage

-   **Nom canonique**: Microsoft. NetworkAndSharingCenter
-   **GUID**: {8E908FC9-BECC-40f6-915B-F4CA0E70D03D}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\netcenter.dll,-1
-   **Pages**

    | Nom de la page  | Opens                     |
    |------------|---------------------------|
    | Avancé   | Paramètres de partage avancés |
    | ShareMedia | Options de diffusion multimédia en continu   |

    

     

### <a name="notification-area-icons"></a>Icônes de la zone de notification

-   **Nom canonique**: Microsoft. NotificationAreaIcons
-   **GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\taskbarcpl.dll,-1

### <a name="pen-and-touch"></a>Pen et Touch

-   **Nom canonique**: Microsoft. PenAndTouch
-   **GUID**: {F82DF8F7-8B9F-442e-A48C-818EA735FF9B}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\tabletpc.cpl,-10103
-   **Pages**

    | Nom de la page | Opens       |
    |-----------|-------------|
    | 1         | Les raccourcis      |
    | 2         | Écriture manuscrite |

    

     

### <a name="personalization"></a>Personnalisation

-   **Nom canonique**: Microsoft. Personalization
-   **GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\themecpl.dll,-1
-   **Pages**

    | Nom de la page        | Opens                |
    |------------------|----------------------|
    | pageColorization | Couleur et apparence |
    | pageWallpaper    | Arrière-plan du Bureau   |

    

     

### <a name="phone-and-modem"></a>Téléphone et modem

-   **Nom canonique**: Microsoft. PhoneAndModem
-   **GUID**: {40419485-C444-4567-851A-2DD7BFA1684D}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\telephon.cpl,-1
-   La fenêtre lancée par cette valeur est intitulée « informations sur l’emplacement » dans les versions de Windows antérieures à Windows 8. L’interface utilisateur de l’élément est considérablement modifiée à partir de Windows 8.

### <a name="power-options"></a>Options d’alimentation

-   **Nom canonique**: Microsoft. PowerOptions
-   **GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\powercpl.dll,-1
-   **Pages**

    | Nom de la page          | Opens              |
    |--------------------|--------------------|
    | pageGlobalSettings | Paramètres système    |
    | pagePlanSettings   | Modifier les paramètres du plan |

    

     

### <a name="programs-and-features"></a>Programmes et fonctionnalités

-   **Nom canonique**: Microsoft. ProgramsAndFeatures
-   **GUID**: {7b81be6a-ce2b-4676-A29E-eb907a5126c5}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\appwiz.cpl,-159
-   **Pages**

    | Nom de la page                                | Opens             |
    |------------------------------------------|-------------------|
    | ::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD} | Mises à jour installées |

    

     

### <a name="recovery"></a>Récupération

-   **Nom canonique**: Microsoft. Recovery
-   **GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\recovery.dll,-101

### <a name="region"></a>Région

-   **Nom canonique**: Microsoft. RegionAndLanguage
-   **GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\intl.cpl,-1
-   La région et l’élément de langue trouvés dans Windows 7 ont été fractionnés à partir de Windows 8. Microsoft. RegionAndLanguage lance maintenant l’élément Region. Pour lancer l’élément de langue, utilisez [Microsoft. Language](#location-settings).
-   **Pages**

    | Nom de la page | Opens          |
    |-----------|----------------|
    | 1         | Emplacement       |
    | 2         | Administratif |

    

     

### <a name="remoteapp-and-desktop-connections"></a>Connexions aux programmes RemoteApp et aux services Bureau à distance

-   **Nom canonique**: Microsoft. RemoteAppAndDesktopConnections
-   **GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\tsworkspace.dll,-15300

### <a name="sound"></a>Son

-   **Nom canonique**: Microsoft. Sound
-   **GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\mmsys.cpl,-300

### <a name="speech-recognition"></a>Reconnaissance vocale

-   **Nom canonique**: Microsoft. SpeechRecognition
-   **GUID**: {58E3C745-D971-4081-9034-86E34B30836A}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ System32 \\ Speech \\ SpeechUX \\speechuxcpl.dll,-1

### <a name="storage-spaces"></a>Espaces de stockage

-   **Nom canonique**: Microsoft. StorageSpaces
-   **GUID**: {F942C606-0914-47AB-BE56-1321B8035096}
-   **Système d’exploitation pris en charge**: Windows 8, Windows 8.1
-   **Nom du module**: @C: \\ Windows \\ system32 \\SpaceControl.dll,-1

### <a name="sync-center"></a>Centre de synchronisation

-   **Nom canonique**: Microsoft. synccenter
-   **GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\SyncCenter.dll,-3000

### <a name="system"></a>Système

-   **Nom canonique**: Microsoft.SysTEM
-   **GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\systemcpl.dll,-1

### <a name="tablet-pc-settings"></a>Paramètres du Tablet PC

-   **Nom canonique**: Microsoft. TabletPCSettings
-   **GUID**: {80F3F1D5-FECA-45F3-BC32-752C152E456E}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\tabletpc.cpl,-10100

### <a name="taskbar-and-navigation"></a>Barre des tâches et navigation

-   **Nom canonique**: Microsoft. Taskbar
-   **GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}
-   **Système d’exploitation pris en charge**: Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\shell32.dll,-32517

### <a name="troubleshooting"></a>Dépannage

-   **Nom canonique**: Microsoft. Troubleshooting
-   **GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\DiagCpl.dll,-1
-   **Pages**

    | Nom de la page   | Opens   |
    |-------------|---------|
    | HistoryPage | Historique |

    

     

### <a name="tsappinstall"></a>TSAppInstall

-   **Nom canonique**: Microsoft. TSAppInstall
-   **GUID**: {BAA884F4-3432-48B8-AA72-9BF20EEF31D5}
-   **Système d’exploitation pris en charge**: Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\tsappinstall.exe,-2001

### <a name="user-accounts"></a>Comptes d'utilisateurs

-   **Nom canonique**: Microsoft. UserAccounts
-   **GUID**: {60632754-C523-4B62-b45c-4172da012619}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\usercpl.dll,-1

### <a name="windows-anytime-upgrade"></a>Mise à niveau express

-   **Nom canonique**: Microsoft. WindowsAnytimeUpgrade
-   **GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @ $ (resourceString. \_ SYS \_ Mod \_ chemin d’accès),-1

### <a name="windows-defender"></a>Windows Defender

-   **Nom canonique**: Microsoft. Windowsdefender
-   **GUID**: {D8559EB9-20C0-410E-Beda-7ED416AECC2A}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% ProgramFiles% \\ Windows Defender \\MsMpRes.dll,-104

### <a name="windows-firewall"></a>Pare-feu Windows

-   **Nom canonique**: Microsoft. WindowsFirewall
-   **GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @C: \\ Windows \\ system32 \\FirewallControlPanel.dll,-12122
-   **Pages**

    | Nom de la page         | Opens        |
    |-------------------|--------------|
    | pageConfigureApps | Applications autorisées |

    

     

### <a name="windows-mobility-center"></a>Centre de mobilité Windows

-   **Nom canonique**: Microsoft. MobilityCenter
-   **GUID**: {5ea4f148-308C-46d7-98a9-49041b1dd468}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\mblctr.exe,-1002

### <a name="windows-to-go"></a>Windows To Go

-   **Nom canonique**: Microsoft. PortableWorkspaceCreator
-   **GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}
-   **Système d’exploitation pris en charge**: Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\pwcreator.exe,-151

### <a name="windows-update"></a>Windows Update

-   **Nom canonique**: Microsoft. windowsupdate
-   **GUID**: {36eef7db-88ad-4E81-AD49-0e313f0c35f8}
-   **Système d’exploitation pris en charge**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Nom du module**: @% systemroot% \\ system32 \\wucltux.dll,-1
-   **Pages**

    | Nom de la page         | Opens               |
    |-------------------|---------------------|
    | pageSettings      | Modifier les paramètres     |
    | pageUpdateHistory | Afficher l’historique des mises à jour |

    

     

### <a name="work-folders"></a>Dossiers de travail

-   **Nom canonique**: Microsoft. WorkFolders
-   **GUID**: {ECDB0924-4208-451e-8EE0-373C0956DE16}
-   **Système d’exploitation pris en charge**: Windows 8.1
-   **Nom du module**: @C: \\ Windows \\ system32 \\WorkfoldersControl.dll,-1

## <a name="deprecated-control-panel-canonical-names"></a>Noms canoniques du panneau de configuration déconseillés

Les noms canoniques suivants ne sont plus utilisés à la Windows 8.1 ou une version ultérieure. Certains ont été complètement supprimés. D’autres ont été remappés dans les situations suivantes :

-   Un élément du panneau de configuration est renommé. Un nouveau nom canonique est attribué à l’élément renommé, mais conserve le même GUID. Dans ce cas, l’ancien nom canonique lance l’élément renommé du panneau de configuration. Sachez que l’élément lancé peut ne pas utiliser la même interface utilisateur que la version antérieure de cet élément.
-   La fonctionnalité d’un ou de plusieurs éléments du panneau de configuration est déplacée ou consolidée dans un nouvel élément. Dans ce cas, l’ancien nom canonique est mappé au nouvel élément de panneau de configuration le plus approprié.

> [!Note]  
> Des remappages existent pour la compatibilité descendante. Vous ne devez pas utiliser de valeurs déconseillées dans le nouveau code.

 



| Nom canonique déconseillé                                   | Élément du panneau de configuration                | GUID                                   | Notes                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft. AddHardware                                       | Ajouter un matériel                      | {7A979262-40CE-46ff-AEEE-7884AC3B6136} | Correspond à [Microsoft. DevicesAndPrinters](#devices-and-printers) à partir de Windows 7.                                                                                                                                                                                                                                                                            |
| Microsoft. AudioDevicesAndSoundThemes                        | Son                             | {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D} | Correspond à [Microsoft. Sound](#sound) depuis Windows 7.                                                                                                                                                                                                                                                                                                        |
| Microsoft. BackupAndRestoreCenter/Microsoft. BackupAndRestore | Centre de sauvegarde et de restauration         | {B98A2BEA-7D42-4558-8BD1-832F41BAC6FD} | Microsoft. BackupAndRestoreCenter est mappé à Microsoft. BackupAndRestore dans Windows 7. Les deux sont supprimés à partir de Windows 8 ; Utilisez à la place [Microsoft. FileHistory](#file-history) .                                                                                                                                                                                   |
| Microsoft. CardSpace                                         | Windows CardSpace                 | {78CB147A-98EA-4AA6-B0DF-C8681F69341C} | Suppression depuis Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. DesktopGadgets                                    | Gadgets du Bureau                   | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | Suppression depuis Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. GetProgramsOnline                                 | Place de marché Microsoft Azure               | {3e7efb4c-faf1-453d-89eb-56026875ef90} | Suppression depuis Windows 7.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. InfraredOptions                                   | Infrarouge                          | {A0275511-0E86-4ECA-97C2-ECD8F1221D08} | Correspond à [Microsoft. infrarouge](#infrared) à compter de Windows 7.                                                                                                                                                                                                                                                                                                  |
| Microsoft. langue                                          | Langage                          | {BF782CC9-5A52-4A17-806C-2A894FFEEAC5} | Supprimé à partir de Windows 10, version 1803                                                                                                                                                                                                                                                                                                                    |
| Microsoft. LocationAndOtherSensors                           | Emplacement et autres capteurs        | {E9950154-C418-419e-A90A-20C5287AE24B} | Correspond à [Microsoft. LocationSettings](#infrared) à partir de Windows 8.                                                                                                                                                                                                                                                                                          |
| Microsoft. PenAndInputDevices                                | Stylet et périphériques d’entrée             | {F82DF8F7-8B9F-442E-A48C-818EA735FF9B} | Correspond à [Microsoft. PenAndTouch](#pen-and-touch) à partir de Windows 7.                                                                                                                                                                                                                                                                                          |
| Microsoft. PeopleNearMe                                      | Voisinage immédiat                    | {5224F545-A443-4859-BA23-7B5A95BDC8EF} | Suppression depuis Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. PerformanceInformationAndTools                    | Informations et outils de performance | {78F3955E-3B90-4184-BD14-5397C15F1EFC} | Suppression à partir de Windows 8.1.                                                                                                                                                                                                                                                                                                                                |
| Microsoft. PhoneAndModemOptions                              | Téléphone et modem                   | {40419485-C444-4567-851A-2DD7BFA1684D} | Correspond à [Microsoft. PhoneAndModem](#phone-and-modem) à partir de Windows 7.                                                                                                                                                                                                                                                                                      |
| Microsoft. Printers                                          | Imprimantes                          | {2227A280-3AEA-1069-A2DE-08002B30309D} | Correspond à [Microsoft. DevicesAndPrinters](#devices-and-printers) à partir de Windows 7.                                                                                                                                                                                                                                                                            |
| Microsoft. ProblemReportsAndSolutions                        | Rapports et solutions aux problèmes     | {FCFEECAE-EE1B-4849-AE50-685DCF7717EC} | Correspond à [Microsoft. ActionCenter](#action-center) à partir de Windows 7.                                                                                                                                                                                                                                                                                         |
| Microsoft. RegionalAndLanguageOptions                        | Options régionales et linguistiques     | {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0} | Correspond à [Microsoft. RegionAndLanguage](#region) à partir de Windows 7. Notez que depuis Windows 8, la région et la langue ont chacune leur propre élément du panneau de configuration. Microsoft. RegionalAndLanguageOptions et Microsoft. RegionAndLanguage ouvrent actuellement l’élément Region. Vous devez utiliser [Microsoft. Language](#location-settings) pour accéder à l’élément de langue. |
| Microsoft. SecurityCenter                                    | Security Center Windows           | {087DA31B-0DD3-4537-8E23-64A18591F88B} | Correspond à [Microsoft. ActionCenter](#action-center) à partir de Windows 7.                                                                                                                                                                                                                                                                                         |
| Microsoft. SpeechRecognitionOptions                          | Options de reconnaissance vocale        | {58E3C745-D971-4081-9034-86E34B30836A} | Correspond à [Microsoft. SpeechRecognition](#speech-recognition) à partir de Windows 7.                                                                                                                                                                                                                                                                               |
| Microsoft. TaskbarAndStartMenu                               | Barre des tâches et menu Démarrer            | {0DF44EAA-FF21-4412-828E-260A8728E7F1} | Correspond à [Microsoft. Taskbar](#speech-recognition) à compter de Windows 8.                                                                                                                                                                                                                                                                                         |
| Microsoft. WelcomeCenter                                     | Centre d’accueil                    | {CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1} | Correspond à Microsoft. GettingStarted dans Windows 7. Ouvre la page d’hébergement du panneau de configuration à partir de Windows 8.                                                                                                                                                                                                                                                      |
| Microsoft. WindowsSidebarProperties                          | Propriétés du volet Windows        | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | Correspond à Microsoft. DesktopGadgets dans Windows 7. Suppression depuis Windows 8.                                                                                                                                                                                                                                                                                   |
| Microsoft. WindowsSideShow                                   | Windows SideShow                  | {E95A4861-D57A-4be1-AD0F-35267E261739} | Fonctionnalité déconseillée dans Windows 8, supprimée à partir de Windows 8.1.                                                                                                                                                                                                                                                                                               |



 

## <a name="using-canonical-names-in-local-group-policy"></a>Utilisation de noms canoniques dans les stratégie de groupe locaux

À compter de Windows 7, vous pouvez utiliser des noms canoniques pour restreindre l’accès aux éléments individuels du panneau de configuration par le biais de la stratégie de groupe. Cette même procédure peut être utilisée dans Windows Vista, mais vous devez utiliser le nom du module au lieu du nom canonique.

### <a name="hiding-individual-control-panel-items"></a>Masquage d’éléments individuels du panneau de configuration

Utilisez cette méthode si vous souhaitez afficher plus d’éléments du panneau de configuration que vous ne souhaitez masquer.

1.  Exécutez le fichier Gpedit. msc pour lancer l’éditeur de stratégie de groupe local. Vous pouvez également taper « stratégie de groupe » sur le Windows 8.1 écran d’accueil et sélectionner **modifier la stratégie de groupe** dans les résultats de la recherche.
2.  Sélectionnez **Configuration utilisateur**  >  **modèles d’administration**  >  **le panneau** de configuration.
3.  Sélectionnez **Masquer les éléments du panneau de configuration spécifiés**.
4.  Dans la fenêtre **Masquer les éléments du panneau de configuration spécifiés** qui s’ouvre, cliquez sur **activé**.
5.  Cliquez sur le bouton **Afficher** dans le panneau Options pour afficher la liste des éléments du panneau de configuration non autorisés.
6.  Dans la fenêtre **afficher le contenu** qui s’ouvre, tapez un nom canonique dans la colonne **valeur** . Répétez cette opération si nécessaire.
7.  Cliquez sur **OK**.

### <a name="showing-individual-control-panel-items"></a>Montrer des éléments du panneau de configuration individuels

Utilisez cette méthode si vous souhaitez masquer davantage d’éléments du panneau de configuration que vous le souhaitez.

1.  Exécutez le fichier Gpedit. msc pour lancer l’éditeur de stratégie de groupe local. Vous pouvez également taper « stratégie de groupe » sur le Windows 8.1 écran d’accueil et sélectionner **modifier la stratégie de groupe** dans les résultats de la recherche.
2.  Sélectionnez **Configuration utilisateur**  >  **modèles d’administration**  >  **le panneau** de configuration.
3.  Sélectionnez **afficher uniquement les éléments du panneau de configuration spécifiés**.
4.  Dans la fenêtre **afficher uniquement les éléments du panneau de configuration spécifiés** qui s’ouvre, cliquez sur **activé**. Cela masque tous les éléments du panneau de configuration.
5.  Cliquez sur le bouton **Afficher** dans le panneau Options pour afficher la liste des éléments du panneau de configuration autorisés.
6.  Dans la fenêtre **afficher le contenu** qui s’ouvre, tapez un nom canonique dans la colonne **valeur** . Répétez cette opération si nécessaire.
7.  Cliquez sur **OK**.

Si vous souhaitez supprimer toutes les entrées que vous avez ajoutées à la liste afficher ou masquer les éléments du panneau de configuration, revenez à l’écran à l’étape 4 et sélectionnez **non configuré** pour effacer la liste. Si vous souhaitez conserver vos entrées tout en interrompant les restrictions, sélectionnez **désactivé**.

## <a name="remarks"></a>Notes

Vous pouvez voir des éléments dans votre panneau de configuration qui ne sont pas répertoriés ici. Ces éléments ne font pas partie de Windows, mais sont ajoutés au moment de l’installation de divers logiciels et matériels, comme Microsoft Office ou une carte vidéo. Les éléments du panneau de configuration non-Windows peuvent ou non avoir un nom canonique. Pour rechercher le nom canonique d’un élément du panneau de configuration qui n’est pas répertorié ici, consultez le Registre sous ces chemins d’accès :

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID of the Control Panel item}
         System.ApplicationName
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         CLSID
            {CLSID of the Control Panel item}
               System.ApplicationName
```

Pour plus d’informations qui peuvent vous aider à découvrir les CLSID nécessaires, consultez [comment inscrire des éléments du panneau de configuration exécutables](how-to-register-an-executable-control-panel-item-registration-.md) et [comment inscrire des éléments du panneau de configuration de la dll](how-to-register-dll-control-panel-item-registration-.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exécution des éléments du panneau de configuration](executing-control-panel-items.md)
</dt> <dt>

[**IOpenControlPanel**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel)
</dt> </dl>

 

 



