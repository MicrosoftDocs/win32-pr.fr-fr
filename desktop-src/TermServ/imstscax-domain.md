---
title: Propriété de domaine IMsTscAx
description: Spécifie le domaine auquel l’utilisateur actuel se connecte.
ms.assetid: 5d9a2048-5f5d-43ca-a8b8-400dac7d7472
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété de domaine
- Services Bureau à distance de propriété de domaine, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété de domaine
topic_type:
- apiref
api_name:
- IMsTscAx.Domain
- IMsTscAx.get_Domain
- IMsTscAx.put_Domain
- IMsRdpClient.Domain
- IMsRdpClient.get_Domain
- IMsRdpClient.put_Domain
- IMsRdpClient2.Domain
- IMsRdpClient2.get_Domain
- IMsRdpClient2.put_Domain
- IMsRdpClient3.Domain
- IMsRdpClient3.get_Domain
- IMsRdpClient3.put_Domain
- IMsRdpClient4.Domain
- IMsRdpClient4.get_Domain
- IMsRdpClient4.put_Domain
- IMsRdpClient5.Domain
- IMsRdpClient5.get_Domain
- IMsRdpClient5.put_Domain
- IMsRdpClient6.Domain
- IMsRdpClient6.get_Domain
- IMsRdpClient6.put_Domain
- IMsRdpClient7.Domain
- IMsRdpClient7.get_Domain
- IMsRdpClient7.put_Domain
- IMsRdpClient8.Domain
- IMsRdpClient8.get_Domain
- IMsRdpClient8.put_Domain
- IMsRdpClient9.Domain
- IMsRdpClient9.get_Domain
- IMsRdpClient9.put_Domain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 498098b57ef5ecb19958f6ef0e082022a92f15bab7f1fbfc74bef62d928e8726
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125429"
---
# <a name="imstscaxdomain-property"></a>IMsTscAx ::D propriété omaine

Spécifie le domaine auquel l’utilisateur actuel se connecte.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Domain(
  [in]  BSTR newVal
);

HRESULT get_Domain(
  [out] BSTR *pDomain
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouveau nom de domaine.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Remarques

La définition de la propriété de **domaine** est facultative. s’il n’est pas défini, l’utilisateur peut choisir un domaine lorsque la boîte de dialogue Windows Logon s’affiche pendant la connexion.

La méthode **obtenir le \_ domaine** alloue la mémoire requise pour la mémoire tampon vers laquelle pointe le paramètre *pDomain* . L’appel d’applications C/C++ doit libérer la mémoire avec un appel à la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . cela n’est pas nécessaire pour les Visual Basic et les clients de script.

Cette propriété ne peut être définie que si le contrôle n’est pas dans l’état connecté. Elle retourne **E \_ Fail** si elle est appelée lorsque le contrôle est connecté. Vous pouvez vérifier si le contrôle est connecté en répondant aux événements de connexion dans [**IMsTscAxEvents**](imstscaxevents-interface.md) ou en examinant la propriété [**Connected**](imstscax-connected.md) .

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

[**Connecté**](imstscax-connected.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

