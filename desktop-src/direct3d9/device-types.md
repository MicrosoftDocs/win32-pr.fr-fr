---
description: Types d’appareils (Direct3D 9)
ms.assetid: 860f3de2-beaf-4df1-82d0-a4b7508156c2
title: Types d’appareils (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84efe80c022403c36e760860893f3619e1c9356
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317626"
---
# <a name="device-types-direct3d-9"></a>Types d’appareils (Direct3D 9)

## <a name="hal-device"></a>Appareil HAL

Le type d’appareil principal est le périphérique HAL, qui prend en charge la pixellisation accélérée sur le matériel et le traitement du vertex matériel et logiciel. Si l’ordinateur sur lequel votre application s’exécute est équipé d’un adaptateur d’affichage qui prend en charge Direct3D, votre application doit l’utiliser pour les opérations Direct3D. Les périphériques Hal Direct3D implémentent tout ou partie des modules de transformation, d’éclairage et de pixellisation dans le matériel.

Les applications n’accèdent pas directement aux cartes graphiques. Ils appellent des fonctions et des méthodes Direct3D. Direct3D accède au matériel via la couche HAL. Si l’ordinateur sur lequel votre application est exécutée prend en charge la couche HAL, il obtiendra des performances optimales à l’aide d’un périphérique Hal.

Pour créer un périphérique HAL, appelez [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) en utilisant \_ la couche HAL D3DDEVTYPE comme type de périphérique.

## <a name="reference-device"></a>Appareil de référence

Direct3D prend en charge un type d’appareil supplémentaire appelé appareil de référence ou rastériseur de référence. Contrairement à un périphérique logiciel, le rastériseur de référence prend en charge chaque fonctionnalité Direct3D. Ce périphérique est destiné à être utilisé à des fins de débogage et n’est donc disponible que sur les ordinateurs sur lesquels le kit de développement logiciel (SDK) DirectX a été installé. Étant donné que ces fonctionnalités sont implémentées pour des raisons de précision plutôt que de vitesse et sont implémentées dans les logiciels, les résultats ne sont pas très rapides. Le rastériseur de référence utilise des instructions d’UC spéciales à chaque fois que cela est possible, mais il n’est pas destiné aux applications de vente au détail. Utilisez le rastériseur de référence uniquement à des fins de test de fonctionnalités ou de démonstration. Pour créer un appareil de référence, appelez la méthode [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) à l’aide \_ de D3DDEVTYPE REF comme type de périphérique.

## <a name="hal-vs-ref-devices"></a>Appareils HAL et périphériques REF

Les périphériques HAL (Hardware Abstraction Layer) et les appareils REF (rastériseur de référence) sont les deux principaux types de périphériques Direct3D. la première est basée sur le support matériel et est très rapide, mais peut ne pas prendre en charge tout ; tandis que la seconde n’utilise aucune accélération matérielle, elle est très lente, mais est garantie de prendre en charge l’ensemble complet des fonctionnalités Direct3D, de la manière correcte. En général, vous n’avez jamais besoin d’utiliser des périphériques HAL, mais si vous utilisez une fonctionnalité avancée que votre carte graphique ne prend pas en charge, vous devrez peut-être revenir à REF.

L’autre cas où vous voudrez peut-être utiliser REF est si le périphérique HAL produit des résultats inattendus. autrement dit, vous êtes sûr que votre code est correct, mais le résultat n’est pas ce que vous attendez. Le comportement de l’appareil REF est garanti, donc vous pouvez tester votre application sur l’appareil de référence et voir si le comportement étrange se poursuit. Si ce n’est pas le cas, cela signifie que (a) votre application suppose que la carte graphique prend en charge les éléments qu’elle n’a pas, ou (b) qu’il s’agit d’un bogue de pilote. S’il ne fonctionne toujours pas avec l’appareil de référence, il s’agit d’un bogue de l’application.

## <a name="hardware-vs-software-vertex-processing"></a>Traitement du vertex matériel et logiciel

Le traitement du matériel et du vertex logiciel s’applique uniquement aux périphériques HAL. Lorsque vous poussez des vertex dans le pipeline, ceux-ci doivent être transformés (par les matrices universelles, de vue et de projection) et allumés (par D3D’s de lumière intégrée). cette étape de traitement est appelée T&L (pour la transformation & éclairage). Le traitement du vertex matériel signifie que cette opération est effectuée sur le matériel, si le matériel le prend en charge ; Ergo, le traitement du vertex logiciel est un logiciel. La pratique générale consiste à essayer d’abord de créer un appareil matériel T&L et, si cette opération échoue, essayer de le mélanger et, si cela échoue, essayer le logiciel. (Si le logiciel échoue, abandonner et quitter avec une erreur).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
