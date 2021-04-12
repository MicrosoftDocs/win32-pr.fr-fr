---
description: L’identification connectée identifie le tiers qui a été réellement connecté à. Cela peut être différent de l’identification appelée si l’appel a été détourné.
ms.assetid: 3f9ba728-8e78-4f1f-a0c1-76799fd62c9d
title: Identification connectée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59fdb2f11b27bf9281b381170aa0d5b5ab027088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321202"
---
# <a name="connected-identification"></a>Identification connectée

L’identification connectée identifie le tiers qui a été réellement connecté à. Cela peut être différent de l’identification appelée si l’appel a été détourné.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwConnectedIDFlags**, **dwConnectedIDSize**, **dwConnectedIDOffset**, **dwConnectedIDNameSize** et **dwConnectedIDNameOffset** *).*

**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIL \_ CONNECTEDIDNAME** membre de [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
