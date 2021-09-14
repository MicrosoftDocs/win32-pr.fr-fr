---
title: Envoi d’une commande
description: Envoi d’une commande
ms.assetid: 28c38f36-b6a7-44da-95e2-25b3dccefc84
keywords:
- mciSendString fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69536b167b8fde648c3f3743058542d74bd8647
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123558"
---
# <a name="sending-a-command"></a>Envoi d’une commande

L’exemple de fonction suivant envoie la commande [**Play**](play.md) avec les indicateurs « from » et « to » à l’aide de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



 

 