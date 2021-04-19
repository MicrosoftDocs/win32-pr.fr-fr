---
description: Les mémoires tampons spécifiques à l’appareil peuvent faire partie d’une implémentation de fournisseurs de services d’opérations étendues. Le fournisseur de services définit la signification de ces mémoires tampons.
ms.assetid: 5783f892-ec11-4340-afad-44f2ef55fd18
title: Mémoire tampon spécifique à l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628ee93e4f88fc733e744b3c52af3c0a1c31ecf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518469"
---
# <a name="device-specific-buffer"></a>Mémoire tampon spécifique à l’appareil

Les mémoires tampons spécifiques à l’appareil peuvent faire partie de l’implémentation d’opérations étendues d’un fournisseur de services. Le fournisseur de services définit la signification de ces mémoires tampons.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membres **dwDevSpecificSize** et **dwDevSpecificOffset** de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).

**TAPI 3. x :** Consultez [**ITCallInfo :: GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer) (**CIM \_ DEVSPECIFICBUFFER** membre de [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).

 

 
