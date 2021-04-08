---
description: La méthode GetObject obtient une instance d’un objet Microsoft. Windows. ActCtx existant.
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
ms.openlocfilehash: 11b71d8d40d947472612c91f70e9956aa7798806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750964"
---
# <a name="actctxgetobject-method"></a>ActCtx. GetObject, méthode

La méthode **GetObject** obtient une instance d’un objet [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) existant.

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

Chaîne obligatoire qui indique l’objet. Le nom doit figurer dans le Registre sous **HKEY \_ local \_ machine** \\ **Microsoft** \\ **Visual Studio** \\ **6,0** \\ **<package>** \\ **Automation**.

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

[**CreateObject, méthode**](createobject.md)
</dt> </dl>

 

 




