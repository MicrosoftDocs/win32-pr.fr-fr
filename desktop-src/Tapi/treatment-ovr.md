---
description: Le traitement fait référence à la gestion d’une session entrante qui n’a pas encore reçu de réponse ou qui a été mise en attente, telle que la musique. \_Pour obtenir la liste des traitements définis par l’interface TAPI, consultez constantes LINECALLTREATMENT.
ms.assetid: 0b8d1023-374a-4937-b39c-04043423eb47
title: Traitement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60f29f8848c76029daa7828f40061c828b625ec046dea7fac35159b390a4d106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139742"
---
# <a name="treatment"></a>Traitement

Le traitement fait référence à la gestion d’une session entrante qui n’a pas encore reçu de réponse ou qui a été mise en attente, telle que la musique. Pour obtenir la liste des traitements définis par l’interface TAPI, consultez [ \_ constantes LINECALLTREATMENT](./linecalltreatment--constants.md) .

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

**TAPI 2. x : **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** membre dwCallTreatment** de *lpCallInfo*)

**TAPI 3. x : **[**ITCallInfo :: obten \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** CIL \_ CALLTREATMENT** membre de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))

 

 
