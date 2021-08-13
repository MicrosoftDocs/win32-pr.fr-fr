---
title: Propriété State
description: La propriété State décrit l’état d’un objet à un moment donné. Tous les objets prennent en charge la propriété State.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e174e938dd6252852ded6de957a54f6f94264aa811bd5bb76094af7bbba61f48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564417"
---
# <a name="state-property"></a>Propriété State

La propriété **State** décrit l’état d’un objet à un moment donné. Tous les objets prennent en charge la propriété **State** .

La propriété **State** est récupérée en appelant [**IAccessible :: \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).

Microsoft Active Accessibility fournit des [constantes d’état d’objet](object-state-constants.md), définies dans oleacc. h, qui sont combinées pour identifier l’état d’un objet. Il est recommandé que les développeurs de serveur utilisent ces valeurs d’État prédéfinies. Si des valeurs d’État prédéfinies sont retournées, les clients utilisent [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) pour récupérer une chaîne localisée qui décrit l’État.

Les graphiques qui sont parfois animés doivent avoir la propriété **État** définie sur [**état \_ système \_ animé**](object-state-constants.md) et la propriété [**rôle**](role-property.md) définie sur [**\_ \_ graphique système de rôle**](object-roles.md).

 

 




