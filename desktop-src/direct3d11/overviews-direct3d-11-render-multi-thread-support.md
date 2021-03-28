---
title: Comment vérifier la prise en charge des pilotes
description: Cette rubrique montre comment déterminer si les fonctionnalités de multithreading (y compris la création de ressources et les listes de commandes) sont prises en charge pour l’accélération matérielle.
ms.assetid: f577357c-c2e5-4e58-9870-2e995bdc6782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae42bbb3eedb76d049479839d497a79db81b5697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990612"
---
# <a name="how-to-check-for-driver-support"></a>Procédure : vérifier la prise en charge des pilotes

Cette rubrique montre comment déterminer si les fonctionnalités de multithreading (y compris la [création de ressources](overviews-direct3d-11-render-multi-thread-intro.md) et les [listes de commandes](overviews-direct3d-11-render-multi-thread-command-list.md)) sont prises en charge pour l’accélération matérielle.

Pour les applications, il est recommandé de vérifier la prise en charge du matériel graphique du multithread. Si le matériel et le pilote ne prennent pas en charge la création d’objets multithread, les performances peuvent être limitées des manières suivantes :

-   La création de plusieurs objets (même de différents types) en même temps peut être limitée.
-   La création d’un objet lors du rendu des commandes graphiques à l’aide d’un [contexte immédiat](overviews-direct3d-11-render-multi-thread-render.md) peut être limitée. Par exemple, si le matériel ne prend pas en charge le multithreading, une application doit éviter de créer sur un thread d’arrière-plan un objet qui nécessite beaucoup de temps pour la création. Une opération de création qui prend beaucoup de temps peut bloquer le rendu immédiat du contexte et accroître le risque d’interruption de la fréquence d’images visuelles.

Le runtime prend en charge les listes de multithreads et de commandes, indépendamment de la prise en charge des pilotes et du matériel ; s’il n’existe pas de prise en charge du matériel et des pilotes pour les multithreads ou les listes de commandes, le runtime émulera les fonctionnalités. Pour plus d’informations sur le multithreading, consultez [Introduction au multithreading dans Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md).

**Pour vérifier la prise en charge des pilotes pour le multithreading :**

1.  Initialisez un objet d’interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) . Par défaut, le multithreading est activé.
2.  Appelez [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Transmettez la valeur de **\_ \_ Threading de la fonctionnalité d3d11** au paramètre *Feature* , transmettez la structure de thread de données de la [**\_ fonctionnalité \_ \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) au paramètre *pFeatureSupportData* et transmettez la taille de la structure de thread de données de la **\_ fonctionnalité \_ \_ d3d11** au paramètre *FeatureSupportDataSize* .
3.  Si la méthode [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) réussit, la structure de [**\_ \_ \_ Threading de données de la fonctionnalité d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) que vous avez passée à l’étape précédente sera initialisée avec les informations relatives à la prise en charge du multithreading.
    -   Si **DriverConcurrentCreates** a la **valeur true**, un pilote peut créer plusieurs ressources en même temps (simultanément) sur des threads différents.

        Si **DriverCommandLists** a la **valeur true**, le pilote prend en charge les listes de commandes. Autrement dit, les commandes de rendu émises par un contexte immédiat peuvent être simultanées avec la création d’objets sur des threads distincts avec un faible risque d’interruption de la fréquence d’images.

    -   Si **DriverConcurrentCreates** a la **valeur false**, un pilote ne prend pas en charge la création simultanée, ce qui signifie que la quantité d’accès concurrentiel possible est extrêmement limitée. Le matériel graphique ne peut pas créer d’objets de types différents sur des threads différents simultanueously. En outre, le matériel graphique ne peut pas utiliser un contexte immédiat pour émettre des commandes de rendu alors que le matériel graphique tente de créer une ressource sur un autre thread.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Traitement multithread](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




