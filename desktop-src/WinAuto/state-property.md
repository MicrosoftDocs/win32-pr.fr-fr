---
title: Propriété State
description: La propriété State décrit l’état d’un objet à un moment donné. Tous les objets prennent en charge la propriété State.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151f09fca6c31abaaa98a19139d3e22eb28ec90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840745"
---
# <a name="state-property"></a>Propriété State

La propriété **State** décrit l’état d’un objet à un moment donné. Tous les objets prennent en charge la propriété **State** .

La propriété **State** est récupérée en appelant [**IAccessible :: \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).

Microsoft Active Accessibility fournit des [constantes d’état d’objet](object-state-constants.md), définies dans oleacc. h, qui sont combinées pour identifier l’état d’un objet. Il est recommandé que les développeurs de serveur utilisent ces valeurs d’État prédéfinies. Si des valeurs d’État prédéfinies sont retournées, les clients utilisent [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) pour récupérer une chaîne localisée qui décrit l’État.

Les graphiques qui sont parfois animés doivent avoir la propriété **État** définie sur [**état \_ système \_ animé**](object-state-constants.md) et la propriété [**rôle**](role-property.md) définie sur [**\_ \_ graphique système de rôle**](object-roles.md).

 

 




