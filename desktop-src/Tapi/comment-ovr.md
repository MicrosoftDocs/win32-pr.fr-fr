---
description: Une application peut définir un commentaire pendant l’initiation d’une session. Les commentaires sont souvent utilisés à des fins de journalisation.
ms.assetid: 46201166-de07-47b8-8d9a-c8edb7fb6926
title: Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 757570651315e0d4e9b313af9e926daf12cd25f3a6415037aaf92079bff5b824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118868077"
---
# <a name="comment"></a>Comment

Une application peut définir un commentaire pendant l’initiation d’une session. Les commentaires sont souvent utilisés à des fins de journalisation.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (membres **dwCommentSize** et **dwCommentOffset** de *lpCallInfo*).

**TAPI 3. x :** Consultez [**ITCallInfo :: obtenir \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIL \_ Comment** membre de [**CALLINFO \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
