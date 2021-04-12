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
ms.openlocfilehash: ed61e4f0517822a602f2bb88c944bba82fa1f943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382444"
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

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                         | Description                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | S_OK<br/>                  |
| <dl> <dt>**VFW \_ E \_ non \_ arrêté**</dt> </dl> | Le filtre n’était pas dans un état arrêté.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode doit être appelée pour réinitialiser l’état interne du filtre chaque fois qu’un test d’encodage de prétraitement est annulé avant que le filtre ait reçu un événement de **\_ \_ fin de prétraitement EC** . Il n’est pas nécessaire d’appeler cette méthode si la réussite de l’encodage de prétraitement s’est terminée sans erreurs.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

