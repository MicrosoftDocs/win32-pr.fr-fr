---
title: Identificateurs de clients
description: Identificateurs de clients
ms.assetid: 69ff159c-9264-4958-a712-4aa50db6e48e
keywords:
- Text Services Framework (TSF), identificateurs client
- TSF (Text Services Framework), identificateurs client
- services de texte, identificateurs de clients
- Applications compatibles TSF, identificateurs client
- identificateurs de clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f37b230eed1f47ad3e31a5831bddaf8634837c1173806deb084c1e3a4d08790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117953907"
---
# <a name="client-identifiers"></a>Identificateurs de clients

## <a name="applications"></a>Applications

Une application obtient son identificateur client en appelant [ITfThreadMgr :: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).

## <a name="text-services"></a>Services de texte

Un service de texte obtient son identificateur client lorsque la méthode text service [ITfTextInputProcessor :: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) est appelée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ITfThreadMgr :: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> <dt>

[ITfTextInputProcessor :: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> </dl>

 

 




