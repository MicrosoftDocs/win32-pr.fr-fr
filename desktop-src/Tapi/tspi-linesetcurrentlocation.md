---
description: Cette \_ fonction TSPI lineSetCurrentLocation est obsolète. L’interface TAPI a appelé cette fonction lorsque l’utilisateur (à l’aide de la boîte de dialogue Propriétés de la numérotation) ou une application (à l’aide de la fonction lineSetCurrentLocation) a modifié l’emplacement de traduction des adresses.
ms.assetid: acd9f05b-88ae-439a-95c0-d1e8779a32fe
title: TSPI_lineSetCurrentLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa78427bc4892fd0460b60bcb90f5fef43a38f002368c7ca7251cb1ce611c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012119"
---
# <a name="tspi_linesetcurrentlocation"></a>TSPI \_ lineSetCurrentLocation

Cette \_ fonction TSPI lineSetCurrentLocation est obsolète. L’interface TAPI a appelé cette fonction lorsque l’utilisateur (à l’aide de la boîte de dialogue Propriétés de la **numérotation** ) ou une application (à l’aide de la fonction [**lineSetCurrentLocation**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) ) a modifié l’emplacement de traduction des adresses.

À l’heure actuelle, une modification de l’emplacement de traduction aboutit à un \_ message DEVSTATE de ligne avec *dwParam1* défini sur LINEDEVSTATE \_ TRANSLATECHANGE.

 

 
