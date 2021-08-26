---
description: Méthode constructeur CSourceStream. CSourceStream.
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Constructeur CSourceStream. CSourceStream (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e02827c74ef4c5461a5777221e1839846b855a4b2f4cd27d97ce913399787ba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053849"
---
# <a name="csourcestreamcsourcestream-constructor"></a>Constructeur CSourceStream. CSourceStream

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pObjectName* 
</dt> <dd>

Pointeur vers une chaîne contenant le nom de débogage du pin.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode. Initialisez la valeur sur \_ OK avant de créer l’objet. La valeur est modifiée uniquement si une erreur se produit.

</dd> <dt>

*PMS* 
</dt> <dd>

Pointeur vers le filtre [**CSource**](csource.md) qui a créé ce code confidentiel.

</dd> <dt>

*pName* 
</dt> <dd>

Pointeur vers une chaîne qui contient le nom du code PIN.

</dd> </dl>

## <a name="remarks"></a>Remarques

La chaîne spécifiée dans le paramètre *pObjectName* est utilisée uniquement à des fins de débogage. Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).

La chaîne spécifiée dans le paramètre *pname* est le nom retourné par la méthode [**IPIN :: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) . La `CSourceStream` classe n’utilise pas ce nom pour l’identificateur de code confidentiel retourné par la méthode [**CSourceStream :: QueryId**](csourcestream-queryid.md) . Au lieu de cela, **QueryId** calcule un identificateur de code confidentiel en fonction du numéro de code confidentiel. (Les identificateurs pin prennent en charge la persistance Graph. Pour plus d’informations, consultez [**IPIN :: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)

Le constructeur ajoute automatiquement le code confidentiel au filtre propriétaire, en appelant [**CSource :: AddPin**](csource-addpin.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




