---
title: Méthode IMsRdpDriveCollection RescanDrives
description: Actualise la liste des objets dans la collection. | Méthode IMsRdpDriveCollection RescanDrives
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RescanDrives
- Méthode RescanDrives Services Bureau à distance, interface IMsRdpDriveCollection
- Services Bureau à distance de l’interface IMsRdpDriveCollection, méthode RescanDrives
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.RescanDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2490e3879420701537cd36999ba33fde9ebfaf1e2f93d75550807e552fadacd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606186"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a>IMsRdpDriveCollection :: RescanDrives, méthode

Actualise la liste des objets dans la collection.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RescanDrives(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vboolDynRedir* \[ dans\]
</dt> <dd>

État de redirection par défaut qui sera appliqué aux périphériques ou lecteurs récemment découverts.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, **S \_ OK** est retourné. Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpDriveCollection est défini en tant que 7ff17599-da2c-4677-ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





