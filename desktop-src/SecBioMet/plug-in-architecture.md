---
title: Architecture du plug-in
description: Les unités biométriques exposent les fonctionnalités d’un appareil à l’infrastructure par le biais d’une interface standard qui se compose de capteurs, de moteurs et d’adaptateurs de stockage.
ms.assetid: d2835413-70a3-45fa-93e2-3fe78097554f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33a82f85387698f7fb80c65525004ac541a1108635ca3d929adda7b0cbb932cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119411062"
---
# <a name="plug-in-architecture"></a>Architecture du plug-in

Les périphériques biométriques sont fabriqués dans un large éventail de types et de configurations. le Windows Biometric Framework résout cette variété en fournissant une architecture extensible qui permet aux développeurs tiers de créer des composants de plug-in personnalisés. Le composant principal est un objet logiciel appelé unité biométrique. Les unités biométriques exposent les fonctionnalités d’un appareil à l’infrastructure par le biais d’une interface standard qui se compose de capteurs, de moteurs et d’adaptateurs de stockage. Les unités biométriques et leurs composants constitutifs sont présentés dans les rubriques suivantes.

## <a name="biometric-unit"></a>Unité biométrique

le composant central de l’architecture du plug-in Windows Biometric Framework est l’unité biométrique, un objet logiciel qui expose les fonctionnalités d’un appareil biométrique à l’infrastructure par le biais d’une interface standard.

