---
title: BorderColor, propriété
description: BorderColor, propriété
ms.assetid: 7592db02-c157-45f4-bbcf-e6d5bd99e8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6812910c76ad46e7c065314d0b3e5f03d8a6ad6dcb7b918ef33b1a0315a0ad0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963329"
---
# <a name="bordercolor-property"></a>BorderColor, propriété

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne la couleur de bordure actuellement affichée pour la fenêtre de la bulle du mot pour le caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»)._ * Balloon. BorderColor

</dd> </dl>

## <a name="remarks"></a>Remarques

La plage valide pour une couleur RVB normale est comprise entre 0 et 16 777 215 (&HFFFFFF). L’octet de poids fort d’un nombre de cette plage est égal à 0 ; les 3 octets inférieurs, de l’octet le moins significatif à l’octet le plus significatif, déterminent respectivement la quantité de rouge, de vert et de bleu. Chacun des composants rouge, vert et bleu est représenté par un nombre compris entre 0 et 255 (&HFF).

 

 




