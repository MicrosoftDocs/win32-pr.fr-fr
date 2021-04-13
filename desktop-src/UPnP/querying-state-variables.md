---
title: Interrogation des variables d’État
description: L’interface IUPnPService fournit la méthode QueryStateVariable, qui retourne la valeur d’une variable d’état spécifiée.
ms.assetid: 9e8b98b0-488a-4f9c-9ad7-039dbd470486
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a716bbe93c2306eca43b977a42f33a85187f92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309837"
---
# <a name="querying-state-variables"></a>Interrogation des variables d’État

L’interface [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) fournit la méthode [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) , qui retourne la valeur d’une variable d’état spécifiée.

Le Forum UPnP déconseille l’utilisation de [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable). Les créateurs d’appareils ont été encouragés à écrire des actions appropriées pour fournir ces informations. Les créateurs d’appareils ne sont pas tenus d’implémenter **QueryStateVariable**.

Consultez la section [appel d’actions](invoking-actions.md).

 

 




