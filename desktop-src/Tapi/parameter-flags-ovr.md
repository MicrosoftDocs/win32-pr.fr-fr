---
description: Les indicateurs de paramètres fournissent des informations sur divers indicateurs d’État relatifs à une session de communication, par exemple si l’identification de l’appelant doit être bloquée. Pour obtenir \_ la liste des indicateurs définis par TAPI, consultez constantes LINECALLPARAMFLAGS.
ms.assetid: 30511328-a310-42b7-a81e-3ef2abf586ed
title: Indicateurs de paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf663ea4ff6121f3e130f9c2a2e4c3c1f86f8611be8cc3fef3762adc535e84bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959859"
---
# <a name="parameter-flags"></a>Indicateurs de paramètres

Les indicateurs de paramètres fournissent des informations sur divers indicateurs d’État relatifs à une session de communication, par exemple si l’identification de l’appelant doit être bloquée. Pour obtenir la liste des indicateurs définis par TAPI, consultez [ \_ constantes LINECALLPARAMFLAGS](./linecallparamflags--constants.md) .

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membre **dwCallParamFlags** de *lpCallInfo*).

**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLPARAMSFLAGS** membre de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
