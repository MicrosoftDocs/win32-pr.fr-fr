---
description: La méthode EnableTransitions active ou désactive toutes les transitions dans la chronologie.
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: 'IAMTimeline :: EnableTransitions, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableTransitions
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c05d3a00a57b8008789b83b16eee155eea974e6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234072"
---
# <a name="iamtimelineenabletransitions-method"></a>IAMTimeline :: EnableTransitions, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `EnableTransitions` méthode active ou désactive toutes les transitions dans la chronologie. Si les transitions sont désactivées, les moteurs de rendu les traitent comme des coupes. autrement dit, la sortie rendue passe instantanément d’une piste à la suivante. Le point de coupe par défaut est à mi-chemin dans la durée de la transition. Vous pouvez modifier le point de coupe en appelant la méthode [**IAMTimelineTrans :: SetCutPoint**](iamtimelinetrans-setcutpoint.md) sur la transition. Les transitions désactivées ne sont pas supprimées de la chronologie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnableTransitions(
   BOOL fEnabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fEnabled* 
</dt> <dd>

Valeur booléenne qui spécifie s’il faut activer ou désactiver les transitions. Si la **valeur est true**, les transitions sont activées. Si la **valeur est false**, les transitions sont désactivées.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




