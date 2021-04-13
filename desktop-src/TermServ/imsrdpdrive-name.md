---
title: Propriété IMsRdpDrive Name
description: Récupère le nom du lecteur.
ms.assetid: 5aabb7df-fd46-48aa-ad1d-51da45495782
ms.tgt_platform: multiple
keywords:
- Propriété Name Services Bureau à distance
- Name, propriété Services Bureau à distance, IMsRdpDrive, interface
- Services Bureau à distance de l’interface IMsRdpDrive, propriété Name
topic_type:
- apiref
api_name:
- IMsRdpDrive.Name
- IMsRdpDrive.get_Name
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38eeb0f6112983f508bb43ba69d721aeb52c314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465990"
---
# <a name="imsrdpdrivename-property"></a>IMsRdpDrive :: Name, propriété

Récupère le nom du lecteur.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Name(
  [out] BSTR *pName
);
```



## <a name="property-value"></a>Valeur de la propriété

Nom du lecteur.

## <a name="error-codes"></a>Codes d’erreur

Si la méthode est réussie, **S \_ OK** est retourné. Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDrive est défini en tant que d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

 





