---
description: Origin est une description générale de l’endroit où la session a démarré, par exemple si elle est externe ou interne à un réseau d’entreprise. Pour obtenir \_ la liste des origines prises en charge par TAPI, consultez constantes LINECALLORIGIN.
ms.assetid: d9779438-fd08-495a-ae3d-ffad9b543090
title: Origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a1f4dafd2b4a3ee85b3a05b3c8ab8f95656237b0ad5bf292c53a5bbb2d3bed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002827"
---
# <a name="origin"></a>Origine

Origin est une description générale de l’endroit où la session a démarré, par exemple si elle est externe ou interne à un réseau d’entreprise. Pour obtenir la liste des origines prises en charge par TAPI, consultez [ \_ constantes LINECALLORIGIN](./linecallorigin--constants.md) .

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membre **dwOrigin** de *lpCallInfo*).

**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (membre d'**\_ origine CIL** de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
