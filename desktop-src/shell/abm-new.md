---
description: Inscrit un nouveau appbar et spécifie l’identificateur de message que le système doit utiliser pour envoyer des messages de notification. Un appbar doit envoyer ce message avant d’envoyer d’autres messages appbar.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: Message ABM_NEW (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fad11e6712d0afd0c1a5e9de07fd3d690800db13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750309"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




