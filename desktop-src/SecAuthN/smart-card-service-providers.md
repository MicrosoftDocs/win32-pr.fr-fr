---
description: Les fournisseurs de services de carte à puce (SCSP) fournissent un accès aux fonctionnalités de carte à puce.
ms.assetid: f214385f-3e65-4175-925c-3d1dc4060185
title: Fournisseurs de services de carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57cd16787985a1e8f92105ce61aed4b9532bff806aabb7d8ad4bdd407d807014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917383"
---
# <a name="smart-card-service-providers"></a>Fournisseurs de services de carte à puce

Les fournisseurs de services de carte à puce (SCSP) fournissent un accès aux fonctionnalités de [*carte à puce*](../secgloss/s-gly.md) . Ils peuvent fournir un accès à une capacité unique, par exemple les fournisseurs de services de base fournis par le kit de développement logiciel (SDK) de carte à puce, ou ils peuvent fournir un accès à plusieurs fonctionnalités pour accomplir une tâche plus complexe.

Les fournisseurs de services fournissent un accès via des interfaces COM. Le kit de développement logiciel (SDK) de carte à puce fournit les interfaces COM utilisées par ses propres fournisseurs de services de base, ainsi que plusieurs interfaces d’application qui peuvent être utilisées lors du développement de fournisseurs de services personnalisés.



| Rubrique                                                                                   | Description                                            |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Fournisseurs de services de base](base-service-providers.md)<br/>                         | Fournisseurs de services de base.<br/>                     |
| [Génération d’une commande APDU ISO7816-4](building-an-iso7816-4-apdu-command.md)<br/> | Ajout de fonctionnalités à un fournisseur de services.<br/> |
| [Fournisseur de services de wrappers de fournisseur](vendor-wrapper-service-provider.md)<br/>       | Exemple de wrapper de fournisseur.<br/>                   |



 

Pour obtenir une vue d’ensemble de toutes les interfaces COM fournies par le kit de développement logiciel (SDK) de carte à puce (fournisseur de services de base et interfaces d’application), consultez [interfaces de carte à puce](smart-card-interfaces.md).

 

 
