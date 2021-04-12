---
title: Méthode IConfigAsfWriter2 StreamNumFromPin
description: La méthode StreamNumFromPin récupère le numéro de flux associé à la broche d’entrée spécifiée.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- Méthode StreamNumFromPin format Windows Media
- Méthode StreamNumFromPin format Windows Media, interface IConfigAsfWriter2
- Interface IConfigAsfWriter2 Windows Media format, méthode StreamNumFromPin
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c63a31d515e70b0ee0ac5be617ee52fe23bd5416
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382092"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a>IConfigAsfWriter2 :: StreamNumFromPin, méthode

La méthode **StreamNumFromPin** récupère le numéro de flux associé à la broche d’entrée spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPin* \[ dans\]
</dt> <dd>

Pointeur vers l’interface **IPIN** sur la broche d’entrée.

</dd> <dt>

*pwStreamNum* \[ à\]
</dt> <dd>

Pointeur qui reçoit le numéro de flux.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne la valeur \_ OK. En cas d’échec, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Parfois, vous devrez peut-être utiliser directement les interfaces du kit de développement logiciel (SDK) du format Windows Media pour manipuler un flux avant d’exécuter un graphique de filtre. Étant donné que vous ne pouvez pas supposer qu’un numéro de flux ASF est le même que le numéro de code confidentiel DirectShow, cette méthode est fournie.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

 