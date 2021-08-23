---
description: L’identification connectée identifie le tiers qui a été réellement connecté à. Cela peut être différent de l’identification appelée si l’appel a été détourné.
ms.assetid: 3f9ba728-8e78-4f1f-a0c1-76799fd62c9d
title: Identification connectée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df3052287658d06372f30c9d1fa5ae79c13ab0f7ff10dd9c134b7f730439cc6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867756"
---
# <a name="connected-identification"></a>Identification connectée

L’identification connectée identifie le tiers qui a été réellement connecté à. Cela peut être différent de l’identification appelée si l’appel a été détourné.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwConnectedIDFlags**, **dwConnectedIDSize**, **dwConnectedIDOffset**, **dwConnectedIDNameSize** et **dwConnectedIDNameOffset** *).*

**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIL \_ CONNECTEDIDNAME** membre de [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
