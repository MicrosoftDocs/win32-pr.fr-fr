---
title: Vue d’ensemble du Framework biométrique
description: La prise en charge native des appareils biométriques est intégrée à Windows.
ms.assetid: 616ba95a-27a3-4eac-b802-5217954ed04e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f524437ba60f0ad5c1518225f91ff23c789a917
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463443"
---
# <a name="biometric-framework-overview"></a>Vue d’ensemble du Framework biométrique

Chaque individu a des caractéristiques uniques qui peuvent être utilisées pour l’identification. En général, ces caractéristiques sont physiques et incluent des caractéristiques telles que les empreintes digitales, mais elles peuvent également inclure des caractéristiques comportementales telles que la démarche et le rythme de frappe. Le terme « biométrie » englobe les deux significations. Les informations biométriques remplacent de plus en plus les mots de passe pour identifier et vérifier les utilisateurs. Elle est plus sécurisée et souvent plus pratique pour les utilisateurs et les administrateurs.

Les capteurs permettent de capturer des informations biométriques. Les informations sont capturées par le capteur comme un échantillon biométrique. Un seul échantillon contient des données qui représentent une caractéristique biométrique unique pour une personne. La moyenne de plusieurs échantillons est calculée pour créer un modèle biométrique, et le modèle est stocké en toute sécurité. Par la suite, un exemple d’utilisateur inconnu est comparé aux modèles stockés pour établir et vérifier l’identité de l’utilisateur. Le service de biométrie Windows, qui fait partie de l’Windows Biometric Framework (WBF), offre les fonctionnalités suivantes. L’API du WBF vous permet de réutiliser cette fonctionnalité.

-   Elle capture des échantillons biométriques et s’en sert pour créer un modèle.
-   Enregistre et récupère en toute sécurité des modèles biométriques.
-   Mappe chaque modèle à un identificateur unique, tel qu’un GUID ou un SID.

Vous pouvez également utiliser cette API pour étendre l’infrastructure et créer des adaptateurs de capteur biométriques, des moteurs correspondants et des composants de stockage. Pour plus d’informations sur la création d’adaptateurs de capteur, les moteurs correspondants et les composants de stockage, consultez [création de plug-ins d’adaptateur](creating-adapter-plug-ins.md).

## <a name="core-platform-components"></a>Composants de la plateforme principale

### <a name="windows-biometric-driver-interface-wbdi"></a>Windows Biometric Server (Windows Biometric Driver Interface)

Server est une interface de programmation qu’un pilote biométrique peut utiliser pour exposer le périphérique biométrique par le biais du service de biométrie Windows (WBS). Vous pouvez implémenter un pilote Server à l’aide de n’importe quelle technologie de pilote prise en charge, y compris les éléments suivants. Toutefois, nous vous recommandons d’utiliser UMDF dans la mesure du possible pour améliorer la qualité du pilote et la stabilité du système.

-   Infrastructure de pilote de mode utilisateur (UMDF)
-   Infrastructure de pilote en mode noyau (KMDF)
-   Windows Driver Model (WDM)

Un pilote biométrique Server doit également prendre en charge le GUID de l’interface de pilote Server et tous les contrôles d’e/s obligatoires (IOCTL). Les développeurs de pilotes doivent consulter la documentation et des exemples de code dans le kit WDK (Windows Driver Kit).

### <a name="windows-biometric-service-wbs"></a>Service de biométrie Windows (WBS)

Le service de biométrie Windows gère les pilotes biométriques installés et prend en charge l’API Windows Biometric Framework pour fournir un accès d’appareil aux applications clientes. Le WBS effectue les fonctions suivantes :

-   Il protège la confidentialité des utilisateurs en séparant les applications clientes des données biométriques.
-   Il protège les données biométriques des applications clientes non privilégiées en obligeant les applications à accéder aux données à l’aide d’identificateurs uniques.
-   Il utilise un composant logiciel appelé [unité biométrique](/previous-versions//dd401512(v=vs.85)) pour exposer les fonctionnalités d’un périphérique biométrique particulier par le biais d’une interface standardisée.
-   Il gère les unités biométriques en les regroupant dans des [pools de capteurs](sensor-pools.md)système, privés ou non attribués.
-   Il prend en charge l’utilisation d' [adaptateurs](/previous-versions//dd401508(v=vs.85)) d’unités biométriques pour les appareils physiques qui n’ont pas de capacités de traitement ou de stockage intégrées.

### <a name="windows-biometric-framework-api"></a>API WBF (Windows Biometric Framework)

L’API Windows Biometric Framework vous permet de créer des applications clientes qui peuvent interagir avec le service de biométrie Windows pour effectuer les actions suivantes :

-   Identifiez et vérifiez les utilisateurs.
-   Recherchez des appareils biométriques et interrogez leurs fonctionnalités.
-   Gérer les sessions et surveiller les événements.

## <a name="user-experience-components"></a>Composants de l’expérience utilisateur

### <a name="discovery-points"></a>Points de détection

Les utilisateurs finaux peuvent localiser des appareils biométriques de l’une des manières suivantes :

-   Tapez les mots biométriques, empreinte digitale, visage ou autres expressions associées dans la zone de texte Rechercher pour démarrer le panneau de configuration périphériques biométriques. La liste des résultats pour la biométrie peut contenir des éléments tels que les suivants sur une image Windows 10.
    -   Configurer la connexion par empreinte digitale
    -   Configurer la connexion face

### <a name="supported-scenarios"></a>Scénarios pris en charge

Les scénarios suivants sont pris en charge :

-   Les utilisateurs peuvent ouvrir une session sur un ordinateur local, un groupe de travail ou un domaine à l’aide d’un lecteur d’empreintes digitales, ou un appareil photo IR concentré sur la face.
-   Un utilisateur disposant de privilèges d’administrateur peut élever les applications via le contrôle de compte d’utilisateur (UAC) à l’aide d’une empreinte digitale ou d’un visage.

## <a name="management-components"></a>Composants de gestion

Un système biométrique peut être géré à l’aide d’stratégie de groupe ou de la gestion des appareils mobiles (MDM).

### <a name="biometric-system-management"></a>Gestion des systèmes biométriques

Vous pouvez gérer les fonctionnalités biométriques à l’aide de stratégie de groupe ou MDM. Stratégie de groupe peut être utilisé pour effectuer les actions suivantes :

-   Spécifiez le délai d’expiration pour le changement rapide d’utilisateur, s’il est implémenté par l’ISV.
-   Empêcher l’installation d’appareils biométriques.
-   Forcez la suppression des pilotes pour les périphériques biométriques.
-   Désactivez le service biométrique.

 

 