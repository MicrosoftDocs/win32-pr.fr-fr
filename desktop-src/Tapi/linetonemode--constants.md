---
description: Les \_ constantes LINETONEMODE décrivent les différentes sélections utilisées lors de la génération de tonalités de ligne.
ms.assetid: 7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263
title: Constantes LINETONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e1b5a8d49c927dfa3d5ec87f9a4830a91d79d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528414"
---
# <a name="linetonemode_-constants"></a>\_Constantes LINETONEMODE

Les **\_ constantes LINETONEMODE** décrivent les différentes sélections utilisées lors de la génération de tonalités de ligne.

<dl> <dt>

<span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**\_signal LINETONEMODE**
</dt> <dd> <dl> <dt>



Le ton est un bip, tel que celui utilisé pour annoncer le début d’un enregistrement. La définition exacte est définie par le fournisseur de services.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**\_facturation LINETONEMODE**
</dt> <dd> <dl> <dt>



Le ton est un titre d’information de facturation, tel qu’une tonalité de carte de crédit. La définition exacte est définie par le fournisseur de services.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE \_ occupé**
</dt> <dd> <dl> <dt>



Le ton est occupé. La définition exacte est définie par le fournisseur de services.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE \_ personnalisé**
</dt> <dd> <dl> <dt>



Le ton est un ton personnalisé défini par ses fréquences de composants, de type [**LINEGENERATETONE**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone).


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**\_rappel LINETONEMODE**
</dt> <dd> <dl> <dt>



Le ton est un signal d’inversion. La définition exacte est définie par le fournisseur de services.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil. Les 16 bits de poids faible sont réservés.

Ces constantes sont utilisées pour définir des tonalités à générer sur un appel au tiers distant. Notez que la détection de tons de tonalités non personnalisées n’utilise pas ces constantes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




