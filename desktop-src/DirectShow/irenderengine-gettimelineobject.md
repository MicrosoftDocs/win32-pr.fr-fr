---
description: La méthode GetTimelineObject récupère la chronologie que le moteur de rendu utilise actuellement.
ms.assetid: 74398f85-07b2-42fa-bb4f-a1e7e1669e3f
title: 'IRenderEngine :: GetTimelineObject, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aab8e9a5f77affc464763b1c5a5045eaa4fc042a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006600"
---
# <a name="irenderenginegettimelineobject-method"></a>IRenderEngine :: GetTimelineObject, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetTimelineObject` méthode récupère la chronologie que le moteur de rendu utilise actuellement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTimelineObject(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppTimeline* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IAMTimeline**](iamtimeline.md) de la chronologie. Elle reçoit la valeur **null** s’il n’y a pas de chronologie.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                            | Description                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Réussite.<br/>                            |
| <dl> <dt>**\_pointeur E**</dt> </dl>              | Pointeur non valide.<br/>                    |
| <dl> <dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt> </dl> | Le moteur de rendu n’a pas pu s’initialiser.<br/> |



 

## <a name="remarks"></a>Notes

En cas de retour, si la valeur de *\* ppTimeline* est non **null**, l’interface **IAMTimeline** a un nombre de références en suspens. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

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

[**Interface IRenderEngine**](irenderengine.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




