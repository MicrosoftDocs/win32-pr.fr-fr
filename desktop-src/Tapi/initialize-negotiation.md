---
description: Le type \_ de données d’initialisation de la négociation est une valeur spéciale de type DWORD.
ms.assetid: ce978913-47a1-4387-bd1b-1795aaf82dd7
title: INITIALIZE_NEGOTIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a55879a0952d3f8b5e268ec6a01a666bdbf5ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753420"
---
# <a name="initialize_negotiation"></a>INITIALiser la \_ négociation

Le type de données **d’initialisation de la \_ négociation** est une valeur spéciale de type **DWORD**. Il peut être passé comme paramètre *dwDeviceID* dans les fonctions [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) et [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) . Cela indique que l’interface TAPI peut négocier un numéro de version de l’interface TSPI indépendamment des appareils spécifiques.

 

 
