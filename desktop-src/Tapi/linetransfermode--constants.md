---
description: Les \_ constantes d’indicateur de bit LINETRANSFERMODE décrivent les différentes façons de résoudre les demandes de transfert d’appel.
ms.assetid: 0a01131f-b63c-45ef-a0a9-17d69a0dacf9
title: Constantes LINETRANSFERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff01f68ab4c43cf15a532639ade9d357a269ba6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324690"
---
# <a name="linetransfermode_-constants"></a>\_Constantes LINETRANSFERMODE

Les constantes d’indicateur de bit **LINETRANSFERMODE \_** décrivent les différentes façons de résoudre les demandes de transfert d’appel.

<dl> <dt>

<span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**\_Conférence LINETRANSFERMODE**
</dt> <dd> <dl> <dt>



Le transfert est résolu en établissant une conférence triple entre l’application, le tiers connecté à l’appel initial et le tiers connecté à l’appel de consultation. Un appel de conférence est créé lorsque cette option est sélectionnée.


</dt> </dl> </dd> <dt>

<span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**\_transfert LINETRANSFERMODE**
</dt> <dd> <dl> <dt>



Le transfert est résolu en transférant l’appel initial à l’appel de consultation. Les deux appels deviennent inactifs pour l’application.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




