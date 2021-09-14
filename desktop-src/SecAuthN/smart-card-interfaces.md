---
description: Une interface de carte à puce se compose d’un ensemble prédéfini de services disponibles au sein d’une carte à puce, des protocoles nécessaires pour appeler les services et de toute hypothèse relative au contexte des services.
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: Interfaces de carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f11f619e69cafa484e209c3346357aa5a031d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324770"
---
# <a name="smart-card-interfaces"></a>Interfaces de carte à puce

Une interface de [*carte à puce*](../secgloss/s-gly.md) se compose d’un ensemble prédéfini de services disponibles au sein d’une *carte à puce*, des protocoles nécessaires pour appeler les services et de toute hypothèse relative au contexte des services.

En ce qui concerne les cartes à puce, le terme « interface » est semblable à la façon dont il est utilisé dans COM, qui, à son tour, est similaire au concept de l’identificateur d’application ISO 7816/5, mais avec une portée différente.

Chaque interface de carte à puce est identifiée par un GUID. Par exemple, une interface peut être définie pour fournir des informations de biorythme à son détenteur. Si une carte à puce donnée prend en charge ce service, elle peut demander à prendre en charge ce GUID d’interface. À l’aide des GUID d’interface, une application peut rechercher un ensemble particulier d’interfaces, en localisant une carte qui prend en charge ce jeu pour terminer une tâche.

Bien qu’une interface ait un GUID, elle peut être implémentée différemment sur différentes cartes. Par exemple, l’interface de biorythme mentionnée ci-dessus peut avoir plusieurs implémentations différentes, mais toutes sont référencées à l’aide du même GUID. Les différentes implémentations ne modifient pas l’interaction entre l’application et la carte à puce ; Toutefois, l’interaction entre le [*fournisseur de services*](../secgloss/c-gly.md) et les cartes à puce peut varier en fonction de l’implémentation de l’interface.

L’ensemble des interfaces prises en charge par une carte à puce est défini lors de l’introduction de la carte à puce (voir [Présentation des cartes à puce au système](introducing-smart-cards-to-the-system.md)).

 

 
