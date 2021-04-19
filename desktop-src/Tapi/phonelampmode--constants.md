---
description: Les constantes d’indicateur de bit PHONELAMPMODE décrivent les différentes façons dont une lampe de téléphone peut être allumée.
ms.assetid: 4f6ed2fa-32c9-44b4-bfb5-2c1446ea84fe
title: Constantes PHONELAMPMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d8df5920df79e6fc59eb12bf1f517b4070e617d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542809"
---
# <a name="phonelampmode_-constants"></a>Constantes PHONELAMPMODE_

Les constantes d’indicateur de bit **PHONELAMPMODE_** décrivent les différentes façons dont la lampe d’un téléphone peut être allumée.

<dl> <dt>

<span id="PHONELAMPMODE_DUMMY"></span><span id="phonelampmode_dummy"></span>**PHONELAMPMODE_DUMMY**
</dt> <dd> <dl> <dt>



Cette valeur est utilisée pour décrire une position de bouton/lampe qui n’a pas de lampe correspondante.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_BROKENFLUTTER"></span><span id="phonelampmode_brokenflutter"></span>**PHONELAMPMODE_BROKENFLUTTER**
</dt> <dd> <dl> <dt>



Brisée brisée est la superposition de Flash et la fonction flottant.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_FLASH"></span><span id="phonelampmode_flash"></span>**PHONELAMPMODE_FLASH**
</dt> <dd> <dl> <dt>



Flash signifie un ralentissement et une désactivation.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_FLUTTER"></span><span id="phonelampmode_flutter"></span>**PHONELAMPMODE_FLUTTER**
</dt> <dd> <dl> <dt>



La fonction flottant signifie qu’elle est activée et désactivée rapidement.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_OFF"></span><span id="phonelampmode_off"></span>**PHONELAMPMODE_OFF**
</dt> <dd> <dl> <dt>



La lampe est désactivée.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_STEADY"></span><span id="phonelampmode_steady"></span>**PHONELAMPMODE_STEADY**
</dt> <dd> <dl> <dt>



Stable signifie que la lampe est allumée en permanence.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_UNKNOWN"></span><span id="phonelampmode_unknown"></span>**PHONELAMPMODE_UNKNOWN**
</dt> <dd> <dl> <dt>



Le mode LAMP est actuellement inconnu.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_WINK"></span><span id="phonelampmode_wink"></span>**PHONELAMPMODE_WINK**
</dt> <dd> <dl> <dt>



Clin d’œil signifie que le taux normal est activé ou désactivé.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil. Les 16 bits de poids faible sont réservés.

Lorsque les cadences on et OFF exactes peuvent varier d’un ensemble de téléphones à l’autre, le mappage des véritables modèles d’éclairage de la lampe pour la plupart des téléphones sur les valeurs indiquées ci-dessus doit être simple.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




