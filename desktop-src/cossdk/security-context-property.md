---
description: Propriété de contexte de sécurité
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: Propriété de contexte de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c537dc8c9b925fff5f7fc4f3da99fd361bfb02f61008b7d7af8a421b9f1d11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546820"
---
# <a name="security-context-property"></a>Propriété de contexte de sécurité

Comme pour chaque service automatique fourni par COM+, la vérification automatique des rôles est basée sur les propriétés incluses dans le contexte de l’objet. La détermination du fait qu’une vérification de la sécurité doit être effectuée sur un appel dans un composant est basée sur la propriété de sécurité du contexte de l’objet créé lorsque le composant configuré est instancié.

En général, vous n’avez pas besoin de vous préoccuper de cette propriété. elle est utilisée directement par COM+, et pas par vous. Toutefois, dans certains cas, vous pouvez avoir besoin d’un contrôle strict sur l’activation d’un objet. Dans ce cas, la propriété de sécurité peut affecter le contexte dans lequel votre objet est activé. Autrement dit, si un objet a une configuration incompatible avec le contexte de son créateur, il est activé dans son propre contexte. La propriété de sécurité peut influencer cela, comme peut n’importe quelle propriété du contexte de l’objet.

Si vous ne souhaitez pas que les paramètres de sécurité influencent l’activation, vous pouvez choisir uniquement la vérification de l’accès au niveau du processus. Cela supprime la propriété de sécurité sur le contexte de l’objet, même si elle désactive efficacement la vérification basée sur les rôles et rend les [informations de contexte d’appel de sécurité](security-call-context-information.md) indisponibles.

Pour plus d’informations sur les contrôles d’accès au niveau du processus, consultez [limites de sécurité](security-boundaries.md). Pour savoir comment définir la sécurité au niveau du processus, consultez [définition d’un niveau de sécurité pour les vérifications d’accès](setting-a-security-level-for-access-checks.md).

Pour plus d’informations sur le contexte d’objet, consultez [contextes](com--contexts.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception efficace des rôles](designing-roles-effectively.md)
</dt> <dt>

[Limites de sécurité](security-boundaries.md)
</dt> <dt>

[Informations de contexte de l’appel de sécurité](security-call-context-information.md)
</dt> <dt>

[Utilisation de rôles pour l’autorisation du client](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



