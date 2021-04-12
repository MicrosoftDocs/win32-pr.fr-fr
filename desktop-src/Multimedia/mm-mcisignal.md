---
title: Message MM_MCISIGNAL (mmsystem. h)
description: Le \_ message mm MCISIGNAL est envoyé à une fenêtre pour avertir une application qu’un périphérique MCI a atteint une position définie dans une commande de signal précédente ( \_ signal MCI).
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- Message MM_MCISIGNAL Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MCISIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d42d4d39f31b82c7461a5bd8d8561b0da1b6bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385020"
---
# <a name="mm_mcisignal-message"></a>MM \_ message MCISIGNAL

Le message **mm \_ MCISIGNAL** est envoyé à une fenêtre pour avertir une application qu’un périphérique MCI a atteint une position définie dans une commande de [**signal**](signal.md) précédente ( [**\_ signal MCI**](mci-signal.md)).


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*
</dt> <dd>

Identificateur de l’appareil initialisant le message de signal.

</dd> <dt>

<span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*
</dt> <dd>

Valeur transmise dans le membre **dwUserParm** de la structure de **paramètre de \_ \_ signal \_ MCI DGV** lorsque la commande de **signal** a défini cette fonction de rappel. Il peut également contenir la valeur de position.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>MMSYSTEM. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Messages MCI](mci-messages.md)
</dt> <dt>

[**témoin**](signal.md)
</dt> </dl>

 

 





