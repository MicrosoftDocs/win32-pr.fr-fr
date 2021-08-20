---
title: IMsTscAx propriété ConnectingText
description: Spécifie le texte qui apparaît centré dans le contrôle pendant la connexion du contrôle.
ms.assetid: 9bc82074-988f-491b-80e3-00c3f7ba437a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété ConnectingText
- Services Bureau à distance de la propriété ConnectingText, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété ConnectingText
topic_type:
- apiref
api_name:
- IMsTscAx.ConnectingText
- IMsTscAx.get_ConnectingText
- IMsTscAx.put_ConnectingText
- IMsRdpClient.ConnectingText
- IMsRdpClient.get_ConnectingText
- IMsRdpClient.put_ConnectingText
- IMsRdpClient2.ConnectingText
- IMsRdpClient2.get_ConnectingText
- IMsRdpClient2.put_ConnectingText
- IMsRdpClient3.ConnectingText
- IMsRdpClient3.get_ConnectingText
- IMsRdpClient3.put_ConnectingText
- IMsRdpClient4.ConnectingText
- IMsRdpClient4.get_ConnectingText
- IMsRdpClient4.put_ConnectingText
- IMsRdpClient5.ConnectingText
- IMsRdpClient5.get_ConnectingText
- IMsRdpClient5.put_ConnectingText
- IMsRdpClient6.ConnectingText
- IMsRdpClient6.get_ConnectingText
- IMsRdpClient6.put_ConnectingText
- IMsRdpClient7.ConnectingText
- IMsRdpClient7.get_ConnectingText
- IMsRdpClient7.put_ConnectingText
- IMsRdpClient8.ConnectingText
- IMsRdpClient8.get_ConnectingText
- IMsRdpClient8.put_ConnectingText
- IMsRdpClient9.ConnectingText
- IMsRdpClient9.get_ConnectingText
- IMsRdpClient9.put_ConnectingText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7342e47658e77d9fb29ef03ab1995e5263c78a8e31d2f020852e5fa10864a031
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129671"
---
# <a name="imstscaxconnectingtext-property"></a>IMsTscAx :: ConnectingText, propriété

Spécifie le texte qui apparaît centré dans le contrôle pendant la connexion du contrôle.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ConnectingText(
  [in]  BSTR newVal
);

HRESULT get_ConnectingText(
  [out] BSTR *pConnectingText
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouveau texte affiché.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

Retourne un **HRESULT** différent de zéro si une erreur se produit.

## <a name="remarks"></a>Remarques

Exemple de texte de connexion : « connexion au serveur... ».

La définition de la propriété **ConnectingText** est facultative. S’il n’est pas défini, le contrôle apparaît vide avant l’établissement d’une connexion.

Cette propriété ne peut être définie que si le contrôle n’est pas dans l’état connecté. Elle retourne **E \_ Fail** si elle est appelée lorsque le contrôle est connecté. Vous pouvez vérifier si le contrôle est connecté en répondant aux événements de connexion dans [**IMsTscAxEvents**](imstscaxevents-interface.md) ou en examinant la propriété [**Connected**](imstscax-connected.md) .

La méthode de propriété **obtenir \_ ConnectingText** alloue la mémoire requise pour la mémoire tampon vers laquelle pointe le paramètre *pConnectingText* . L’appel d’applications C/C++ doit libérer la mémoire avec un appel à la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . cela n’est pas nécessaire pour les Visual Basic et les clients de script.

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

 

