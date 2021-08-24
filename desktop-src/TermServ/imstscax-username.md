---
title: Propriété du nom d’utilisateur IMsTscAx
description: Spécifie les informations d’identification d’ouverture de session de nom d’utilisateur.
ms.assetid: 9be25003-b9aa-41bb-a5a9-512546175114
ms.tgt_platform: multiple
keywords:
- Propriété UserName Services Bureau à distance
- Propriété UserName Services Bureau à distance, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété UserName
- Propriété UserName Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété UserName
topic_type:
- apiref
api_name:
- IMsTscAx.UserName
- IMsTscAx.get_UserName
- IMsTscAx.put_UserName
- IMsRdpClient.UserName
- IMsRdpClient.get_UserName
- IMsRdpClient.put_UserName
- IMsRdpClient2.UserName
- IMsRdpClient2.get_UserName
- IMsRdpClient2.put_UserName
- IMsRdpClient3.UserName
- IMsRdpClient3.get_UserName
- IMsRdpClient3.put_UserName
- IMsRdpClient4.UserName
- IMsRdpClient4.get_UserName
- IMsRdpClient4.put_UserName
- IMsRdpClient5.UserName
- IMsRdpClient5.get_UserName
- IMsRdpClient5.put_UserName
- IMsRdpClient6.UserName
- IMsRdpClient6.get_UserName
- IMsRdpClient6.put_UserName
- IMsRdpClient7.UserName
- IMsRdpClient7.get_UserName
- IMsRdpClient7.put_UserName
- IMsRdpClient8.UserName
- IMsRdpClient8.get_UserName
- IMsRdpClient8.put_UserName
- IMsRdpClient9.UserName
- IMsRdpClient9.get_UserName
- IMsRdpClient9.put_UserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 609619a012c9eea865a275bc6ee86cfc06c798ba27902636f9d5f792b8cb0dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770879"
---
# <a name="imstscaxusername-property"></a>IMsTscAx :: UserName, propriété

Spécifie les informations d’identification d’ouverture de session de nom d’utilisateur.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_UserName(
  [in]  BSTR newVal
);

HRESULT get_UserName(
  [out] BSTR *pUserName
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouveau nom d’utilisateur.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Remarques

La définition de la propriété **username** est facultative. si elle n’est pas spécifiée, l’utilisateur peut fournir un nom d’utilisateur lorsque la boîte de dialogue Windows Logon s’affiche pendant la connexion.

Cette propriété ne peut être définie que si le contrôle n’est pas dans l’état connecté. Elle retourne **E \_ Fail** si elle est appelée lorsque le contrôle est connecté. Vous pouvez vérifier si le contrôle est connecté en répondant aux événements de connexion dans [**IMsTscAxEvents**](imstscaxevents-interface.md) ou en examinant la propriété [**Connected**](imstscax-connected.md) .

La méthode de propriété **obtenir le \_ nom d’utilisateur** alloue la mémoire requise pour la mémoire tampon vers laquelle pointe le paramètre *pVersion* . L’appel d’applications C/C++ doit libérer la mémoire avec un appel à la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . cela n’est pas nécessaire pour les Visual Basic et les clients de script.

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

 

