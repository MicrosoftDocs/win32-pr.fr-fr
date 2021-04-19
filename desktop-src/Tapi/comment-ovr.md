---
description: Une application peut définir un commentaire pendant l’initiation d’une session. Les commentaires sont souvent utilisés à des fins de journalisation.
ms.assetid: 46201166-de07-47b8-8d9a-c8edb7fb6926
title: Commentaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12b9530e2fbb0c08b928607a71ee6b14cbdf6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524074"
---
# <a name="comment"></a>Commentaire

Une application peut définir un commentaire pendant l’initiation d’une session. Les commentaires sont souvent utilisés à des fins de journalisation.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membres **dwCommentSize** et **dwCommentOffset** de *lpCallInfo*).

**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIL \_ Comment** membre de [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
