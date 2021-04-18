---
description: Quand une application redirige une session, TAPI conserve les informations d’identification relatives à l’emplacement qui a redirigé la session et à l’emplacement vers lequel elle a été redirigée.
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: Identification de la redirection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8316b7d1566a24ead21f7b1fdf2d16b1c48a2b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522746"
---
# <a name="redirect-identification"></a>Identification de la redirection

Quand une application [redirige](redirect-ovr.md) une session, TAPI conserve les informations d’identification relatives à l’emplacement qui a redirigé la session et à l’emplacement vers lequel elle a été redirigée.

La « redirection » fait référence à l’emplacement qui a appelé l’opération de redirection. « Redirection » identifie la nouvelle destination pour la session.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

* * TAPI 2. x : * *[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize** et **dwRedirectingIDNameOffset** membres de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x : * *[**ITCallInfo :: obten \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)appelé avec les **membres CIS \_ REDIRECTIONIDNAME**, **CIS \_ REDIRECTIONIDNUMBER**, **CIS \_ REDIRECTINGIDNAME** ou **CIS \_ REDIRECTINGIDNUMBER** de la [**\_ chaîne CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)

 

 
