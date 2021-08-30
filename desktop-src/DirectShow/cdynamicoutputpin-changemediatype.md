---
description: La méthode ChangeMediaType modifie dynamiquement le type de média pour la connexion.
ms.assetid: 38efdfdc-f636-4cad-b8d3-8c63a277644e
title: Méthode CDynamicOutputPin. ChangeMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 892709431e1f521ce4c70f6783d0fb9156b544e4d2c4e95282a1879a9bb70885
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983299"
---
# <a name="cdynamicoutputpinchangemediatype-method"></a>Méthode CDynamicOutputPin. ChangeMediaType

La `ChangeMediaType` méthode modifie dynamiquement le type de média pour la connexion. La modification peut se produire pendant l’exécution du graphique de filtre. Une fois cette méthode appelée, les exemples avec l’ancien type de média ne peuvent pas être remis. L’appelant doit s’assurer qu’aucun ancien échantillon n’est en attente.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ChangeMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*crédit* 
</dt> <dd>

Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui spécifie le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                           | Description                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>                                                                                                                      |
| <dl> <dt>**E \_ échec**</dt> </dl>                | Échec. Le filtre propriétaire n’a peut-être pas appelé [**CDynamicOutputPin :: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).<br/> |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | Le pin n’est pas connecté.<br/>                                                                                                     |



 

## <a name="remarks"></a>Remarques

Appelez la méthode [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) avant d’appeler cette méthode.

Cette méthode vérifie d’abord si la broche d’entrée en aval peut accepter le nouveau format sans se reconnecter. Il interroge la broche d’entrée de l’interface [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) . Si la broche d’entrée prend en charge **IPinConnection**, la méthode appelle la méthode [**IPinConnection ::D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) avec le type de média proposé. Si la broche d’entrée accepte le nouveau type de média, la méthode appelle la méthode [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) et renégocie les spécifications de l’allocateur.

En revanche, si le code pin en aval ne prend pas en charge **IPinConnection**, ou s’il rejette le nouveau type de média, la méthode appelle la méthode [**CDynamicOutputPin ::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) pour effectuer une reconnexion dynamique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




