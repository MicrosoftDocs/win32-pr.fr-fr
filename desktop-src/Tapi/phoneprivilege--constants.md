---
description: Les \_ constantes d’indicateur de bit PHONEPRIVILEGE décrivent les différentes façons d’ouvrir un appareil téléphonique.
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: Constantes PHONEPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d04c074e03d6f0b7f7a6c58e4268e0bd5057a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526706"
---
# <a name="phoneprivilege_-constants"></a>\_Constantes PHONEPRIVILEGE

Les constantes d’indicateur de bit **PHONEPRIVILEGE \_** décrivent les différentes façons d’ouvrir un appareil téléphonique.

<dl> <dt>

<span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**\_moniteur PHONEPRIVILEGE**
</dt> <dd> <dl> <dt>



Une application qui ouvre un appareil téléphonique avec le privilège moniteur est informée des événements et des modifications d’État sur le téléphone. L’application ne peut pas appeler les opérations sur le périphérique téléphonique qui modifieraient son état, de sorte que seules les opérations d’État peuvent être appelées. Plusieurs applications peuvent surveiller un appareil téléphonique à un moment donné.


</dt> </dl> </dd> <dt>

<span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**\_propriétaire PHONEPRIVILEGE**
</dt> <dd> <dl> <dt>



Une application qui ouvre un appareil téléphonique avec le privilège propriétaire est autorisée à modifier l’état des lampes, de la sonnerie, de l’affichage, du hookswitch et des blocs de données du téléphone. L’ouverture d’un appareil téléphonique en mode propriétaire permet également d’analyser l’appareil téléphonique. Une seule application est autorisée à être le propriétaire d’un appareil téléphonique à un moment donné.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




