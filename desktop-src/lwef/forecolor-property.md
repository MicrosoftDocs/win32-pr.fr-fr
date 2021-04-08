---
title: ForeColor, propriété
description: ForeColor, propriété
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef05c9f51e040326c75f142e4649a8dbd0cfdbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839517"
---
# <a name="forecolor-property"></a>ForeColor, propriété

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne la couleur de premier plan actuellement affichée dans la fenêtre de la bulle du mot pour le caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («*** CharacterID * * * »). Balloon. ForeColor**

</dd> </dl>

## <a name="remarks"></a>Notes

La propriété **ForeColor** retourne une valeur qui spécifie la couleur du texte dans la bulle de mot. La plage valide pour une couleur RVB normale est comprise entre 0 et 16 777 215 (&HFFFFFF). L’octet de poids fort d’un nombre de cette plage est égal à 0 ; les 3 octets inférieurs, de l’octet le moins significatif à l’octet le plus significatif, déterminent respectivement la quantité de rouge, de vert et de bleu. Chacun des composants rouge, vert et bleu est représenté par un nombre compris entre 0 et 255 (&HFF).

 

 




