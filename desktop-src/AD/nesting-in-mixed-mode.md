---
title: Imbrication en mode mixte
description: Cette rubrique répertorie les restrictions des groupes de sécurité dans un domaine en mode mixte.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Imbrication en mode mixte AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d63d475edf77398a69a519a08f3803f69d67d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839285"
---
# <a name="nesting-in-mixed-mode"></a>Imbrication en mode mixte

Cette rubrique répertorie les restrictions des groupes de sécurité dans un domaine en mode mixte.

Les groupes de sécurité dans un domaine en mode mixte présentent les restrictions suivantes :

-   Les groupes universels ne peuvent pas être créés dans des domaines en mode mixte, car l’étendue universelle est prise en charge uniquement dans les domaines en mode natif Windows 2000.
-   Un groupe global peut contenir des comptes appartenant au même domaine que le groupe. Un groupe global ne peut pas contenir de groupes universels, de groupes globaux ou de comptes d’un autre domaine.
-   Un groupe de domaine local peut contenir des groupes globaux et des comptes à partir de n’importe quel domaine ou forêt. Un groupe de domaine local ne peut pas contenir un autre groupe de domaine local.

Sachez que les groupes de distribution peuvent être imbriqués en fonction des règles d’imbrication pour le mode natif.

 

 




