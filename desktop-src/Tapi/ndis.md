---
description: La classe de périphérique NDIS se compose d’appareils qui peuvent être associés à des pilotes MAC (Media Access Control) NDIS (Network Driver Interface Specification) pour prendre en charge les communications réseau. Vous accédez à ces appareils à l’aide de fonctions.
ms.assetid: 98cdd929-0bd7-4509-b2f5-4edd8d6a8080
title: NDIS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0be1a69f98f9a4ff8cdc2f8ea173b208c0011d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518342"
---
# <a name="ndis"></a>NDIS

La classe de périphérique NDIS se compose d’appareils qui peuvent être associés à des pilotes MAC (Media Access Control) NDIS (Network Driver Interface Specification) pour prendre en charge les communications réseau. Vous accédez à ces appareils à l’aide de fonctions.

Les fonctions [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) et [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplissent une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **dwStringFormat** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ces membres supplémentaires :

``` syntax
HANDLE  hDevice;          // NDIS connection identifier
CHAR    szDeviceType[1];  // name of device 
```

Le membre **hDevice** est l’identificateur à passer à un Mac, tel que le Mac asynchrone pour la mise en réseau à distance, pour associer une connexion réseau à l’appel/la connexion modem. Le membre **szDeviceType** est une chaîne se terminant par un caractère null qui spécifie le nom de l’appareil associé à l’identificateur.

 

 



