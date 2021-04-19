---
description: Les \_ constantes LINECARDOPTION définissent les valeurs utilisées dans le membre dwOptions de la structure LINECARDENTRY retournée dans le cadre de la structure LINETRANSLATECAPS retournée par lineGetTranslateCaps.
ms.assetid: 36c67fbf-e5ca-4ec4-a03a-0b828667abcc
title: Constantes LINECARDOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9948d4a8963e8a9c860f68f0067c601f602c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537706"
---
# <a name="linecardoption_-constants"></a>\_Constantes LINECARDOPTION

Les **\_ constantes LINECARDOPTION** définissent les valeurs utilisées dans le membre **DwOptions** de la structure [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) retournée dans le cadre de la structure [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) retournée par [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps). Les **\_ constantes LINECARDOPTION** t ont les valeurs suivantes :

<dl> <dt>

<span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION \_ masqué**
</dt> <dd> <dl> <dt>



Cette carte d’appel a été masquée par l’utilisateur. Elle n’est pas affichée par Dial Helper dans la liste principale des cartes d’appel disponibles, mais apparaît dans la liste des cartes à partir desquelles les règles de numérotation peuvent être copiées.


</dt> </dl> </dd> <dt>

<span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION \_ prédéfini**
</dt> <dd> <dl> <dt>



Cette carte d’appel est l’une des définitions prédéfinies de carte d’appel, incluse avec la téléphonie par Microsoft. Elle ne peut pas être entièrement supprimée à l’aide de Dial Helper. Si l’utilisateur tente de le supprimer, il est masqué. Elle reste donc accessible pour la copie des règles de numérotation.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Non extensible. Tous les 32 bits sont réservés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




