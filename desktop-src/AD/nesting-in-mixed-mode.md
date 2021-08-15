---
title: Imbrication en mode mixte
description: Cette rubrique répertorie les restrictions des groupes de sécurité dans un domaine en mode mixte.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Imbrication en mode mixte AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c53fd79cb10c452dbb363c3d6803071e6e52871f0ce87b03f9d06a61eaece8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185821"
---
# <a name="nesting-in-mixed-mode"></a>Imbrication en mode mixte

Cette rubrique répertorie les restrictions des groupes de sécurité dans un domaine en mode mixte.

Les groupes de sécurité dans un domaine en mode mixte présentent les restrictions suivantes :

-   les groupes universels ne peuvent pas être créés dans des domaines en mode mixte, car l’étendue universelle est prise en charge uniquement dans les domaines en mode natif Windows 2000.
-   Un groupe global peut contenir des comptes appartenant au même domaine que le groupe. Un groupe global ne peut pas contenir de groupes universels, de groupes globaux ou de comptes d’un autre domaine.
-   Un groupe de domaine local peut contenir des groupes globaux et des comptes à partir de n’importe quel domaine ou forêt. Un groupe de domaine local ne peut pas contenir un autre groupe de domaine local.

Sachez que les groupes de distribution peuvent être imbriqués en fonction des règles d’imbrication pour le mode natif.

 

 




