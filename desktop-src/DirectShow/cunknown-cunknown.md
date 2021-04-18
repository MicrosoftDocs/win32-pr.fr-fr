---
description: Méthode de constructeur.
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Constructeur CUnknown. CUnknown (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b500e7f12a2242b6c05367bc061f50680d2d608b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532800"
---
# <a name="cunknowncunknown-constructor"></a>Constructeur CUnknown. CUnknown

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pName* 
</dt> <dd>

Chaîne contenant le nom de l’objet. utilisé dans le constructeur [**CBaseObject**](cbaseobject.md) pour le débogage.

</dd> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers le propriétaire de cet objet. Si l’objet est agrégé, passer un pointeur vers l’interface IUnknown de l’objet d’agrégation. Sinon, affectez la valeur **null** à ce paramètre.

</dd> </dl>

## <a name="remarks"></a>Notes

L’objet est initialisé avec un nombre de références égal à zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




