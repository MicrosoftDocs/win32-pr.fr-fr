---
description: 'En savoir plus sur : IMFMediaKeys :: Shutdown, méthode'
ms.assetid: 464b598c-5fa7-40af-83ba-8619fbd84b04
title: 'IMFMediaKeys :: Shutdown, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.Shutdown
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 198eea5af6980828f6a85c9f4680812dbf4dbf0e3dbac2c5181c6347ffbf386e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114339"
---
# <a name="imfmediakeysshutdown-method"></a>IMFMediaKeys :: Shutdown, méthode

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Shutdown();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

L' **arrêt** doit être appelé par l’application avant la version finale. La référence CDM (Content decryption module) et toutes les autres ressources sont publiées à ce stade. Toutefois, les sessions associées ne sont pas libérées ou fermées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFMediaKeys**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




