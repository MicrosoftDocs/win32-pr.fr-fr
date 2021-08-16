---
description: Le type \_ de données d’initialisation de la négociation est une valeur spéciale de type DWORD.
ms.assetid: ce978913-47a1-4387-bd1b-1795aaf82dd7
title: INITIALIZE_NEGOTIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24763b9214dcffab99c83f24028e451a33d70dd7e4210f4eff64b0c39306d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762776"
---
# <a name="initialize_negotiation"></a>INITIALiser la \_ négociation

Le type de données **d’initialisation de la \_ négociation** est une valeur spéciale de type **DWORD**. Il peut être passé comme paramètre *dwDeviceID* dans les fonctions [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) et [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) . Cela indique que l’interface TAPI peut négocier un numéro de version de l’interface TSPI indépendamment des appareils spécifiques.

 

 
