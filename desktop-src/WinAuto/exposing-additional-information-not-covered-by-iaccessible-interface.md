---
title: Exposition d’informations supplémentaires non couvertes par l’interface IAccessible
description: En fonction de leurs produits, les développeurs de serveurs peuvent avoir besoin d’exposer des informations ou des fonctionnalités en plus de la prise en charge de Microsoft Active Accessibility.
ms.assetid: c45009ca-6be3-4645-9097-36671a41dfce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3834c60de8f18fd5ec0719919a1cd79e22f451e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095569"
---
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a>Exposition d’informations supplémentaires non couvertes par l’interface IAccessible

En fonction de leurs produits, les développeurs de serveurs peuvent avoir besoin d’exposer des informations ou des fonctionnalités en plus de la prise en charge de Microsoft Active Accessibility. Dans ce cas, collaborez avec les fournisseurs de technologie d’assistance (clients) pour vous assurer qu’ils ajoutent la prise en charge des fonctionnalités.

N’essayez pas d’étendre l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Les interfaces ne peuvent pas être modifiées une fois qu’elles sont publiées. Pour exposer des informations supplémentaires, utilisez une interface personnalisée et exposez-la à l’aide de l’une des techniques suivantes :

-   [Utilisation \_ d’objid NATIVEOM pour exposer une interface de modèle objet natif pour une fenêtre](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [Utilisation de QueryService pour exposer une interface de modèle objet natif pour un objet IAccessible](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

Notez que l’objectif de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) est d’avoir une interface bien définie qui est utilisée par les serveurs et les clients. Avant d’exposer des interfaces personnalisées, veillez à exposer le plus d’informations possible via **IAccessible**.

Vous ne pouvez pas utiliser [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour exposer des interfaces personnalisées. Utilisez **IServiceProvider :: QueryService** comme indiqué dans les procédures suivantes.

 

 