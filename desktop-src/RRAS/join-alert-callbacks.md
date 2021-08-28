---
title: Rappels d’alerte de jointure
description: Lorsque le gestionnaire de groupe de multidiffusion est informé qu’il existe de nouveaux récepteurs pour un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le \_ rappel de rappel d’alerte de jointure PMGM \_ \_ .
ms.assetid: b625f8ec-f59b-4151-aa38-48cf8f004966
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0da66e405441804cbca4452cedd7a6599067138bee95a33eaee7a2f10c34c9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074119"
---
# <a name="join-alert-callbacks"></a>Rappels d’alerte de jointure

Lorsque le gestionnaire de groupe de multidiffusion est informé qu’il existe de nouveaux récepteurs pour un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ rappel d' \_ alerte \_ de jointure PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) . Ce rappel indique aux protocoles de routage que les nouveaux hôtes ont rejoint les groupes spécifiés. Par conséquent, les protocoles de routage doivent demander des données de multidiffusion pour les groupes spécifiés par le rappel.

Le gestionnaire de groupe de multidiffusion utilise un ensemble prédéfini de règles utilisées pour déterminer le moment où ce rappel est appelé. Cet ensemble de règles est basé sur le type de demande de jointure envoyé par le client et l’ordre dans lequel les demandes de jointure ont été reçues.

## <a name="wildcard-join-requests"></a>Demandes de jointure de caractères génériques

Lorsqu’une jointure de caractères génériques pour un groupe ( \* , g) est reçue à partir du premier client, le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ rappel d' \_ alerte \_ PMGM Join**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) à tous les autres clients inscrits. Lorsqu’une jointure de caractères génériques est reçue pour un groupe à partir du deuxième client, le gestionnaire de groupe de multidiffusion appelle ce rappel au premier client pour rejoindre le groupe.

## <a name="source-specific-join-requests"></a>Demandes de jointure Source-Specific

Le gestionnaire de groupe de multidiffusion n’appelle pas ce rappel pour les jointures suivantes dans le groupe.

Lorsqu’une jointure spécifique à la source pour un ou plusieurs groupes est reçue, le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ rappel d' \_ alerte \_ PMGM Join**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) uniquement pour le client qui possède l’interface entrante vers la source.

 

 




