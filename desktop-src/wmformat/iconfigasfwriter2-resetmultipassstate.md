---
title: Méthode IConfigAsfWriter2 ResetMultiPassState
description: La méthode ResetMultiPassState réinitialise le filtre quand un test d’encodage de prétraitement est annulé avant d’être terminé.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- Méthode ResetMultiPassState format Windows Media
- Méthode ResetMultiPassState format Windows Media, interface IConfigAsfWriter2
- Interface IConfigAsfWriter2 Windows Media format, méthode ResetMultiPassState
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f10563ed716b6b33258fe57ff8129bff78b401170db1512566015d0b05d54dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839869"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a>IConfigAsfWriter2 :: ResetMultiPassState, méthode

La méthode **ResetMultiPassState** réinitialise le filtre quand un test d’encodage de prétraitement est annulé avant d’être terminé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                         | Description                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | S_OK<br/>                  |
| <dl> <dt>**VFW \_ E \_ non \_ arrêté**</dt> </dl> | Le filtre n’était pas dans un état arrêté.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode doit être appelée pour réinitialiser l’état interne du filtre chaque fois qu’un test d’encodage de prétraitement est annulé avant que le filtre ait reçu un événement de **\_ \_ fin de prétraitement EC** . Il n’est pas nécessaire d’appeler cette méthode si la réussite de l’encodage de prétraitement s’est terminée sans erreurs.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

