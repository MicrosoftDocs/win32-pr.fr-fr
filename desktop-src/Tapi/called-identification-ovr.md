---
description: L’identification appelée identifie l’adresse de destination d’origine d’une session. Dans les situations où une session a été redirigée, transférée ou transférée, elle est différente de l’identification connectée.
ms.assetid: a03286eb-83a9-4170-b514-e8899fd04c74
title: Identification appelée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c751b54d167aace808ddd6003810aa0062102dcb064e3b8ab4252a6c6230a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117947667"
---
# <a name="called-identification"></a>Identification appelée

L’identification appelée identifie l’adresse de destination d’origine d’une session. Dans les situations où une session a été redirigée, transférée ou transférée, elle est différente de l' [identification connectée](connected-identification-ovr.md).

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCalledIDFlags**, **dwCalledIDSize**, **dwCalledIDOffset**, **dwCalledIDNameSize**, **dwCalledIDNameOffset** et **dwCalledIDAddressType** , membres de *lpCallInfo*).

**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLEDIDADDRESSTYPE** membre de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo :: obtenir \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ CALLEDIDNAME** et **CIS \_ CALLEDIDNAME** members de [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
