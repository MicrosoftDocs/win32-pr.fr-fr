---
description: Inscrit un nouveau appbar et spécifie l’identificateur de message que le système doit utiliser pour envoyer des messages de notification. Un appbar doit envoyer ce message avant d’envoyer d’autres messages appbar.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: Message ABM_NEW (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400439e6808d40eb74c18fa4219109a0abca1973cdac4dcb9de5154384fd0071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460966"
---
# <a name="abm_new-message"></a>ABM \_ un nouveau message

Inscrit un nouveau appbar et spécifie l’identificateur de message que le système doit utiliser pour envoyer des messages de notification. Un appbar doit envoyer ce message avant d’envoyer d’autres messages appbar.


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pabd* 
</dt> <dd>

Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) qui contient le handle de fenêtre et l’identificateur de message du nouvel appbar. Vous devez spécifier les membres **cbSize**, **HWND** et **uCallbackMessage** lors de l’envoi de ce message. tous les autres membres sont ignorés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** si une erreur se produit ou si le appbar est déjà inscrit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




