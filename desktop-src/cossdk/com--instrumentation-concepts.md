---
description: Le service d’instrumentation COM+ vous permet de créer vos propres programmes de gestion et de journalisation des événements COM+ lorsque vous souhaitez afficher diverses mesures de performances pour vos composants COM+.
ms.assetid: 07f68734-a382-4fe5-86af-90805f61c68d
title: Concepts d’instrumentation COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d86b5dbb7bb3f6db14d82220d88c58dbc0a8255
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915700"
---
# <a name="com-instrumentation-concepts"></a>Concepts d’instrumentation COM+

Le service d’instrumentation COM+ vous permet de créer vos propres programmes de gestion et de journalisation des événements COM+ lorsque vous souhaitez afficher diverses mesures de performances pour vos composants COM+. l’instrumentation com+ peut également être utilisée pour configurer des événements définis par l’utilisateur et pour convertir des événements com+ au format d’analyseur de Visual Studio (VSA) lors de la mise à niveau des packages mts qui reçoivent des événements mts.

> [!Note]  
> à partir de Windows Server 2003, seuls les administrateurs ont des privilèges d’accès en lecture aux journaux de suivi pour les événements système.

 

En s’abonnant aux événements publiés par l’éditeur des événements système, les clients peuvent implémenter les [interfaces d’instrumentation com+](com--instrumentation-interfaces.md) pour recevoir des notifications pour diverses mesures de performances de com+, telles que des informations sur des objets com+ spécifiques, des applications com+ et des services com+. Les métriques sont publiées sur le client à l’aide du [service d’événements com+](com--events.md), un système d’événements (LCE) faiblement couplés qui stocke les informations d’événements provenant de différents serveurs de publication dans un magasin d’événements du catalogue com+.

> [!Note]  
> L’instrumentation COM+ ne garantit pas la remise d’un événement.

 

Chaque mesure a un horodateur qui indique l’heure à laquelle la mesure a été générée, et non l’heure à laquelle elle a été distribuée ou reçue. Le client peut corréler l’horodateur et déterminer le coût de l’exécution d’une application COM+, le coût d’une transaction exécutée dans une application COM+, ou le coût d’un appel de méthode au sein d’une application COM+.

Vous pouvez également utiliser le service d’instrumentation COM+ pour filtrer les informations de métriques de performances spécifiques que vous souhaitez afficher. Par exemple, lorsque vous vous abonnez à une interface ou une méthode d’instrumentation COM+, vous pouvez spécifier des propriétés pour l’abonnement dans la structure [**COMSVCSEVENTINFO**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) , telles que l’ID d’application (membre **guidApp** ) ou l’ID de processus (membre **dwPid** ).

Lorsque l’ID d’application est spécifié, vous recevez uniquement les métriques de l’application spécifiée. Lorsque l’ID de processus est spécifié, vous recevez des métriques de l’application serveur spécifiée et des applications de bibliothèque qui sont chargées dans ce processus. L’utilisateur peut spécifier l’ID d’application et l’ID de processus, mais l’ID d’application doit être celui de l’application serveur en cours d’exécution dans le processus avec l’ID de processus spécifié. Si aucun de ces paramètres n’est spécifié, l’utilisateur reçoit des métriques à partir de toutes les applications serveur et de la bibliothèque.

Les métriques d’instrumentation COM+ fournissent suffisamment d’informations pour que l’application de surveillance les mette en corrélation avec les métriques du système d’exploitation pour l’analyse des performances, la planification de la capacité et la modélisation et la prédiction.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interfaces d’instrumentation COM+](com--instrumentation-interfaces.md)
</dt> </dl>

 

 



