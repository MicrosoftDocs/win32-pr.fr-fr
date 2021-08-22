---
title: Fonctions de gestion des profils
description: Fonctions de gestion des profils
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Windows Système de couleurs (WCS), fonctions
- WCS (Windows Color System), fonctions
- gestion des couleurs des images, fonctions
- gestion des couleurs, fonctions
- couleurs, fonctions
- Référence WCS, fonctions
- référence pour WCS, functions
- Windows Système de couleurs (WCS), profils
- WCS (Windows Color System), profils
- gestion des couleurs des images, profils
- gestion des couleurs, profils
- couleurs, profils
- Référence WCS, profils
- référence pour WCS, profils
- gestion des profils
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f047c2dee199800fad976dd7b959fbbb54d585fd252fb8b5390c3223415db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587769"
---
# <a name="profile-management-functions"></a>Fonctions de gestion des profils

## <a name="profile-management-functions"></a>Fonctions de gestion des profils

Les fonctions d’API suivantes sont utiles pour la gestion des profils.



| Fonction                                                                               | Description                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Associe un profil de couleurs spécifié à un périphérique spécifié.                                                              |
| [**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Convertit un [espace de couleurs](c.md) logique en un [profil de périphérique](d.md). |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Dissocie un profil de couleurs spécifié avec un périphérique spécifié sur un ordinateur spécifié. |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Énumère tous les profils qui remplissent les critères d’énumération donnés. |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | récupère le chemin d’accès du répertoire de couleurs Windows sur un ordinateur spécifié. |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Obtient la rampe gamma à partir des panneaux d’affichage de couleur directe.                                                                                                |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Récupère le profil de couleurs inscrit pour l’espace de [couleurs](c.md)standard spécifié. |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Installe un profil donné pour une utilisation sur un ordinateur spécifié. Le profil est également copié dans le répertoire des couleurs. |
| [**RegisterCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | Associe une valeur d’identification spécifiée à la bibliothèque de liens dynamiques du module de gestion des couleurs spécifiée (DLL CMM). lorsque cet ID apparaît dans un profil de couleurs, Windows pouvez alors localiser le CMM correspondant afin de créer une transformation. |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Définit la rampe gamma sur les panneaux d’affichage de couleur directe.                                                                                                  |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Inscrit un profil spécifié pour un [espace de couleurs](c.md)standard donné. Le profil peut être interrogé à l’aide de [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew). |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Supprime un profil de couleurs spécifié d’un ordinateur spécifié. Les fichiers associés sont éventuellement supprimés du système. |
| [**UnregisterCMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Dissocie une valeur d’ID spécifiée d’une bibliothèque de liens dynamiques (DLL) de module de gestion des couleurs donnée. |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Associe un profil de couleurs WCS spécifié à un périphérique spécifié.                                                                                    |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Convertit un profil WCS en profil ICC.                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Dissocie un profil de couleurs WCS spécifié avec un périphérique spécifié sur un ordinateur spécifié.                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Énumère tous les profils de couleurs qui répondent aux critères d’énumération dans la portée de gestion des profils spécifiée.                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | Retourne la taille, en octets, de la mémoire tampon requise par la fonction [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) pour énumérer les profils de couleurs. |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | Récupère le profil de couleurs par défaut pour un appareil ou la valeur par défaut indépendante du périphérique si l’appareil n’est pas spécifié.                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Retourne la taille, en octets, du nom du profil de couleurs par défaut d’un appareil, y compris la marque de fin **null** .                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Récupère l’intention de rendu par défaut dans la portée de gestion des profils spécifiée.                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Détermine si l’utilisateur a choisi d’utiliser une liste d’association de profils par utilisateur pour l’appareil spécifié.                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Crée un handle vers un profil de couleurs spécifié.                                                                                                       |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Définit le nom du profil de couleurs par défaut du type de profil spécifié dans l’étendue de gestion des profils spécifiée.                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Définit l’intention de rendu par défaut dans la portée de gestion des profils spécifiée.                                                                         |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Permet à l’utilisateur de spécifier s’il faut utiliser une liste d’association de profils par utilisateur pour l’appareil spécifié.                                              |



 

## <a name="profile-consumption-functions"></a>Fonctions de consommation des profils

Les API de consommation des profils sont les API de ICM2 qui prennent des profils XML ICC ou WCS, des handles de profil ou des intentions de rendu en tant que paramètres, et un ensemble de nouvelles API pour la prise en charge des profils WCS pour le code de gestion des couleurs des applications.

 

## <a name="profiles-and-profile-management-functions"></a>Fonctions de gestion des profils et des profils

Le flux de travail de gestion des profils est basé sur les API ICM2 existantes qui sont augmentées pour fournir des fonctionnalités supplémentaires pour la révision du code de l’application.

Les profils contiennent des informations utilisées par les algorithmes de traitement des couleurs pour convertir la couleur entre différents espaces de couleurs. La gestion des profils permet d’interroger et de spécifier les profils qui sont utilisés à différentes étapes par le modèle de traitement des couleurs pour gérer la sortie en couleurs des différents périphériques avec des caractéristiques de couleur différentes.

La gestion des profils fournit l’ensemble de fonctionnalités suivant :

 

1. Installation des profils de couleurs à utiliser dans le système.

 

2. Association d’un ou plusieurs profils de couleurs installés à un appareil particulier.

 

3. Choix d’un profil de couleurs par défaut d’un type particulier parmi les profils pouvant être utilisés dans une étape particulière du traitement des couleurs. Il peut s’agir d’un appareil parmi les profils qui lui sont associés, ou parmi les profils installés dans le système, et non spécifiques à l’appareil.

 

4. Énumération des profils de couleurs qui répondent à des critères particuliers parmi les profils installés dans le système.

Les extensions de nom de fichier de profil WCS sont « . CDMP » pour DMPs, « . camp » pour les CAMPs et « . GMMP » pour GMMPs.

 

**Gestion des profils par utilisateur et activation de l’exécution dans le contexte LUA**

L’objectif de la conception décrite dans le document actif est le suivant :

 

1. L’implémentation ICM2 héritée ne prend pas en charge la gestion des profils par utilisateur. Les différents utilisateurs ne peuvent pas avoir leurs propres paramètres de profil. Dans Vista, l’infrastructure de gestion des profils WCS permet aux utilisateurs de configurer des paramètres de profil individuels pour la plupart des fonctionnalités.

 

2. Toutes les API de gestion des profils ICM2 héritées modifient les paramètres au niveau du système et nécessitent des privilèges d’administrateur. dans Windows Vista, tous les utilisateurs s’exécutent dans les paramètres de compte d’utilisateur à faibles privilèges (LUA) la plupart du temps, et les administrateurs peuvent élever les privilèges de manière sélective pour exécuter des applications qui modifient les paramètres au niveau du système. Dans la gestion des profils WCS, tous les paramètres de profil par utilisateur sont configurables dans le contexte LUA. Les applications de gestion des profils peuvent s’exécuter en tant que paramètres LUA, en renforçant leur portée d’utilisation et en veillant à ce que la sécurité du système ne soit pas compromise.

La gestion des profils dans Vista offre les améliorations suivantes par rapport à l’infrastructure ICM2 héritée :

 

1. Il permet l’Association de profils à des appareils, les paramètres de profil par défaut et l’énumération de profils dans une étendue par utilisateur et à l’échelle du système.

 

2. L’installation d’un profil reste au niveau du système et nécessite des privilèges d’administrateur. Cela est cohérent avec l’installation du profil lors de l’installation du périphérique, car l’installation de l’appareil est à l’ensemble du système et nécessite des privilèges d’administrateur.

 

Le fait que les appareils puissent être installés à partir du contexte LUA est spécifique à ce qui est pris en charge pour cette classe d’appareil. Par exemple, dans Vista, il est possible d’installer une imprimante à partir du contexte LUA si l’utilisateur dispose des droits nécessaires pour copier des fichiers dans le magasin de pilotes par un administrateur de domaine à l’aide des stratégies du magasin de pilotes. L’infrastructure de gestion des profils de couleurs n’a rien à faire à ce sujet, car l’installation s’effectue dans le contexte du spouleur.

 

3. La modification des paramètres de profil dans l’étendue par utilisateur peut être effectuée dans le contexte LUA. les modifications à l’ensemble du système nécessitaient des privilèges d’administrateur. Les opérations de gestion des profils qui nécessitent la lecture des informations de configuration peuvent être effectuées dans un contexte LUA pour les paramètres par utilisateur et à l’ensemble du système.

La portée de gestion des profils indique l’étendue des opérations effectuées. à l’ensemble du système ou par utilisateur.

Pour chaque opération, il est indiqué s’il peut être effectué à partir du contexte LUA. Si une opération ne peut pas être effectuée dans le contexte LUA, l’API de gestion des profils correspondante retourne un échec avec accès refusé. Les applications qui utilisent l’API, telles que le panneau de configuration de la gestion des couleurs, peuvent permettre à l’utilisateur d’élever au contexte d’administration (à l’aide de OTS ou de l’interface utilisateur de consentement), puis d’appeler l’API à partir du contexte élevé pour que l’opération aboutisse.



Opération

Étendue de gestion des profils

Condition préalable

Après condition

Exécutable dans le contexte LUA

$ {ROWSPAN2} $Install profil $ {REMOVE} $  

À l’ensemble du système

Le profil a été copié, installé dans le système et peut être utilisé. Le profil est énumérable dans l’étendue à l’échelle du système et de l’utilisateur actuel pour tous les utilisateurs.

Lors de l’installation du pilote de périphérique, régie par les stratégies d’installation du pilote. « NON » dans le cas contraire.

Utilisateur actuel

Non pris en charge

$ {ROWSPAN2} $Uninstall profil $ {REMOVE} $  

À l’ensemble du système

Le profil est installé dans le système

Profil désinstallé du système et éventuellement supprimé du magasin de profils. Le profil n’est plus disponible et n’est pas énumérable dans une étendue.

Non

Utilisateur actuel

Non pris en charge

$ {ROWSPAN2} profil $Associate avec l’appareil $ {REMOVE} $  

À l’ensemble du système

Le profil est installé et est de type ICC ou CDMP

Le profil peut être utilisé avec l’appareil par tous les utilisateurs. Il est énumérable, dans une portée à l’échelle du système et également pour l’étendue de l’utilisateur actuel pour tous les utilisateurs, comme associé à l’appareil.

Non

Utilisateur actuel

Le profil est installé. Peu importe si le profil est déjà associé à l’appareil dans l’étendue à l’échelle du système et s’il est de type ICC ou CDMP.

Le profil peut être utilisé avec l’appareil par l’utilisateur actuel. Elle est énumérable uniquement dans l’étendue de l’utilisateur actuel (à moins qu’il y ait également une association à l’échelle du système) associée à l’appareil.

Oui

Profil de $Disassociate $ {ROWSPAN2} du périphérique $ {REMOVE} $  

À l’ensemble du système

Le profil est associé à l’appareil dans l’étendue à l’échelle du système et est de type ICC ou CDMP

Le profil n’est plus disponible pour une utilisation (sauf pour les utilisateurs qui ont également cette association dans leur étendue d’utilisateur actuel). Elle n’est pas énumérable dans une portée à l’échelle du système. Toutefois, elle peut être énumérable dans l’étendue de l’utilisateur actuel pour un utilisateur qui a cette association dans son étendue.

Non

Utilisateur actuel

Le profil est associé à l’appareil dans l’étendue de l’utilisateur actuel (qu’il soit associé à l’étendue système) et est de type ICC ou CDMP.

Le profil n’est plus disponible ou est énumérable comme associé à l’appareil, par l’utilisateur actuel (sauf s’il est également associé à l’appareil à l’échelle du système).

Oui

$ {ROWSPAN2} $Set profil pour un type (DMP ou ICC) comme valeur par défaut pour un appareil $ {REMOVE} $  

À l’ensemble du système

Le profil est de type ICC ou CDMP

Le profil est utilisé par défaut pour le type particulier avec l’appareil, pour tous les utilisateurs, à l’exception de ceux qui ont remplacé ce paramètre dans l’étendue de l’utilisateur actuel. (Le profil est installé et associé au système d’appareil en largeur, si ce n’est pas déjà le cas.)

Non

Utilisateur actuel

Le profil est de type ICC ou CDMP

Le profil est utilisé par défaut pour le type particulier avec l’appareil dans le cas de l’utilisateur actuel, quelle que soit la valeur par défaut à l’ensemble du système pour ce. (Le profil est installé et associé à l’appareil pour l’utilisateur actuel, si ce n’est pas déjà le cas.)

Oui, si le profil est déjà installé

$ {ROWSPAN2} $Set profil pour un type (ICC, DMP, CAMP, GMMP) et une combinaison de sous-type en tant que valeur globale par défaut $ {REMOVE} $  

À l’ensemble du système

Seuls les profils ICC et CDMP peuvent être associés à des appareils.

Le profil est utilisé par défaut pour le type particulier. Les utilisateurs peuvent remplacer ce paramètre dans l’étendue de l’utilisateur actuel. (Le profil est installé, si ce n’est pas déjà le cas.)

Non

Utilisateur actuel

Seuls les profils ICC et CDMP peuvent être associés à des appareils.

Le profil est utilisé par défaut pour le type particulier de l’utilisateur actuel. (Le profil est installé, si ce n’est pas déjà le cas.)

Oui, si le profil est déjà installé.

$ {ROWSPAN2} $Erase la substitution de l’utilisateur actuel pour un paramètre de profil par défaut particulier, afin que la valeur système par défaut soit toujours utilisée (comme secours) même pour l’étendue de l’utilisateur actuel. $ {REMOVE} $  

À l’ensemble du système

Non applicable

Utilisateur actuel

Même pour les requêtes de l’utilisateur actuel sur les paramètres de profil par défaut, les paramètres à l’ensemble du système sont retournés pour être utilisés.

Oui

$ {ROWSPAN2} $Enumerate les profils installés répondant à des critères particuliers (tels que la classe de périphérique, la classe de profil, etc.) $ {REMOVE} $  

À l’ensemble du système

Seuls les profils ICC et CDMP peuvent être associés et énumérés pour les appareils.

Les profils qui sont installés et qui répondent aux critères spécifiés dans l’étendue à l’échelle du système sont énumérés.

Oui

Utilisateur actuel

Seuls les profils ICC et CDMP peuvent être associés à des appareils et, par conséquent, énumérés pour les appareils.

Les profils qui sont installés et qui répondent aux critères spécifiés dans l’étendue à l’échelle du système sont énumérés.

Oui

$ {ROWSPAN2} $Enumerate profils associés à un appareil particulier répondant à des critères particuliers, tels que la classe de périphérique et la classe de profil $ {REMOVE} $  

À l’ensemble du système

Seuls les profils ICC et CDMP peuvent être associés et énumérés pour les appareils.

Les profils associés à l’appareil dans une étendue à l’échelle du système et satisfont aux critères spécifiés dans l’étendue à l’échelle du système sont énumérés.

Oui

Utilisateur actuel

Seuls les profils ICC et CDMP peuvent être associés et énumérés pour les appareils.

Les profils qui sont disponibles comme associés à l’appareil dans l’étendue de l’utilisateur actuel, y compris les associations à l’échelle du système et satisfont aux critères spécifiés dans l’étendue de l’utilisateur actuel sont énumérés.

Oui



 

Les types de profil de couleurs valides sont fournis par l’énumération COLORPROFILETYPE.

Les sous-types de profil de couleurs valides sont fournis par l’énumération COLORPROFILESUBTYPE.

Les combinaisons valides de type de profil/sous-type sont indiquées dans le tableau suivant.



COLORPROFILETYPE 

COLORPROFILESUBTYPE valide

Remarques

Paramètre par défaut de l’appareil

Valeur par défaut globale

Utilisation prévue

Utilisation prévue

\_CCI CPT

CPST \_ aucun

Obtenir/définir le profil ICC par défaut associé à un appareil

CPST \_ RGBWorkingSpace ou CPST \_ CustomWorkingSpace

Obtient/définit le profil ICC en tant que profil d’espace de travail RVB global ou personnalisé. Consultez Remarque.

Les COLORPROFILETYPE CPT \_ ICC et CPT \_ DMP s’excluent mutuellement. Le profil de couleurs par défaut que vous définissez pour un espace de travail donné (RVB ou personnalisé) peut être un profil ICC ou DMP, mais pas les deux.

CPT \_ DMP

CPST \_ aucun

Obtenir/définir le profil DMP par défaut associé à un appareil

CPST \_ RGBWorkingSpace ou CPST \_ CustomWorkingSpace

Obtient/définit le profil DMP en tant que profil d’espace de travail RVB global ou personnalisé. Consultez Remarque.

Les COLORPROFILETYPE CPT \_ ICC et CPT \_ DMP s’excluent mutuellement. Le profil de couleurs par défaut que vous définissez pour un espace de travail donné (RVB ou personnalisé) peut être un profil ICC ou DMP, mais pas les deux.



 

> [!Note]  
> Quand WcsSetDefaultColorProfile est appelé pour définir un profil DMP comme profil par défaut pour l’espace de travail RVB ou un espace de travail personnalisé, seul un profil DMP de type RGBVirtualDevice, LCD ou CRT est valide.
>
>  
>
> Quand WcsSetDefaultColorProfile est appelé pour définir un profil ICC comme profil par défaut pour l’espace de travail RVB ou un espace de travail personnalisé, seul un profil ICC dont la classe est « SPAC » ou « DISP » et dont l’espace colorimétrique est « RGB » est valide.

 

L’architecture est conçue conformément aux exigences des opérations, comme indiqué dans les énumérations et les tables ci-dessus.

### <a name="profile-management-public-api-layer"></a>Couche API publique de gestion des profils

Étant donné que l’étendue de gestion des profils n’est pas prise en charge par les API ICM2 héritées, un nouvel ensemble d’API de gestion des profils WCS est requis, qui définit l’étendue de gestion des profils en tant qu’utilisateur à l’échelle du système ou ? Les API ICM2 héritées continuent à être prises en charge pour la compatibilité descendante et fonctionnent sur l’étendue de gestion des profils qui est implicite pour l’appel. o ICM2 API qui fonctionnent sur l’étendue de l’utilisateur actuel ? Cela concerne les opérations qui sont prises en charge à la fois pour l’étendue de l’utilisateur au niveau du système et de l’utilisateur actuel dans la gestion des profils WCS. Les API ICM2 héritées appellent sur les nouvelles API WCS avec une étendue de gestion de profil en tant qu’utilisateur actuel. Cela est logique du point de vue de l’utilisateur, car cela permet d’activer des paramètres par utilisateur à partir d’applications héritées et d’exécuter la plupart des opérations dans le contexte LUA. o ICM2 API qui fonctionnent sur une étendue à l’échelle du système ? Cela concerne les opérations (installer les profils et les profils de désinstallation) qui prennent uniquement en charge l’étendue à l’échelle du système. Aucune nouvelle API de gestion des profils WCS n’est créée et les API existantes peuvent être modifiées.

Les implémentations sous-jacentes des opérations de gestion des profils fonctionnent sur les entités de données de configuration suivantes pour créer le contexte des algorithmes de traitement des couleurs afin de fournir des fonctionnalités de gestion des couleurs. Il s’agit de paramètres spécifiques à l’appareil ou globaux (indépendants du périphérique). o données de configuration spécifiques à l’appareil :? Liste des profils associés à un appareil particulier. ? Profil par défaut pour les différents types de profils associés à un appareil. ? Mode de correspondance des profils utilisé pour l’énumération. o données de configuration globale :? Liste des profils installés dans le système. ? Profil global par défaut pour les différents types de profils. ? Les implémentations sous-jacentes du stockage de données de configuration prennent la portée de stockage pour les données de configuration (indépendantes des appareils ou des appareils), qui peuvent être à l’échelle du système ou de l’utilisateur actuel. Cela diffère de l’étendue de gestion des profils. Une opération avec l’étendue de gestion du profil utilisateur actuel peut entraîner une lecture à partir d’une étendue de stockage à l’échelle du système si le paramètre de l’utilisateur actuel pour cette opération n’est pas présent. ? La couche d’API ICM2/WCS appelle dans cette couche de stockage pour obtenir et définir des données avec une étendue de stockage appropriée. La couche de stockage est transparente pour l’étendue de gestion des profils. La logique permettant de combiner des données à partir d’étendues de stockage à l’échelle de l’utilisateur et du système pour créer ou mettre à jour une configuration en fonction de l’étendue de gestion des profils spécifiée par l’appelant de l’API. Cette logique est présente dans la couche API ICM2/WCS.

### <a name="device-specific-storage-layer"></a>Couche de stockage spécifique à l’appareil

Le stockage de différentes classes d’appareils, tels que l’impression, la capture ou l’affichage, peut être différent. Par exemple, les données de configuration d’un périphérique d’impression doivent être stockées à l’aide d’API d’impression standard, telles que SetPrinterDataEx et GetPrinterDataEx, pour permettre la copie des profils et le transfert des paramètres vers un ordinateur client pendant la connexion point-à-impression. ? Cette couche exporte les fonctionnalités pour ouvrir le magasin, obtenir des données, définir des données et fermer le magasin à l’aide d’interfaces prédéfinies communes afin que la couche de stockage de configuration de la gestion des profils puisse les appeler tout en étant transparente pour la façon dont les données sont stockées pour cet appareil.

Le diagramme suivant illustre cette architecture.



Couche API publique de gestion des profils

$ {ROWSPAN2} $Legacy les API ICM2 pour les opérations qui prennent uniquement en charge l’étendue de gestion des profils à l’échelle du système dans Vista (installer, désinstaller et obtenir le répertoire de couleurs). Ils appellent la couche de stockage de configurations avec une étendue de stockage appropriée. $ {REMOVE} $  

API ICM2 héritée pour les opérations qui prennent en charge à la fois l’étendue de gestion du profil utilisateur et à l’échelle du système dans Vista (toutes les opérations autres que installer, désinstaller et obtenir le répertoire de couleurs). Ils fonctionnent implicitement sur l’étendue de l’utilisateur actuel et appellent la nouvelle API WCS avec l’étendue de gestion des profils comme utilisateur actuel.

Nouvelle API WCS avec prise en charge de l’étendue de gestion du profil à l’échelle du système et de l’utilisateur actuel. Ils appellent la couche de stockage de configurations avec une étendue de stockage appropriée.



 



Configuration de la gestion des profils Stockage couche

Routines de configuration globale indépendantes du périphérique

Routines de configuration spécifiques à l’appareil

$ {ROWSPAN3} $Profile l’installation et la gestion des paramètres de profil par défaut indépendants du périphérique, pris en charge dans l’étendue du stockage à l’échelle du système et de l’utilisateur actuel. $ {REMOVE} $  

L’Association d’appareils et la gestion des paramètres de profil par défaut spécifiques au périphérique, pris en charge dans l’étendue du stockage à l’échelle du système et de l’utilisateur actuel.

couche de Stockage Device-Specific

Imprimer un stockage spécifique

Afficher un stockage spécifique

Capturer un stockage spécifique



 

Les API ICM2 héritées pour les opérations qui prennent uniquement en charge l’étendue de gestion des profils à l’échelle du système dans Vista n’ont aucune modification de comportement. Les opérations d’installation et de désinstallation appartiennent à cette catégorie.

Les API ICM2 héritées pour les opérations qui prennent en charge à la fois l’étendue de gestion du profil à l’échelle du système et de l’utilisateur actuel ont un comportement modifié pour interroger et configurer les paramètres de l’utilisateur actuel. Toutes les opérations autres que install et Uninstall appartiennent à cette catégorie.

 

 




