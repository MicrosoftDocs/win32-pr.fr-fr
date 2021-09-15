---
description: Permet au filtre de traitement d’image d’écrire des propriétés sur le pilote (et l’appareil).
ms.assetid: b9bb8d81-2945-46ba-a0a2-7009000574aa
title: 'IWiaImageFilter :: ApplyProperties, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.ApplyProperties
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3c20527ee587b975adea34e7c480349836620015
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523140"
---
# <a name="iwiaimagefilterapplyproperties-method"></a>IWiaImageFilter :: ApplyProperties, méthode

Permet au filtre de traitement d’image d’écrire des propriétés sur le pilote (et l’appareil).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ApplyProperties(
  [in] IWiaPropertyStorage *pWiaPropertyStorage
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pWiaPropertyStorage* \[ dans\]
</dt> <dd>

Type : **[ **IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)\***

Spécifie un pointeur vers le [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pour les propriétés à appliquer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

N’appelez pas cette méthode directement à partir de votre application. elle est appelée par Windows acquisition d’images (WIA) 2,0 après que le filtre de traitement d’image a traité les données brutes.

*pWiaPropertyStorage* est l’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) dans laquelle le filtre de traitement d’image doit écrire des propriétés. Un filtre de traitement d’image doit utiliser uniquement la méthode [IPropertyStorage :: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) pour écrire des propriétés.

Cette méthode permet au filtre de traitement d’image d’écrire des propriétés sur le pilote (et l’appareil). Cela peut être nécessaire pour les filtres qui implémentent des fonctionnalités telles que l’exposition automatique lors de l’analyse des films.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
