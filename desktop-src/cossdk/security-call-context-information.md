---
description: Informations de contexte de l’appel de sécurité
ms.assetid: 8b170c17-f095-4c25-9ee2-480681b7e5f6
title: Informations de contexte de l’appel de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0aed07f79fdba16f0ea6139a58cc50871d795e1eacbf94737b04dbf5f1fe900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546866"
---
# <a name="security-call-context-information"></a>Informations de contexte de l’appel de sécurité

La sécurité basée sur les rôles repose sur un mécanisme général qui vous permet de récupérer des informations de sécurité concernant tous les appelants en amont dans la chaîne d’appels à votre composant. Ces informations sont disponibles uniquement si vous avez activé la vérification des rôles au niveau du composant. Pour plus d’informations sur la façon de définir la sécurité au niveau du composant, consultez [définition d’un niveau de sécurité pour les vérifications d’accès](setting-a-security-level-for-access-checks.md).

Vous pouvez utiliser l’interface [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) pour accéder aux informations de contexte de l’appel de sécurité par programme. Pour obtenir une description, consultez [sécurité des composants de programmation](programmatic-component-security.md).

Le contexte de l’appel de sécurité est passé chaque fois qu’une limite de sécurité est franchie. Pour les appels entre les composants d’une application, qui résident dans la même limite de sécurité, aucune information de contexte d’appel n’est transmise. Pour les appels entre des processus ou entre des applications au sein d’un processus, appelez le flux d’informations de contexte.

Cette fonctionnalité est particulièrement utile si vous souhaitez effectuer un audit et une journalisation détaillés. Vous pouvez récupérer et enregistrer des informations de sécurité pour chaque appelant en amont.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception efficace des rôles](designing-roles-effectively.md)
</dt> <dt>

[Limites de sécurité](security-boundaries.md)
</dt> <dt>

[Propriété de contexte de sécurité](security-context-property.md)
</dt> <dt>

[Utilisation de rôles pour l’autorisation du client](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



