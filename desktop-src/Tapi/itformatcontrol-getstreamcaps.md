---
description: La méthode GetStreamCaps récupère les fonctionnalités associées à un index de format donné.
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: 'ITFormatControl :: GetStreamCaps, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f54cbd44a946c0fcd3cf297c4cacadc49369765b8c1b6505031a145768c3b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406109"
---
# <a name="itformatcontrolgetstreamcaps-method"></a>ITFormatControl :: GetStreamCaps, méthode

\[cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **GetStreamCaps** récupère les fonctionnalités associées à un index de format donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStreamCaps(
  [in]  DWORD                   dwIndex,
  [out] AM_MEDIA_TYPE           **ppMediaType,
  [out] TAPI_STREAM_CONFIG_CAPS *pStreamConfigCaps,
  [out] BOOL                    *pfEnabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwIndex* \[ dans\]
</dt> <dd>

Index du format détecté.

</dd> <dt>

*ppMediaType* \[ à\]
</dt> <dd>

Pointeur vers un descripteur de **\_ \_ type de média am** du format terminal. Pour plus d’informations sur le **\_ \_ type de média am**, consultez la documentation de DirectX.

</dd> <dt>

*pStreamConfigCaps* \[ à\]
</dt> <dd>

Structure [**d' \_ \_ \_ embouts de configuration de flux TAPI**](tapi-stream-config-caps.md) qui fournit des informations détaillées sur les fonctionnalités de flux.

</dd> <dt>

*pfEnabled* \[ à\]
</dt> <dd>

Indique si le format associé à l’index actuel est activé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|--------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                         |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> <dt>

[**\_majuscules de la configuration de flux TAPI \_ \_**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




