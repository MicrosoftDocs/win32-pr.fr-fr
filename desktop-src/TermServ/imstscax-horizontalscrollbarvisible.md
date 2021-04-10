---
title: IMsTscAx propriété HorizontalScrollBarVisible
description: Indique si le contrôle a affiché une barre de défilement horizontale.
ms.assetid: d3c22c5f-321f-476e-bcdb-224eb988a7bb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété HorizontalScrollBarVisible
- Services Bureau à distance de la propriété HorizontalScrollBarVisible, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété HorizontalScrollBarVisible
topic_type:
- apiref
api_name:
- IMsTscAx.HorizontalScrollBarVisible
- IMsTscAx.get_HorizontalScrollBarVisible
- IMsRdpClient.HorizontalScrollBarVisible
- IMsRdpClient.get_HorizontalScrollBarVisible
- IMsRdpClient2.HorizontalScrollBarVisible
- IMsRdpClient2.get_HorizontalScrollBarVisible
- IMsRdpClient3.HorizontalScrollBarVisible
- IMsRdpClient3.get_HorizontalScrollBarVisible
- IMsRdpClient4.HorizontalScrollBarVisible
- IMsRdpClient4.get_HorizontalScrollBarVisible
- IMsRdpClient5.HorizontalScrollBarVisible
- IMsRdpClient5.get_HorizontalScrollBarVisible
- IMsRdpClient6.HorizontalScrollBarVisible
- IMsRdpClient6.get_HorizontalScrollBarVisible
- IMsRdpClient7.HorizontalScrollBarVisible
- IMsRdpClient7.get_HorizontalScrollBarVisible
- IMsRdpClient8.HorizontalScrollBarVisible
- IMsRdpClient8.get_HorizontalScrollBarVisible
- IMsRdpClient9.HorizontalScrollBarVisible
- IMsRdpClient9.get_HorizontalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08fa2abb97a28af013e5791bcbd643f3f479d5c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032786"
---
# <a name="imstscaxhorizontalscrollbarvisible-property"></a>IMsTscAx :: HorizontalScrollBarVisible, propriété

Indique si le contrôle a affiché une barre de défilement horizontale.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_HorizontalScrollBarVisible(
  [out] BOOL *pfHScrollVisible
);
```



## <a name="property-value"></a>Valeur de la propriété

La valeur de ce paramètre est **true** si la barre de défilement horizontale est visible, et **false** dans le cas contraire.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Le contrôle affiche automatiquement une barre de défilement horizontale si la largeur du contrôle est inférieure à la largeur du bureau.

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

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)
</dt> </dl>

 

 





