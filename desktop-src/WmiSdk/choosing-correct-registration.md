---
description: WMI prend en charge différents modèles de thread, selon la façon dont le fournisseur est hébergé et le type de fonctionnalité de fournisseur, tel que la classe ou la propriété.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Choix de l’inscription correcte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b66ec0266b5482dcff13a7de05a5bd1414312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533926"
---
# <a name="choosing-correct-registration"></a>Choix de l’inscription correcte

WMI prend en charge différents modèles de thread, selon la façon dont le fournisseur est hébergé et le type de fonctionnalité de fournisseur, tel que la [classe](writing-a-class-provider.md) ou la [propriété](writing-a-property-provider.md). Par exemple, les [*fournisseurs découplés*](gloss-d.md) ne prennent pas en charge tous les types de fonctionnalités du fournisseur. Pour plus d’informations sur les différents modèles d’hébergement et sur la façon de les configurer, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).

## <a name="in-process-providers"></a>Fournisseurs de In-Process

Les fournisseurs in-process s’exécutent dans un processus hôte partagé, Wmiprvse.exe. La plupart des types de fournisseurs in-process utilisent le modèle de cloisonnement multithread (MTA).

Le modèle MTA est pris en charge pour les types de fonctionnalités de fournisseur suivants :

-   [Fournisseur de classes](writing-a-class-provider.md)
-   [Fournisseur d’instance](writing-an-instance-provider.md)
-   [Fournisseur de méthode](writing-a-method-provider.md)
-   [Fournisseur de propriétés](writing-a-property-provider.md)
-   [Fournisseur d’événements](writing-an-event-provider.md)
-   [Fournisseur de consommateur d’événements](writing-an-event-consumer-provider.md)

Le modèle STA (Single-Threaded Apartment) est pris en charge pour certains types de fonctionnalités du fournisseur :

-   [Fournisseur d’instance](writing-an-instance-provider.md)
-   [Fournisseur de méthode](writing-a-method-provider.md)
-   [Fournisseur d’événements](writing-an-event-provider.md)
-   [Fournisseur de consommateur d’événements](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a>Fournisseurs hors processus

Les fournisseurs qui sont hébergés dans un autre hôte de service partagé prennent en charge la fonctionnalité de fournisseur suivante :

-   [Fournisseur de classes](writing-a-class-provider.md)
-   [Fournisseur d’instance](writing-an-instance-provider.md)
-   [Fournisseur de méthode](writing-a-method-provider.md)
-   [Fournisseur de propriétés](writing-a-property-provider.md)
-   [Fournisseur d’événements](writing-an-event-provider.md)
-   [Fournisseur de consommateur d’événements](writing-an-event-consumer-provider.md)

Pour plus d’informations sur les hôtes de service partagés, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).

## <a name="decoupled-providers"></a>Fournisseurs découplés

Les fournisseurs découplés sont hébergés dans une application. Pour plus d’informations, consultez [incorporation d’un fournisseur dans une application](incorporating-a-provider-in-an-application.md). Les fournisseurs créés à l’aide de WMI dans le .NET Framework sont découplés. Les fournisseurs découplés prennent en charge la fonctionnalité de fournisseur suivante :

-   [Fournisseur d’instance](writing-an-instance-provider.md)
-   [Fournisseur de méthode](writing-a-method-provider.md)
-   [Fournisseur d’événements](writing-an-event-provider.md)
-   [Fournisseur de consommateur d’événements](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’un fournisseur WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Hébergement et sécurité du fournisseur](provider-hosting-and-security.md)
</dt> </dl>

 

 



