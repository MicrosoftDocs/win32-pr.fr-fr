---
description: La méthode GetObject obtient une instance d’un Microsoft existant. Windows. Objet ActCtx.
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: ActCtx. GetObject, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.GetObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: a102fdae74232fa9a67c4b9455050bcdba32a219d8a66180ae8bc6ce6cb96c8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885279"
---
# <a name="actctxgetobject-method"></a>ActCtx. GetObject, méthode

La méthode **GetObject** obtient une instance d’un [**Microsoft. Windows existant. Objet ActCtx**](microsoft-windows-actctx-object.md) .

## <a name="syntax"></a>Syntaxe


```JScript
ActCtx.GetObject(
  bstrName
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrName,* 
</dt> <dd>

Chaîne obligatoire qui indique l’objet. le nom doit figurer dans le registre sous **HKEY \_ LOCAL \_ MACHINE** \\ **Microsoft** \\ **Visual Studio** \\ **6,0** \\ **<package>** \\ **Automation**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx est défini en tant que 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CreateObject, méthode**](createobject.md)
</dt> </dl>

 

 




