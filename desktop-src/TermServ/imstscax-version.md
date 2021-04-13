---
title: Propriété version de IMsTscAx
description: Spécifie le numéro de version du contrôle actuel.
ms.assetid: 91ddeb4c-9d61-41e7-af96-95b0c4884682
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriétés de version
- Propriété version Services Bureau à distance, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété de version
- Propriété version Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété de version
topic_type:
- apiref
api_name:
- IMsTscAx.Version
- IMsTscAx.get_Version
- IMsRdpClient.Version
- IMsRdpClient.get_Version
- IMsRdpClient2.Version
- IMsRdpClient2.get_Version
- IMsRdpClient3.Version
- IMsRdpClient3.get_Version
- IMsRdpClient4.Version
- IMsRdpClient4.get_Version
- IMsRdpClient5.Version
- IMsRdpClient5.get_Version
- IMsRdpClient6.Version
- IMsRdpClient6.get_Version
- IMsRdpClient7.Version
- IMsRdpClient7.get_Version
- IMsRdpClient8.Version
- IMsRdpClient8.get_Version
- IMsRdpClient9.Version
- IMsRdpClient9.get_Version
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff25f274d1f076c9c4119648ccb9cc6d82f43b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465322"
---
# <a name="imstscaxversion-property"></a>IMsTscAx :: version, propriété

Spécifie le numéro de version du contrôle actuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Version(
  [out] BSTR *pVersion
);
```



## <a name="property-value"></a>Valeur de la propriété

Numéro de version.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Cette méthode alloue la mémoire requise pour la mémoire tampon vers laquelle pointe le paramètre *pVersion* . L’appel d’applications C/C++ doit libérer la mémoire avec un appel à la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . Cela n’est pas nécessaire pour les Visual Basic et les clients de script.

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

 