Un seul capteur physique est associé à chaque unité biométrique. Le capteur capture les données biométriques et peut également, en fonction de ses capacités matérielles, exécuter d’autres opérations biométriques telles que la correspondance de modèle et le stockage. Les capteurs qui ne prennent pas en charge la correspondance ou le stockage d’intégration nécessitent des modules logiciels supplémentaires pour exécuter ces fonctions. Pour plus d’informations, consultez [adaptateurs](/previous-versions//dd401508(v=vs.85)).

L’illustration suivante montre la façon dont les données circulent via une unité biométrique. Fondamentalement, le workflow de données forme un type de pipeline. L’entrée initiale du pipeline est un exemple biométrique capturé par un capteur physique. Le moteur tente de faire correspondre l’exemple aux modèles qui existent déjà dans le magasin de modèles ou, si aucune correspondance n’est trouvée, génère un nouveau modèle à partir d’échantillons physiques répétés et enregistre le modèle dans le magasin.

![transmission de données via une unité biométrique](images/biometricunit-dataflow.png)

## <a name="biometric-unit-life-cycle"></a>Cycle de vie des unités biométriques

### <a name="creation"></a>Création

lorsque le Service biométrique Windows démarre ou lorsqu’il reçoit une notification matérielle de la part du gestionnaire de Plug-and-Play, il recherche tout matériel qui prend en charge le GUID d’interface \_ DEVINTERFACE \_ \_ (E2B5183A-99EA-4cc3-AD6B-80CA8D715B80). Pour chaque périphérique biométrique qui l’a découvert, alors :

-   Ouvre un handle vers l’appareil.
-   interroge les fonctionnalités de l’appareil à l’aide d’une interface de contrôle de pilote biométrique Windows.
-   Ouvre la clé de registre de l’appareil et tente de localiser les informations relatives aux plug-ins d’adaptateur associés.
-   ouvre la clé de registre Windows biometric Service et recherche des informations sur tous les plug-ins globaux qui doivent remplacer les valeurs spécifiques à l’appareil trouvées à l’étape précédente.
-   Crée une unité biométrique pour représenter l’appareil et la transmet à un fournisseur de services biométriques.

### <a name="configuration"></a>Configuration

Lorsqu’un fournisseur de services biométriques accepte une unité biométrique, il configure l’unité et l’attribue à un pool de capteurs. Pour plus d’informations, consultez [pools de capteurs](sensor-pools.md). L’unité est configurée en chargeant les adaptateurs appropriés, en se connectant à un magasin de modèles et en modifiant éventuellement le mode d’opération. Une unité biométrique peut être configurée pour fonctionner dans l’un des deux modes suivants :

-   En mode de base, l’unité agit comme un simple appareil de capture. Il n’utilise pas le traitement ou le stockage intégré, mais s’appuie entièrement sur les adaptateurs logiciels pour une prise en charge supplémentaire. Elle doit être en mesure de générer des exemples dans un format standard. Par exemple, les lecteurs d’empreintes digitales doivent générer des exemples conformes à l’INCITS ANSI 381-2004. L’objectif du mode de base est de prendre en charge l’interopérabilité entre les composants de différents fournisseurs.
-   En mode avancé, l’unité biométrique utilise des fonctions de traitement et de stockage intégrées. Il doit exposer les interfaces standard, mais peut générer et traiter des exemples dans n’importe quel format souhaité.

Lorsqu’une unité biométrique est déplacée d’un pool de capteurs à un autre, ses adaptateurs sont déchargés et reconfigurés pour le nouveau pool de capteurs. L’identité de l’unité biométrique reste constante ; seule la configuration matérielle et les plug-ins d’adaptateur sont modifiés.

### <a name="shut-down"></a>Éteindre

lorsque le service biométrique Windows s’arrête ou lorsque le gestionnaire de Plug-and-Play le notifie qu’une unité a été supprimée, le service supprime toutes les unités biométriques.

## <a name="adapters"></a>Adaptateurs

Les composants logiciels enfichables appelés adaptateurs connectent une unité biométrique à son matériel sous-jacent et fournissent toutes les fonctionnalités qui peuvent être manquantes dans le matériel du capteur. Vous pouvez créer trois types d’adaptateurs :

-   Un adaptateur de capteur encapsule un périphérique biométrique et fournit une interface standard pour configurer le capteur, capturer des échantillons et contrôler le workflow de données biométriques pour le moteur de traitement.
-   Un adaptateur de moteur génère des modèles biométriques à partir d’exemples capturés, fait correspondre des exemples à des modèles existants et des modèles d’index.
-   Un adaptateur de stockage gère les bases de données de modèles.

Les adaptateurs peuvent être chargés et déchargés au moment de l’exécution. cela permet au Service de Windows biométrique de reconfigurer dynamiquement une unité biométrique en la connectant à un ensemble différent de cartes.

Enfin, chaque interface de capteur, de moteur et d’adaptateur de stockage expose deux méthodes, **ControlUnit** et **ControlUnitPrivileged**, qui permettent aux applications clientes d’accéder aux fonctionnalités d’adaptateur personnalisées définies par le fournisseur. Cela permet au fournisseur de définir un ensemble quasiment illimité d’opérations de contrôle pour un appareil. En outre, en choisissant la fonction à implémenter, un fournisseur peut choisir de mettre des opérations de contrôle à la disposition des utilisateurs sans privilèges tout en restreignant les autres opérations aux utilisateurs privilégiés.

Pour plus d’informations sur la création d’adaptateurs, consultez [créer des plug-ins d’adaptateur](creating-adapter-plug-ins.md).

## <a name="adapter-performance-requirements"></a>Exigences en matière de performances de l’adaptateur

Étant donné que l’objectif est une réponse rapide globale, les performances d’un adaptateur ne sont pas spécifiées en termes de limites de temps sur des routines spécifiques. Au lieu de cela, les performances sont spécifiées sous la forme d’un ensemble d’exigences pour l’expérience utilisateur globale.

Deux conditions sont requises :

-   Toute interaction entre l’utilisateur et le système d’exploitation qui implique la biométrie doit se terminer dans les deux secondes. Cet intervalle mesure l’heure de début et de fin que l’utilisateur perçoit du moment où il touche ou le glissement du capteur jusqu’à ce que l’écran de l’appareil affiche un événement. (Par exemple, pendant le déverrouillage, il ne doit pas y avoir plus d’un délai de deux secondes entre l’utilisateur qui touche ou fait glisser le capteur d’empreintes digitales et l’écran de verrouillage qui accuse réception de l’identité de l’utilisateur.)
-   Pour l’affichage initial des vignettes d’informations d’identification sur l’écran de connexion ou de verrouillage, nous autorisons un peu plus de temps (trois secondes, maximum), mais nous préférons encore plus tôt. Plus précisément, la mosaïque doit être visible à l’écran dans un délai de trois secondes après l’apparition du panneau de verrouillage ou de connexion.

Ces nombres ne sont pas arbitraires. De nombreuses études ont montré que les êtres humains ont tendance à rencontrer tout ce qui se passe dans un délai de deux secondes dans le cadre du moment « maintenant ». Si l’événement A et l’événement B se produisent dans un délai de deux secondes l’un de l’autre, les utilisateurs perçoivent ces événements comme étant simultanés. Si les événements sont séparés par plus d’environ trois secondes, les gens pensent qu’il y a un retard : ils estiment que quelque chose est trop long. C’est un problème de la psychologie humaine intégrée.

 

 