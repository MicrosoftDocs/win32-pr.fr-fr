---
description: Numéro du Trunk sur lequel l’appel est routé. Ce membre est utilisé pour les appels entrants et sortants.
ms.assetid: e57e1aac-a2f1-42b7-9a0c-c74009a75305
title: Trunk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4afea1387c6d43dc4d9a2f5a6a12f260a8daeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204127"
---
# <a name="trunk"></a>Trunk

Numéro du Trunk sur lequel l’appel est routé. Ce membre est utilisé pour les appels entrants et sortants.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

* * TAPI 2. x : * *[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwTrunk** of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x : * *[**ITCallInfo :: obten \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), appelé avec le membre de **\_ Trunk CIL** de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

 

 
