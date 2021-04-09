---
title: BackColor, propriété (fonctionnalités de l’environnement Windows hérité)
description: BackColor, propriété
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332fcc6a9081b52300dbee4c69c77602e84a62e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739653"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a>BackColor, propriété (fonctionnalités de l’environnement Windows hérité)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne la couleur d’arrière-plan actuellement affichée dans la fenêtre de la bulle du mot pour le caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). Balloon. BackColor_*

</dd> </dl>

## <a name="remarks"></a>Notes

La plage valide pour une couleur RVB normale est comprise entre 0 et 16 777 215 (&HFFFFFF). L’octet de poids fort d’un nombre de cette plage est égal à 0 ; les 3 octets inférieurs, de l’octet le moins significatif à l’octet le plus significatif, déterminent respectivement la quantité de rouge, de vert et de bleu. Chacun des composants rouge, vert et bleu est représenté par un nombre compris entre 0 et 255 (&HFF).

 

 




