---
description: Supprime les segments de média définis par la plage de temps spécifiée du IMFSourceBuffer.
ms.assetid: 86536d73-18c0-4acc-81ec-72f1dfe400c5
title: 'IMFSourceBuffer :: Remove, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Remove
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: af9aed011a1a4b53733d70646fc14b21e7c97f9d193a60e679f5f5f532679e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941909"
---
# <a name="imfsourcebufferremove-method"></a>IMFSourceBuffer :: Remove, méthode

Supprime les segments de média définis par la plage de temps spécifiée du [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Remove(
  [in] double start,
  [in] double end
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Démarrer* \[ dans\]
</dt> <dd>

Début de l’intervalle de temps.

</dd> <dt>

*fin* \[ dans\]
</dt> <dd>

Fin de l’intervalle de temps.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




