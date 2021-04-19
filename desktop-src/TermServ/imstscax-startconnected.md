---
title: IMsTscAx propriété StartConnected
description: Indique si le contrôle établira la connexion au serveur de l’hôte de session Bureau à distance Bureau à distance dès le démarrage.
ms.assetid: cf2956c0-be4f-4f80-a14b-253ae8117824
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété StartConnected
- Services Bureau à distance de la propriété StartConnected, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété StartConnected
topic_type:
- apiref
api_name:
- IMsTscAx.StartConnected
- IMsTscAx.get_StartConnected
- IMsTscAx.put_StartConnected
- IMsRdpClient.StartConnected
- IMsRdpClient.get_StartConnected
- IMsRdpClient.put_StartConnected
- IMsRdpClient2.StartConnected
- IMsRdpClient2.get_StartConnected
- IMsRdpClient2.put_StartConnected
- IMsRdpClient3.StartConnected
- IMsRdpClient3.get_StartConnected
- IMsRdpClient3.put_StartConnected
- IMsRdpClient4.StartConnected
- IMsRdpClient4.get_StartConnected
- IMsRdpClient4.put_StartConnected
- IMsRdpClient5.StartConnected
- IMsRdpClient5.get_StartConnected
- IMsRdpClient5.put_StartConnected
- IMsRdpClient6.StartConnected
- IMsRdpClient6.get_StartConnected
- IMsRdpClient6.put_StartConnected
- IMsRdpClient7.StartConnected
- IMsRdpClient7.get_StartConnected
- IMsRdpClient7.put_StartConnected
- IMsRdpClient8.StartConnected
- IMsRdpClient8.get_StartConnected
- IMsRdpClient8.put_StartConnected
- IMsRdpClient9.StartConnected
- IMsRdpClient9.get_StartConnected
- IMsRdpClient9.put_StartConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bda77a06723a6df63055374a3fc96cb80f7654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510939"
---
# <a name="imstscaxstartconnected-property"></a>IMsTscAx :: StartConnected, propriété

Indique si le contrôle établira la connexion au serveur de l’hôte de session Bureau à distance Bureau à distance dès le démarrage.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_StartConnected(
  [in]  BOOL fStartConnected
);

HRESULT get_StartConnected(
  [out] BOOL *pfStartConnected
);
```



## <a name="property-value"></a>Valeur de la propriété

Affectez la valeur **true** à ce paramètre si le contrôle doit se connecter immédiatement au démarrage, ou **false** dans le cas contraire.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Cette propriété est particulièrement utile lorsque les propriétés de contrôle sont définies dans la liste de paramètres d’une <OBJECT> balise, plutôt qu’à l’aide d’appels de script.

Cette propriété ne peut être utilisée que si le nom du serveur est également spécifié à l’aide de la propriété de serveur. Ce paramètre doit être défini avant le démarrage du contrôle, par exemple, en l’incluant dans la liste des paramètres d’une <OBJECT> balise lors de l’utilisation du contrôle à partir d’une page Web.

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

[Incorporation du contrôle Bureau à distance ActiveX dans une page Web](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





