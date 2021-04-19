---
title: Propriété IMsRdpClientSecuredSettings2 PCB
description: Spécifie le paramètre d’objet BLOB de préconnexion à utiliser avant la connexion pour la transmission au serveur. | Propriété IMsRdpClientSecuredSettings2 PCB
ms.assetid: e2ddd9fd-d868-4fc5-835d-0f4db5da71e3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété PCB
- Services Bureau à distance de propriété PCB, interface IMsRdpClientSecuredSettings2
- Services Bureau à distance de l’interface IMsRdpClientSecuredSettings2, propriété PCB
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings2.PCB
- IMsRdpClientSecuredSettings2.get_PCB
- IMsRdpClientSecuredSettings2.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99b9a04a854f218fcbe1735ec6271aa4a58edba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523793"
---
# <a name="imsrdpclientsecuredsettings2pcb-property"></a>IMsRdpClientSecuredSettings2 ::P propriété CB

Spécifie le paramètre d’objet BLOB de préconnexion à utiliser avant la connexion pour la transmission au serveur.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *bstrPCB
);
```



## <a name="property-value"></a>Valeur de la propriété

Paramètre PCB.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md)
</dt> </dl>

 

 





