---
title: Modification de l’étendue ou du type d’un groupe
description: Cette rubrique montre comment modifier l’étendue ou le type d’un groupe dans des domaines en mode natif.
ms.assetid: bdae7bc9-072a-4063-9562-8e0fcb1b7937
ms.tgt_platform: multiple
keywords:
- regroupe Active Directory, en modifiant l’étendue ou le type d’un groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65c64b4a2dafe4bf6c0e65463ef16e0270c0be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671005"
---
# <a name="changing-a-groups-scope-or-type"></a>Modification de l’étendue ou du type d’un groupe

La modification d’une étendue de groupe ou d’un type n’est pas autorisée dans les domaines en mode mixte. Toutefois, les conversions suivantes sont autorisées dans les domaines en mode natif :

Groupe global vers groupe universel : cela est autorisé uniquement si le groupe global n’est pas membre d’un autre groupe global.

Groupe de domaine local vers groupe universel : le groupe de domaine local en cours de conversion ne peut pas contenir un autre groupe de domaine local.

Groupe universel à groupe global ou groupe de domaine local : pour la conversion en groupe global, le groupe universel en cours de conversion ne peut pas contenir des utilisateurs ou des groupes globaux d’un autre domaine. Pour la conversion en groupe de domaine local, le groupe universel en cours de conversion ne peut pas être membre d’un groupe universel ou d’un groupe de domaine local d’un autre domaine.

En mode natif, un type de groupe peut être converti librement entre des groupes de sécurité et des groupes de distribution.

Sachez que si un groupe est utilisé pour définir le contrôle d’accès, la modification de l’étendue ou du type peut affecter les entrées de contrôle d’accès (ACE) qui contiennent ce groupe. Le système de sécurité ignorera les ACE qui contiennent des groupes qui ne sont pas des groupes de sécurité.

 

 




