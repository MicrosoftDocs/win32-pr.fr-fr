---
description: Gestion des erreurs dans WinHTTP
ms.assetid: 96bceda2-ca96-4f88-ab38-35021889c2dd
title: Gestion des erreurs dans WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72dac7775934684afe6cc9c9d54bc36bb8f3295c91deef7449e9a00600bc687e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899183"
---
# <a name="error-handling-in-winhttp"></a>Gestion des erreurs dans WinHTTP

Toutes les fonctions de l’API WinHTTP ne signalent pas les erreurs de la même façon.

Certaines fonctions, telles que [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts), retournent une valeur **booléenne** qui indique un échec lorsque la **valeur est false**. Si la **valeur false** est retournée, les appelants intéressés par l’erreur doivent appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). si **GetLastError** est appelé lorsque la fonction succès (retournée n’importe quoi mais **false**), la valeur retournée est imprévisible et peut changer entre les versions Windows, les Service packs ou même entre les appels à la même fonction.

Certaines fonctions, telles que [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect), retournent un pseudo-handle [HINTERNET](hinternet-handles-in-winhttp.md) . Ces fonctions sont exactement les mêmes, sauf que l’échec est indiqué en retournant la **valeur null**. Si la **valeur null** est retournée, les appelants intéressés par l’erreur doivent appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). si **GetLastError** est appelé lorsque la fonction succès (retournée n’importe quoi mais **NULL**), la valeur retournée est imprévisible et peut changer entre les versions Windows, les Service packs ou même entre les appels à la même fonction.

Certaines fonctions, telles que [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult), retournent un code d’erreur **DWORD** et il n’est pas nécessaire d’appeler d’autres fonctions pour obtenir plus d’informations sur l’erreur. Pour ces fonctions, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) ne doit pas être appelé. si **GetLastError** est appelé, indépendamment de la réussite ou de l’échec de la fonction, la valeur retournée est imprévisible et peut changer entre les versions Windows, les Service packs ou même entre les appels à la même fonction.

 

 
