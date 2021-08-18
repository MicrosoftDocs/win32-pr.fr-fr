---
description: La méthode SplitAt fractionne l’objet à l’heure spécifiée.
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: 'IAMTimelineSplittable :: SplitAt, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cdcedc25cf7f0998c6eac11de63f6e0d329e2ca8500576e0ad9e69cfc0bb3067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052409"
---
# <a name="iamtimelinesplittablesplitat-method"></a>IAMTimelineSplittable :: SplitAt, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SplitAt` méthode fractionne l’objet à l’heure spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SplitAt(
   REFERENCE_TIME Time
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Time* 
</dt> <dd>

Heure à laquelle fractionner l’objet, par rapport au début de la chronologie, en unités de 100 nanosecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Il peut prendre les valeurs suivantes :



| Code de retour                                                                                   | Description                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | Rien à fractionner.<br/>                       |
| <dl> <dt>**\_OK**</dt> </dl>          | Réussite.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | L’objet n’existe pas pour l’instant.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                    |



 

## <a name="remarks"></a>Remarques

Si vous fractionnez une source, un effet ou une transition, cette méthode crée un deuxième objet du même type. L’objet d’origine est tronqué à l’heure de fractionnement spécifiée et le nouvel objet remplace la partie tronquée. Le nouvel objet hérite de toutes les mêmes propriétés. Dans un objet source, la méthode fractionne également tous les effets qui tombent sur l’heure de fractionnement.

L’appel de cette méthode sur une piste fractionne toutes les sources, effets et transitions contenus dans la piste à l’heure de fractionnement spécifiée. Elle ne crée pas de deuxième piste. (Une piste commence à l’heure zéro et s’étend à l’infini.)

Pour une piste, si l’heure de fractionnement est postérieure à tout dans la piste, la méthode retourne S \_ false. Pour tout autre objet, si l’heure de fractionnement n’est pas comprise dans l’objet, la méthode retourne E \_ INVALIDARG.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMTimelineSplittable**](iamtimelinesplittable.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




