---
title: Message EM_GETTOUCHOPTIONS (RichEdit. h)
description: Récupère les options tactiles associées à un contrôle RichEdit.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- EM_GETTOUCHOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812d37de1972c6da205944d9913dc3fa046c205d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033099"
---
# <a name="em_gettouchoptions-message"></a>\_Message GETTOUCHOPTIONS em

Récupère les options tactiles associées à un contrôle RichEdit.


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Options tactiles à récupérer. Il peut avoir l’une des valeurs suivantes.



| Valeur                                                                                                                                                                        | Signification                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**RTO \_ SHOWHANDLES**</dt> </dl>          | Récupère si les pinceaux tactiles sont visibles.<br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**RTO \_ DISABLEHANDLES**</dt> </dl> | La récupération de cet indicateur n’est pas implémentée.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur de l’option spécifiée par le paramètre *wParam* . Il est différent de zéro si *wParam* est **RTO \_ SHOWHANDLES** et que les pinceaux tactiles sont visibles ; sinon,.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTOUCHOPTIONS em**](em-settouchoptions.md)
</dt> </dl>

 

 





