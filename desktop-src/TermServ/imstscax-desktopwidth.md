---
title: IMsTscAx propriété DesktopWidth
description: Spécifie la largeur, en pixels, du contrôle actif sur le Bureau à distance initial.
ms.assetid: 3b349f6c-d068-4047-b8b5-29d022894729
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété DesktopWidth
- Services Bureau à distance de la propriété DesktopWidth, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété DesktopWidth
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopWidth
- IMsTscAx.get_DesktopWidth
- IMsTscAx.put_DesktopWidth
- IMsRdpClient.DesktopWidth
- IMsRdpClient.get_DesktopWidth
- IMsRdpClient.put_DesktopWidth
- IMsRdpClient2.DesktopWidth
- IMsRdpClient2.get_DesktopWidth
- IMsRdpClient2.put_DesktopWidth
- IMsRdpClient3.DesktopWidth
- IMsRdpClient3.get_DesktopWidth
- IMsRdpClient3.put_DesktopWidth
- IMsRdpClient4.DesktopWidth
- IMsRdpClient4.get_DesktopWidth
- IMsRdpClient4.put_DesktopWidth
- IMsRdpClient5.DesktopWidth
- IMsRdpClient5.get_DesktopWidth
- IMsRdpClient5.put_DesktopWidth
- IMsRdpClient6.DesktopWidth
- IMsRdpClient6.get_DesktopWidth
- IMsRdpClient6.put_DesktopWidth
- IMsRdpClient7.DesktopWidth
- IMsRdpClient7.get_DesktopWidth
- IMsRdpClient7.put_DesktopWidth
- IMsRdpClient8.DesktopWidth
- IMsRdpClient8.get_DesktopWidth
- IMsRdpClient8.put_DesktopWidth
- IMsRdpClient9.DesktopWidth
- IMsRdpClient9.get_DesktopWidth
- IMsRdpClient9.put_DesktopWidth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16cd1391c6aeb27d9ec0f87317b06e9084337fbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508554"
---
# <a name="imstscaxdesktopwidth-property"></a>IMsTscAx ::D propriété esktopWidth

Spécifie la largeur, en pixels, du contrôle actif sur le Bureau à distance initial.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_DesktopWidth(
  [in]  LONG newVal
);

HRESULT get_DesktopWidth(
  [out] LONG *pVal
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouvelle largeur, en pixels.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

La définition de la propriété **DesktopWidth** est facultative, mais elle doit être définie avant d’appeler la méthode [**Connect**](imstscax-connect.md) . Si la largeur du Bureau n’est pas spécifiée ou si elle est définie sur zéro, la largeur du Bureau est définie sur la largeur du contrôle. Les valeurs minimales et maximales dépendent de la version du système d’exploitation du client Bureau à distance.

<dl> <dt>

<span id="_"></span>Windows 8/Windows Server 2012
</dt> <dd>

200 minimum, 8192 maximum

</dd> <dt>

<span id="_"></span>Windows 7/Windows Server 2008
</dt> <dd>

200 minimum, 2048 maximum

</dd> <dt>

Windows Vista
</dt> <dd>

200 minimum, 1200 maximum

</dd> </dl>

Après l’établissement d’une connexion, toute modification apportée à la largeur du contrôle ne modifie pas la largeur du Bureau à distance. Au lieu de cela, le contrôle affiche des barres de défilement ou centre le Bureau à distance, le cas échéant. Pour modifier la taille du Bureau d’une connexion active, utilisez la méthode [**IMsRdpClient8 :: reconnect**](imsrdpclient8-reconnect.md) .

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
</dt> </dl>

 

 





