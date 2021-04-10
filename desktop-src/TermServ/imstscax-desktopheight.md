---
title: IMsTscAx propriété DesktopHeight
description: Spécifie la hauteur, en pixels, du contrôle actuel sur le Bureau à distance initial.
ms.assetid: 7071053b-bdd1-408b-ab69-965c504fafb0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété DesktopHeight
- Services Bureau à distance de la propriété DesktopHeight, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété DesktopHeight
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopHeight
- IMsTscAx.get_DesktopHeight
- IMsTscAx.put_DesktopHeight
- IMsRdpClient.DesktopHeight
- IMsRdpClient.get_DesktopHeight
- IMsRdpClient.put_DesktopHeight
- IMsRdpClient2.DesktopHeight
- IMsRdpClient2.get_DesktopHeight
- IMsRdpClient2.put_DesktopHeight
- IMsRdpClient3.DesktopHeight
- IMsRdpClient3.get_DesktopHeight
- IMsRdpClient3.put_DesktopHeight
- IMsRdpClient4.DesktopHeight
- IMsRdpClient4.get_DesktopHeight
- IMsRdpClient4.put_DesktopHeight
- IMsRdpClient5.DesktopHeight
- IMsRdpClient5.get_DesktopHeight
- IMsRdpClient5.put_DesktopHeight
- IMsRdpClient6.DesktopHeight
- IMsRdpClient6.get_DesktopHeight
- IMsRdpClient6.put_DesktopHeight
- IMsRdpClient7.DesktopHeight
- IMsRdpClient7.get_DesktopHeight
- IMsRdpClient7.put_DesktopHeight
- IMsRdpClient8.DesktopHeight
- IMsRdpClient8.get_DesktopHeight
- IMsRdpClient8.put_DesktopHeight
- IMsRdpClient9.DesktopHeight
- IMsRdpClient9.get_DesktopHeight
- IMsRdpClient9.put_DesktopHeight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb75467b35703420ce49fd99ea032b139d721505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942413"
---
# <a name="imstscaxdesktopheight-property"></a>IMsTscAx ::D propriété esktopHeight

Spécifie la hauteur, en pixels, du contrôle actuel sur le Bureau à distance initial.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_DesktopHeight(
  [in]  LONG newVal
);

HRESULT get_DesktopHeight(
  [out] LONG *pVal
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouvelle hauteur, en pixels.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

La définition de la propriété **DesktopHeight** est facultative, mais elle doit être définie avant d’appeler la méthode [**Connect**](imstscax-connect.md) . Si la hauteur du Bureau n’est pas spécifiée ou si a la valeur zéro, la hauteur du Bureau est définie sur la hauteur du contrôle. Les valeurs minimales et maximales dépendent de la version du système d’exploitation du client Bureau à distance.

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

Après l’établissement d’une connexion, toute modification apportée à la hauteur du contrôle ne modifie pas la hauteur du Bureau à distance. Au lieu de cela, le contrôle affiche des barres de défilement ou centre le Bureau à distance, le cas échéant. Pour modifier la taille du Bureau d’une connexion active, utilisez la méthode [**IMsRdpClient8 :: reconnect**](imsrdpclient8-reconnect.md) .

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

 

 





