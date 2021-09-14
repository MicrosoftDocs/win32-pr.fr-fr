---
description: Le privilège fait référence au fait qu’une application possède ou surveille la session.
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Privilège
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2f773edb05afc029a8f9fb6b014cd8a737eef0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095665"
---
# <a name="privilege"></a>Privilège

Le privilège fait référence au fait qu’une application possède ou surveille la session. Si l’application possède la session, elle est autorisée à effectuer diverses opérations de session. Si l’application est uniquement surveillée, elle reçoit des messages d’État et peut accéder aux informations de session, mais toute tentative d’exécution de la plupart des opérations génère une erreur.

Pendant l’initialisation, une application indique à TAPI le niveau de privilège requis pour les adresses. L’interface TAPI offre des sessions entrantes uniquement aux applications qui ont été inscrites pour le propriétaire ou le propriétaire et le privilège de surveillance.

Le privilège d’une application sur une session qu’il crée est toujours propriétaire.

**TAPI 2. x :** Consultez [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **dwCallPrivilege** , membre de [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).

**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir le \_ privilège**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo :: \_ obtenir CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), appelé avec le membre **CIL \_ NUMBEROFOWNERS** ou **CIL \_ NUMBEROFMONITORS** de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

 

 
