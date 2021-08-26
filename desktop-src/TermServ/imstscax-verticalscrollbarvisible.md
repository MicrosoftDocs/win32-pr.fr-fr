---
title: IMsTscAx propriété VerticalScrollBarVisible
description: Indique si le contrôle affiche une barre de défilement verticale.
ms.assetid: b31e2db3-b367-4900-a2c6-51fd794341c2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété VerticalScrollBarVisible
- Services Bureau à distance de la propriété VerticalScrollBarVisible, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété VerticalScrollBarVisible
topic_type:
- apiref
api_name:
- IMsTscAx.VerticalScrollBarVisible
- IMsTscAx.get_VerticalScrollBarVisible
- IMsRdpClient.VerticalScrollBarVisible
- IMsRdpClient.get_VerticalScrollBarVisible
- IMsRdpClient2.VerticalScrollBarVisible
- IMsRdpClient2.get_VerticalScrollBarVisible
- IMsRdpClient3.VerticalScrollBarVisible
- IMsRdpClient3.get_VerticalScrollBarVisible
- IMsRdpClient4.VerticalScrollBarVisible
- IMsRdpClient4.get_VerticalScrollBarVisible
- IMsRdpClient5.VerticalScrollBarVisible
- IMsRdpClient5.get_VerticalScrollBarVisible
- IMsRdpClient6.VerticalScrollBarVisible
- IMsRdpClient6.get_VerticalScrollBarVisible
- IMsRdpClient7.VerticalScrollBarVisible
- IMsRdpClient7.get_VerticalScrollBarVisible
- IMsRdpClient8.VerticalScrollBarVisible
- IMsRdpClient8.get_VerticalScrollBarVisible
- IMsRdpClient9.VerticalScrollBarVisible
- IMsRdpClient9.get_VerticalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b09cf6c50c4724cc7374163998af7b7bab77d61f4c16177fedddcc9b1e8de055
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125259"
---
# <a name="imstscaxverticalscrollbarvisible-property"></a>IMsTscAx :: VerticalScrollBarVisible, propriété

Indique si le contrôle affiche une barre de défilement verticale.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_VerticalScrollBarVisible(
  [out] BOOL *pfVScrollVisible
);
```



## <a name="property-value"></a>Valeur de la propriété

La valeur de ce paramètre est **true** si la barre de défilement verticale est visible, et **false** dans le cas contraire.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Remarques

Le contrôle affiche automatiquement une barre de défilement verticale si la hauteur du contrôle actuel est inférieure à la hauteur du bureau.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





