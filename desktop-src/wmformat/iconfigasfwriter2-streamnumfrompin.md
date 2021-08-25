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
ms.openlocfilehash: 9124d3acaea81e36b212f3dec001374cc035efca449f35af5e43fa18ce50d6dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839820"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a>IConfigAsfWriter2 :: StreamNumFromPin, méthode

La méthode **StreamNumFromPin** récupère le numéro de flux associé à la broche d’entrée spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
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

## <a name="remarks"></a>Remarques

parfois, vous devrez peut-être utiliser directement les interfaces du kit de développement logiciel (SDK) de Format multimédia Windows pour manipuler un flux avant d’exécuter un graphique de filtre. étant donné que vous ne pouvez pas supposer qu’un numéro de flux ASF est le même que le numéro de code confidentiel DirectShow, cette méthode est fournie.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

 