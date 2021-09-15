---
description: La méthode CreateObject de Microsoft. Windows. L’objet ActCtx crée un objet dans le contexte du manifeste actuel.
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: ActCtx. CreateObject, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.CreateObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2b4c4393d59ea5ab711dbf4bb1f4c88d906b6582
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238085"
---
# <a name="actctxcreateobject-method"></a>ActCtx. CreateObject, méthode

La méthode **CreateObject** de [**Microsoft. Windows.**](microsoft-windows-actctx-object.md)L’objet ActCtx crée un objet dans le contexte du manifeste actuel.

## <a name="syntax"></a>Syntaxe


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Arguments* 
</dt> <dd>

Chaîne qui spécifie le type d’objet à créer. Par exemple, un ProgID COM.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx est défini en tant que 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetObject, méthode**](getobject.md)
</dt> </dl>

 

 




