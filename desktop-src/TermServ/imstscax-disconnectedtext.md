---
title: IMsTscAx propriété DisconnectedText
description: Spécifie le texte qui apparaît centré dans le contrôle avant qu’une connexion ne soit terminée.
ms.assetid: ec7efe7a-8fb9-4c45-8e16-78951365de13
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété DisconnectedText
- Services Bureau à distance de la propriété DisconnectedText, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété DisconnectedText
topic_type:
- apiref
api_name:
- IMsTscAx.DisconnectedText
- IMsTscAx.get_DisconnectedText
- IMsTscAx.put_DisconnectedText
- IMsRdpClient.DisconnectedText
- IMsRdpClient.get_DisconnectedText
- IMsRdpClient.put_DisconnectedText
- IMsRdpClient2.DisconnectedText
- IMsRdpClient2.get_DisconnectedText
- IMsRdpClient2.put_DisconnectedText
- IMsRdpClient3.DisconnectedText
- IMsRdpClient3.get_DisconnectedText
- IMsRdpClient3.put_DisconnectedText
- IMsRdpClient4.DisconnectedText
- IMsRdpClient4.get_DisconnectedText
- IMsRdpClient4.put_DisconnectedText
- IMsRdpClient5.DisconnectedText
- IMsRdpClient5.get_DisconnectedText
- IMsRdpClient5.put_DisconnectedText
- IMsRdpClient6.DisconnectedText
- IMsRdpClient6.get_DisconnectedText
- IMsRdpClient6.put_DisconnectedText
- IMsRdpClient7.DisconnectedText
- IMsRdpClient7.get_DisconnectedText
- IMsRdpClient7.put_DisconnectedText
- IMsRdpClient8.DisconnectedText
- IMsRdpClient8.get_DisconnectedText
- IMsRdpClient8.put_DisconnectedText
- IMsRdpClient9.DisconnectedText
- IMsRdpClient9.get_DisconnectedText
- IMsRdpClient9.put_DisconnectedText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4768e639cbfb1543e06c03f2d9e6566d0adb147e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742125"
---
# <a name="imstscaxdisconnectedtext-property"></a>IMsTscAx ::D propriété isconnectedText

Spécifie le texte qui apparaît centré dans le contrôle avant qu’une connexion ne soit terminée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_DisconnectedText(
  [in]  BSTR newVal
);

HRESULT get_DisconnectedText(
  [out] BSTR *pDisconnectedText
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouveau texte affiché.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

La définition de la propriété **DisconnectedText** est facultative. S’il n’est pas spécifié, le contrôle apparaît vide avant l’établissement d’une connexion.

Cette propriété ne peut être définie que si le contrôle n’est pas dans l’état connecté. La méthode retourne **E \_ Fail** si elle est appelée après la connexion du contrôle. Vous pouvez vérifier si le contrôle est connecté en répondant aux événements de connexion dans [**IMsTscAxEvents**](imstscaxevents-interface.md) ou en examinant la propriété [**Connected**](imstscax-connected.md) .

Cette méthode alloue la mémoire requise pour la mémoire tampon vers laquelle pointe le paramètre *pDisconnectedText* . L’appel d’applications C/C++ doit libérer la mémoire avec un appel à la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . Cela n’est pas nécessaire pour les Visual Basic et les clients de script.

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

 

