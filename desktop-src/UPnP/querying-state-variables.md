---
title: Interrogation des variables d’État
description: L’interface IUPnPService fournit la méthode QueryStateVariable, qui retourne la valeur d’une variable d’état spécifiée.
ms.assetid: 9e8b98b0-488a-4f9c-9ad7-039dbd470486
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aa3baecf7bd1fd01537f3a461d1e615f539c6c7ce633621a736419942bcd4ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137182"
---
# <a name="querying-state-variables"></a>Interrogation des variables d’État

L’interface [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) fournit la méthode [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) , qui retourne la valeur d’une variable d’état spécifiée.

Le Forum UPnP déconseille l’utilisation de [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable). Les créateurs d’appareils ont été encouragés à écrire des actions appropriées pour fournir ces informations. Les créateurs d’appareils ne sont pas tenus d’implémenter **QueryStateVariable**.

Consultez la section [appel d’actions](invoking-actions.md).

 

 




