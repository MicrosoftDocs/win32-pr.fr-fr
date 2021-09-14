---
title: TfClientId (msctf. h)
description: Le type de données TfClientId est utilisé pour identifier le client.
ms.assetid: 984dc390-6e15-4491-8c06-77c27c5bdd6f
keywords:
- TfClientId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffba8e1d5ea3c8114d9f567c3829141dd8902dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008805"
---
# <a name="tfclientid"></a>TfClientId

Le type de données **TfClientId** est utilisé pour identifier le client.


```C++
typedef DWORD TfClientId;
```



## <a name="remarks"></a>Notes

Dans TSF, les applications et les services de texte sont généralement appelés clients. Chaque client reçoit un identificateur unique qu’il utilise pour s’identifier lui-même lors de l’appel de différentes méthodes de gestionnaire TSF. Cet identificateur est du type **TfClientId** .

Le type de données **TfClientId** est fourni par le gestionnaire TSF. Une application obtient une valeur **TfClientId** lorsqu’elle appelle [ITfThreadMgr :: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate). La valeur TfClientId d’un service de texte est transmise à la méthode [ITfTextInputProcessor :: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) . Tout objet qui ne correspond pas aux catégories ci-dessus peut obtenir un identificateur de client en appelant [ITfClientId :: GetClientId](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications Windows 2000 Professional \[ desktop apps \| UWP\]<br/>                    |
| Serveur minimal pris en charge<br/> | applications de bureau Windows 2000 Server apps-applications \[ \| UWP\]<br/>                          |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 Professional<br/>                                      |
| En-tête<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITfClientId::GetClientId**](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)
</dt> <dt>

[**ITfTextInputProcessor :: Activate**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[**ITfThreadMgr :: Activate**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> </dl>

 

 





