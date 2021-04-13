---
title: Utilisation de la boîte de dialogue connexions
description: La fonction WNetConnectionDialog crée une boîte de dialogue qui permet à l’utilisateur de parcourir les ressources réseau et de s’y connecter.
ms.assetid: ef375004-e426-4dee-b318-b470721116fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f69d0f32772e614d60598853af620ae3c6452f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315683"
---
# <a name="using-the-connections-dialog-box"></a>Utilisation de la boîte de dialogue connexions

La fonction [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) crée une boîte de dialogue qui permet à l’utilisateur de parcourir les ressources réseau et de s’y connecter. Vous pouvez également appeler la fonction [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) pour créer une boîte de dialogue de connexion. **WNetConnectionDialog1** requiert une structure [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) .

La fonction [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) crée une boîte de dialogue qui permet à l’utilisateur de se déconnecter des ressources réseau.

L’exemple de code suivant montre comment appeler la fonction **WNetConnectionDialog** pour créer une boîte de dialogue qui affiche les ressources de disque. Si l’appel échoue, l’exemple appelle un gestionnaire d’erreurs défini par l’application.


```C++
DWORD dwResult; 
//
// Call the WNetConnectionDialog function.
//
dwResult = WNetConnectionDialog(hwnd, RESOURCETYPE_DISK);
//
// Call an application-defined error handler 
//  to process errors.
//
if(dwResult != NO_ERROR) 
{
    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetConnectionDialog"); 
    return FALSE; 
}
```



Pour plus d’informations sur l’utilisation d’un gestionnaire d’erreurs défini par l’application, consultez [récupération des erreurs réseau](retrieving-network-errors.md).

 

 