---
description: Les \_ constantes LINELOCATIONOPTION définissent les valeurs utilisées dans le membre dwOptions de la structure LINELOCATIONENTRY retournée dans le cadre de la structure LINETRANSLATECAPS retournée par lineGetTranslateCaps.
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: Constantes LINELOCATIONOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f60398953d2f809e29a78323e3b1dedfcac7a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545945"
---
# <a name="linelocationoption_-constants"></a>\_Constantes LINELOCATIONOPTION

Les constantes **LINELOCATIONOPTION \_** définissent les valeurs utilisées dans le membre **DwOptions** de la structure [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) retournée dans le cadre de la structure [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) retournée par [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).

<dl> <dt>

<span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION \_ PULSEDIAL**
</dt> <dd> <dl> <dt>



Le mode de numérotation par défaut à cet emplacement est la numérotation par impulsions. Si ce bit est défini, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) insère un modificateur de numérotation « P » au début de la chaîne de numérotation renvoyée lorsque cet emplacement est sélectionné. Si ce bit n’est pas défini, **lineTranslateAddress** insère un modificateur de numérotation « T » au début de la chaîne de numérotation.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Non extensible. Tous les 32 bits sont réservés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




