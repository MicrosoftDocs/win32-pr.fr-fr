---
title: IMsRdpClient2 propriété ConnectedStatusText
description: Contient le texte affiché dans la zone cliente du contrôle pendant que le contrôle est dans l’état connecté.
ms.assetid: c3d8433b-2fb0-413d-88a3-667149f858ba
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété ConnectedStatusText
- Services Bureau à distance de la propriété ConnectedStatusText, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété ConnectedStatusText
topic_type:
- apiref
api_name:
- IMsRdpClient2.ConnectedStatusText
- IMsRdpClient2.get_ConnectedStatusText
- IMsRdpClient2.put_ConnectedStatusText
- IMsRdpClient3.ConnectedStatusText
- IMsRdpClient3.get_ConnectedStatusText
- IMsRdpClient3.put_ConnectedStatusText
- IMsRdpClient4.ConnectedStatusText
- IMsRdpClient4.get_ConnectedStatusText
- IMsRdpClient4.put_ConnectedStatusText
- IMsRdpClient5.ConnectedStatusText
- IMsRdpClient5.get_ConnectedStatusText
- IMsRdpClient5.put_ConnectedStatusText
- IMsRdpClient6.ConnectedStatusText
- IMsRdpClient6.get_ConnectedStatusText
- IMsRdpClient6.put_ConnectedStatusText
- IMsRdpClient7.ConnectedStatusText
- IMsRdpClient7.get_ConnectedStatusText
- IMsRdpClient7.put_ConnectedStatusText
- IMsRdpClient8.ConnectedStatusText
- IMsRdpClient8.get_ConnectedStatusText
- IMsRdpClient8.put_ConnectedStatusText
- IMsRdpClient9.ConnectedStatusText
- IMsRdpClient9.get_ConnectedStatusText
- IMsRdpClient9.put_ConnectedStatusText
- IMsRdpClient10.ConnectedStatusText
- IMsRdpClient10.get_ConnectedStatusText
- IMsRdpClient10.put_ConnectedStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd6ee2ac155aa3fc4873ee1a5eb890774b50978
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414625"
---
# <a name="imsrdpclient2connectedstatustext-property"></a>IMsRdpClient2 :: ConnectedStatusText, propriété

Contient le texte affiché dans la zone cliente du contrôle pendant que le contrôle est dans l’état connecté.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ConnectedStatusText(
  [in]  BSTR newVal
);

HRESULT get_ConnectedStatusText(
  [out] BSTR *pConnectedStatusText
);
```



## <a name="property-value"></a>Valeur de la propriété

La propriété **ConnectedStatusText** contient le texte affiché dans la zone cliente du contrôle pendant que le contrôle est dans l’état connecté.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Texte à afficher dans la zone cliente du contrôle pendant que le contrôle est dans l’état connecté. Il s’agit du texte qui est visible, par exemple, lorsque l’utilisateur bascule le contrôle en mode plein écran dans un navigateur Web, un scénario qui laisse une partie du contrôle hébergé dans le navigateur.

La méthode **obtenir \_ ConnectedStatusText** alloue la mémoire requise pour la mémoire tampon vers laquelle pointe le paramètre *pConnectedStatusText* . L’appel d’applications C/C++ doit libérer la mémoire avec un appel à la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . cela n’est pas nécessaire pour les Visual Basic et les clients de script.

Cette propriété ne peut pas être définie lorsque le contrôle est connecté. Vous pouvez vérifier si le contrôle est connecté en appelant la méthode [**IMsTscAx :: \_ Connect Connected**](imstscax-connected.md) .

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient2 est défini en tant que e7e17dc4-3b71-4BA7-a8e6-281ffadca28f<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

