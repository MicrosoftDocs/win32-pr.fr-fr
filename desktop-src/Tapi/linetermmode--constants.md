---
description: Les \_ constantes d’indicateur de bit LINETERMMODE décrivent les différents types d’événements sur une ligne téléphonique qui peuvent être routés vers un appareil terminal.
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: Constantes LINETERMMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e689e2e4e432d6cf804e64babd462e749e7e9e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528077"
---
# <a name="linetermmode_-constants"></a>\_Constantes LINETERMMODE

Les constantes d’indicateur de bit **LINETERMMODE \_** décrivent les différents types d’événements sur une ligne téléphonique qui peuvent être routés vers un appareil terminal.

<dl> <dt>

<span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**\_boutons LINETERMMODE**
</dt> <dd> <dl> <dt>



Il s’agit d’événements bouton-pression envoyés du terminal à la ligne.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**\_affichage LINETERMMODE**
</dt> <dd> <dl> <dt>



Il s’agit des informations d’affichage envoyées à partir de la ligne vers le terminal.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE \_ HOOKSWITCH**
</dt> <dd> <dl> <dt>



Il s’agit des événements hookswitch envoyés du terminal à la ligne.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**\_lampes LINETERMMODE**
</dt> <dd> <dl> <dt>



Il s’agit d’événements de lampe envoyés de la ligne vers le terminal.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE \_ MEDIABIDIRECT**
</dt> <dd> <dl> <dt>



Il s’agit du flux de média bidirectionnel associé à un appel sur la ligne et le terminal. Utilisez cette valeur lorsque le routage des deux canaux unidirectionnels du flux de média d’un appel ne peut pas être contrôlé indépendamment.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE \_ MEDIAFROMLINE**
</dt> <dd> <dl> <dt>



Il s’agit du flux de média unidirectionnel de la ligne vers le terminal associé à un appel sur la ligne. Utilisez cette valeur lorsque le routage des deux canaux unidirectionnels du flux de média d’un appel peut être contrôlé indépendamment.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE \_ MEDIATOLINE**
</dt> <dd> <dl> <dt>



Il s’agit du flux de média unidirectionnel entre le terminal et la ligne associée à un appel sur la ligne. Utilisez cette valeur lorsque le routage des deux canaux unidirectionnels du flux de média d’un appel peut être contrôlé indépendamment.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**\_sonnerie LINETERMMODE**
</dt> <dd> <dl> <dt>



Il s’agit des informations de contrôle de sonnerie envoyées du commutateur au terminal.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

Ces constantes décrivent les classes de flux de contrôle et d’informations qui peuvent être acheminées directement entre un appareil de ligne et un périphérique terminal (tel qu’un ensemble de téléphones).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




