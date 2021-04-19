---
description: Les \_ constantes d’indicateur de bit LINETERMSHARING décrivent les différentes façons dont un terminal peut être partagé entre des appareils de ligne, des adresses ou des appels.
ms.assetid: 50a52a50-4d94-4068-9ea4-bea862400036
title: Constantes LINETERMSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2587621b6362195a610339ba5620b32f1d4f761
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537454"
---
# <a name="linetermsharing_-constants"></a>\_Constantes LINETERMSHARING

Les constantes d’indicateur de bit **LINETERMSHARING \_** décrivent les différentes façons dont un terminal peut être partagé entre des appareils de ligne, des adresses ou des appels.

<dl> <dt>

<span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING \_ privé**
</dt> <dd> <dl> <dt>



L’appareil terminal est privé sur un appareil à ligne unique.


</dt> </dl> </dd> <dt>

<span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING \_ SHAREDCONF**
</dt> <dd> <dl> <dt>



Le périphérique terminal peut être utilisé par plusieurs lignes. Les requêtes [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) des différents terminaux finissent par être fusionnées ou interrogées sur le terminal.


</dt> </dl> </dd> <dt>

<span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING \_ SHAREDEXCL**
</dt> <dd> <dl> <dt>



Le périphérique terminal peut être utilisé par plusieurs lignes. Le dernier périphérique de ligne à faire un [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) ou un [**\_ lineSetTerminal TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) sur le terminal pour un mode terminal donné disposera d’une connexion exclusive au terminal pour ce mode.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

Ces constantes décrivent les classes de flux de contrôle et d’informations qui peuvent être acheminées directement entre un appareil de ligne et un périphérique terminal (tel qu’un ensemble de téléphones).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

