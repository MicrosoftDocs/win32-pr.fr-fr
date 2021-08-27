---
description: La propriété de manifeste est utilisée pour définir ou récupérer le contexte d’activation actif.
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: ActCtx. manifest, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.Manifest
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 77d45bd0dc97ed99ee976da4e262ed3d4819b0ec4c744a4e0a8d76b98f5bacd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977229"
---
# <a name="actctxmanifest-property"></a>ActCtx. manifest, propriété

La propriété de **manifeste** est utilisée pour définir ou récupérer le contexte d’activation actif.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Si un contexte d’activation peut être créé avec le fichier manifeste fourni, le script suivant définit la propriété de manifeste et active la constante d’activation spécifiée par le manifeste. Si un contexte d’activation ne peut pas être créé à partir du manifeste, le contexte d’activation reste défini sur le contexte d’activation actuellement actif.

ActCtxObj. manifest = "<*nom du fichier manifeste*>";

Si un contexte d’activation a déjà été créé ou activé, le script suivant définit la propriété de **manifeste** sur le contexte d’activation actuel. Si un contexte d’activation n’a pas été créé ou activé précédemment, définit la propriété de **manifeste** sur une chaîne vide.

« BSTR bstrManifest = ActCtxObj. manifest »

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx est défini en tant que 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



 

 




