---
title: Role, propriété
description: La propriété Role décrit l’élément d’interface utilisateur d’un objet. Tous les objets prennent en charge la propriété Role.
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2881b301537e9a25dabb260b84bc889cef4e4a6f9f6a5a2c8fab540d78daf8c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133722"
---
# <a name="role-property"></a>Role, propriété

La propriété **role** décrit l’élément d’interface utilisateur d’un objet. Tous les objets prennent en charge la propriété **role** .

Dans de nombreux cas, le rôle de l’objet est évident. Par exemple, Windows ont le rôle de [**\_ \_ fenêtre système rôle**](object-roles.md) et les boutons de commande Push ont le rôle [**\_ \_ PUSHBUTTON système rôle**](object-roles.md) .

La propriété **role** est récupérée en appelant [**IAccessible :: \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).

## <a name="identifying-an-objects-role"></a>Identification du rôle d’un objet

Microsoft Active Accessibility fournit des [constantes de rôle](object-roles.md), définies dans oleacc. h, qui identifient les rôles d’objet communs. Il est recommandé que les développeurs de serveurs utilisent ces valeurs de rôle prédéfinies. Si une constante de rôle prédéfinie est retournée, les clients utilisent la fonction [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) pour récupérer une chaîne localisée qui décrit le rôle.

Pour les contrôles d’animation, tels que le contrôle d’animation affiché lors de la copie de fichiers, utilisez l' [**\_ \_ animation de système de rôle**](object-roles.md). Les graphiques qui sont parfois animés sont décrits comme un [**\_ \_ graphique de système de rôle**](object-roles.md) avec la propriété [**État**](state-property.md) définie sur [**état \_ système \_ animé**](object-state-constants.md).

Notez que certains rôles ne sont pas faciles à décrire. Par exemple, la vue de grande icône d’un dossier permet une disposition arbitraire des icônes, donc son rôle peut être décrit comme [**\_ \_ regroupement de système de rôle**](object-roles.md). Ou un contrôle qui fournit des éléments dans des lignes et des colonnes fixes peut avoir le rôle de [**\_ \_ table système Role**](object-roles.md) . Étant donné qu’un rôle est utilisé pour communiquer le modèle d’utilisation à un utilisateur final, il est important d’utiliser le rôle approprié. Par exemple, si votre contrôle agit comme un bouton, utilisez le [**\_ \_ PUSHBUTTON système de rôle**](object-roles.md).

 

 




