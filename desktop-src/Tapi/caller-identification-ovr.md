---
description: L’identification de l’appelant fournit des informations sur le tiers appelant lors de la réception d’une session entrante. Une application utilise généralement ces données dans le cadre d’un message d’État à un utilisateur.
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: Identification de l’appelant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93513e3d94fac9c550b23651b3987bc794905beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866593"
---
# <a name="caller-identification"></a>Identification de l’appelant

L’identification de l’appelant fournit des informations sur le tiers appelant lors de la réception d’une session entrante. Une application utilise généralement ces données dans le cadre d’un message d’État à un utilisateur.

Ces informations ne sont pas toujours disponibles immédiatement. Une application qui souhaite utiliser ces informations et qui a vérifié que le fournisseur de services est pris en charge doit vérifier plusieurs fois avant de supposer que les informations ne sont pas disponibles.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset** et **dwCallerIDAddressType** , membres de *lpCallInfo*).

**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLERIDADDRESSTYPE** membre de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo :: obtenir \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ CALLERIDNAME** et **CIS \_ CALLERIDNAME** members de [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
