---
description: La méthode CreateObject de l’objet Microsoft. Windows. ActCtx crée un objet dans le contexte du manifeste actuel.
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203383"
---
# <a name="actctxcreateobject-method"></a>ActCtx. CreateObject, méthode

La méthode **CreateObject** de l’objet [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) crée un objet dans le contexte du manifeste actuel.

## <a name="syntax"></a>Syntaxe


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*objectId* 
</dt> <dd>

Chaîne qui spécifie le type d’objet à créer. Par exemple, un ProgID COM.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx est défini en tant que 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetObject, méthode**](getobject.md)
</dt> </dl>

 

 




