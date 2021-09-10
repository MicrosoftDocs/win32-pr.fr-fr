---
title: Message MCIWNDM_SENDSTRING (VFW. h)
description: Le \_ message MCIWNDM SENDSTRING envoie une commande MCI sous forme de chaîne à l’appareil associé à la fenêtre MCIWnd. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSendString.
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- message MCIWNDM_SENDSTRING Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SENDSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36a034a3459803b1652bafed4eb389866add211
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364320"
---
# <a name="mciwndm_sendstring-message"></a>\_Message MCIWNDM SENDSTRING

Le message **MCIWNDM \_ SENDSTRING** envoie une commande MCI sous forme de chaîne à l’appareil associé à la fenêtre MCIWnd. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) .


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="sz"></span><span id="SZ"></span>*SZ*
</dt> <dd>

Commande de chaîne à envoyer à l’appareil MCI.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Le gestionnaire de messages pour **MCIWNDM \_ SENDSTRING** ajoute un alias d’appareil à la commande MCI que vous envoyez à l’appareil. Par conséquent, vous ne devez pas utiliser d’alias dans une commande MCI que vous émettez avec **MCIWNDM \_ SENDSTRING**.

Pour obtenir la chaîne de retour, qui contient le résultat de la commande, envoyez le message [**MCIWNDM \_ RETURNSTRING**](mciwndm-returnstring.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[Chaînes de commande multimédia](multimedia-command-strings.md)
</dt> </dl>

 

 





