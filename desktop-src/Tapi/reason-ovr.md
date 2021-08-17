---
description: Les raisons possibles d’une session entrante, telles que celle qui a été transférée, sont répertoriées dans les \_ constantes LINECALLREASON.
ms.assetid: 94cc1a79-7ce4-47ec-bdd8-ee7f0d9f48ed
title: Raison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4be431b5d3918714a11fb95411a8d5503a47f9e6d4cd462f9a208f00dfb96c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139952"
---
# <a name="reason"></a>Motif

Les raisons possibles d’une session entrante, telles que celle qui a été transférée, sont répertoriées dans les [ \_ constantes LINECALLREASON](./linecallreason--constants.md).

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

**TAPI 2. x : **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** membre dwReason** de *lpCallInfo*)

**TAPI 3. x : **[**ITCallInfo :: obten \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** \_ raison CIL** membre de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))

 

 
