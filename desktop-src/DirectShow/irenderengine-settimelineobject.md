---
description: La méthode SetTimelineObject définit la chronologie à utiliser par le moteur de rendu.
ms.assetid: 9b60b148-9768-43ba-a986-a96838c4d2bb
title: 'IRenderEngine :: SetTimelineObject, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 954fab15e92e6111439abb66d53d53525a5afdb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541298"
---
# <a name="irenderenginesettimelineobject-method"></a>IRenderEngine :: SetTimelineObject, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `SetTimelineObject` méthode définit la chronologie que le moteur de rendu utilise.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetTimelineObject(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTimeline* 
</dt> <dd>

Pointeur vers l’interface [**IAMTimeline**](iamtimeline.md) de l’objet Timeline.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                            | Description                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Opération réussie.<br/>                            |
| <dl> <dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt> </dl> | Le moteur de rendu n’a pas pu s’initialiser.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>          | Mémoire insuffisante.<br/>                |
| <dl> <dt>**\_pointeur E**</dt> </dl>              | Pointeur non valide.<br/>                    |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



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

 

 




