---
description: Un périphérique Direct3D est le composant de rendu de Direct3D. Il encapsule et stocke l’état de rendu. En outre, un appareil Direct3D effectue des transformations et des opérations d’éclairage, et pixellise une image sur une surface.
ms.assetid: b592edb8-351a-4a82-9ff7-8a69d82723bc
title: Périphériques Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07726069b952ba99d608e5f36df8e1fb7745cd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200733"
---
# <a name="direct3d-devices-direct3d-9"></a>Périphériques Direct3D (Direct3D 9)

Un périphérique Direct3D est le composant de rendu de Direct3D. Il encapsule et stocke l’état de rendu. En outre, un appareil Direct3D effectue des transformations et des opérations d’éclairage, et pixellise une image sur une surface.

-   [XPDM et WDDM](xpdm-vs-wddm.md)
-   [Types d’appareils (Direct3D 9)](device-types.md)
-   [Création d’un appareil (Direct3D 9)](creating-a-device.md)
-   [Mode fenêtre/Full-Screen (Direct3D 9)](windowed-vs-full-screen-mode.md)
-   [Sélection d’un appareil (Direct3D 9)](selecting-a-device.md)
-   [Appareils perdus (Direct3D 9)](lost-devices.md)
-   [Détermination de la prise en charge matérielle (Direct3D 9)](determining-hardware-support.md)
-   [Traitement des données de vertex (Direct3D 9)](processing-vertex-data.md)
-   [Primitives](primitives.md)

De manière architecturale, les périphériques Direct3D contiennent un module de transformation, un module d’éclairage et un module de pixellisation, comme le montre le diagramme suivant.

![diagramme de l’architecture des appareils Direct3D](images/d3ddev.png)

Direct3D prend actuellement en charge deux types principaux de périphériques Direct3D :

-   Un appareil Hal avec la pixellisation et l’ombrage accélérés par le matériel avec traitement des vertex matériel et logiciel
-   Un appareil de référence

Vous pouvez considérer ces appareils comme deux pilotes distincts. Les logiciels et les périphériques de référence sont représentés par des pilotes logiciels et le périphérique Hal est représenté par un pilote matériel. La méthode la plus courante pour tirer parti de ces appareils consiste à utiliser le périphérique Hal pour l’expédition des applications et l’appareil de référence pour le test des fonctionnalités. Ils sont fournis par des tiers pour émuler des appareils particuliers, par exemple un matériel de développement qui n’a pas encore été publié.

Le périphérique Direct3D créé par une application doit correspondre aux fonctionnalités du matériel sur lequel l’application s’exécute. Direct3D offre des fonctionnalités de rendu, soit en accédant à du matériel 3D installé sur l’ordinateur, soit en émulant les fonctionnalités du matériel 3D dans le logiciel. Par conséquent, Direct3D fournit des appareils pour l’accès au matériel et l’émulation de logiciel.

Les appareils à accélération matérielle offrent des performances bien supérieures à celles des périphériques logiciels. Le type d’unité Hal est disponible sur tous les adaptateurs graphiques pris en charge par Direct3D. Dans la plupart des cas, les applications ciblent des ordinateurs dotés d’une accélération matérielle et s’appuient sur l’émulation logicielle pour prendre en charge les ordinateurs de niveau inférieur.

À l’exception de l’appareil de référence, les périphériques logiciels ne prennent pas toujours en charge les mêmes fonctionnalités qu’un périphérique matériel. Les applications doivent toujours interroger les fonctionnalités de l’appareil pour déterminer quelles sont les fonctionnalités prises en charge.

Étant donné que le comportement du logiciel et des périphériques de référence fournis avec Direct3D 9 est identique à celui du périphérique HAL, le code de l’application créé pour fonctionner avec le périphérique Hal fonctionnera avec le logiciel ou les appareils de référence sans modification. Notez que, si le logiciel fourni ou le comportement de l’appareil de référence est identique à celui du périphérique HAL, les fonctionnalités de l’appareil varient et un périphérique logiciel particulier peut implémenter un ensemble de fonctionnalités bien plus petit.

## <a name="behaviors"></a>Comportements

Direct3D vous permet de spécifier le comportement d’un appareil, ainsi que le type de l’appareil. La méthode [**IDirect3D9 :: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) active une combinaison d’un ou plusieurs indicateurs de comportement pour contrôler les comportements globaux du périphérique Direct3D. Ces comportements spécifient ce qui est et ne sont pas conservés dans la partie Runtime de Direct3D, et les types d’appareils spécifient le pilote à utiliser. Bien que certaines combinaisons de comportements d’appareil ne soient pas valides, il est possible d’utiliser tous les comportements d’appareil avec tous les types d’appareils. Par exemple, il est possible de spécifier D3DDEVTYPE \_ SW sur un appareil créé avec D3DCREATE \_ PUREDEVICE.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main](getting-started.md)
</dt> </dl>

 

 
