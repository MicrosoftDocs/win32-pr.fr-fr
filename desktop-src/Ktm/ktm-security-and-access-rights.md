---
description: Le modèle de sécurité Windows permet aux appelants du gestionnaire de transactions KTM (Kernel Transaction Manager) de contrôler l’accès aux objets transaction, gestionnaire de transactions, gestionnaire de ressources et inscription.
ms.assetid: c9d51d4d-9f07-44d6-a2e1-4a47367cc4ae
title: Sécurité KTM et droits d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed4e42c9aaf8498ff16ebd1d32f539fef5b54b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519510"
---
# <a name="ktm-security-and-access-rights"></a>Sécurité KTM et droits d’accès

Le modèle de sécurité Windows permet aux appelants du gestionnaire de transactions KTM (Kernel Transaction Manager) de contrôler l’accès aux objets transaction, gestionnaire de transactions, gestionnaire de ressources et inscription. Pour plus d’informations, consultez [modèle de contrôle d’accès](/windows/desktop/SecAuthZ/access-control-model). Pour les applications qui ne sont pas concernées par la sécurité, les transactions peuvent être créées avec des listes de contrôle d’accès (ACL) permissive qui permettent à n’importe quel gestionnaire de ressources de s’inscrire sur une transaction.

## <a name="transactions"></a>Transactions

Lorsqu’un client utilise la fonction [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction) , le système vérifie les droits d’accès demandés par rapport au descripteur de sécurité de l’objet de transaction.

Les droits d’accès valides pour les objets de transaction incluent la possibilité d’interroger et de définir des informations, de les inscrire et diverses opérations de transaction, ainsi que des [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights). Les [**masques d’accès aux transactions**](transaction-access-masks.md) répertorient les droits d’accès spécifiques d’une transaction.

Étant donné que les transactions ont un État durable, il est essentiel que les services RMs et TMs qui interagissent avec le KTM remplissent leurs obligations en ce qui concerne la récupération. Si vous ne respectez pas ces obligations, vous risquez de provoquer des fuites de ressources qui ne sont pas nettoyées, même en cas de redémarrage du système. Tenez compte de l’effet d’une fuite persistante ou d’un code malveillant qui a provoqué la consommation des ressources de noyau par le KTM, jusqu’à ce qu’il aboutisse à une défaillance du système. après le redémarrage qui en résulte, le KTM lit son journal et recrée tous les objets persistants, provoquant potentiellement la répétition de la même défaillance du système. La limitation basée sur les quotas empêchera l’insuffisance de ressources persistantes à partir d’un gestionnaire de ressources non autorisé ou incorrect. Enfin, des mécanismes d’administration doivent être créés pour permettre la détection et la correction de ces fuites persistantes.

## <a name="transaction-managers"></a>Gestionnaires de transactions

Lorsqu’un client utilise la fonction [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager) , le système vérifie les droits d’accès demandés par rapport au descripteur de sécurité de l’objet Resource Manager.

Les droits d’accès valides pour les objets du gestionnaire de transactions incluent la capacité à interroger et à définir des informations, à créer des services RMs, à récupérer et à renommer des opérations, ainsi qu’à des [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights). Les [**masques d’accès du gestionnaire de transactions**](transaction-manager-access-masks.md) répertorient les droits d’accès spécifiques pour un gestionnaire de transactions.

Un gestionnaire de ressources peut créer ses propres objets gestionnaire de transactions avec des listes de contrôle d’accès restrictives pour limiter les gestionnaires de ressources qui peuvent participer aux transactions qui utilisent le journal de ce gestionnaire de transactions.

## <a name="resource-managers"></a>Gestionnaires de ressources

Lorsqu’un client utilise la fonction [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) , le système vérifie les droits d’accès demandés par rapport au descripteur de sécurité de l’objet Resource Manager.

Les droits d’accès valides pour les objets Resource Manager incluent la possibilité d’interroger et de définir des informations, de récupérer, d’inscrire, d’enregistrer et de propager et de récupérer des opérations, ainsi que des [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights). [**Gestionnaire des ressources masques d’accès**](resource-manager-access-masks.md) répertorie les droits d’accès spécifiques d’un gestionnaire de ressources.

Un gestionnaire de ressources peut créer ses propres objets Resource Manager avec des ACL restrictives s’il souhaite empêcher du code malveillant d’intercepter des notifications ou de forcer des résultats transactionnels particuliers.

## <a name="enlistments"></a>Inscriptions

Lorsqu’un client utilise la fonction [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) , le système vérifie les droits d’accès demandés par rapport au descripteur de sécurité de l’objet d’inscription.

Les droits d’accès valides pour les objets d’inscription incluent la possibilité d’interroger et de définir des informations, de récupérer des opérations, ainsi que des [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights). Les [**masques d’accès d’inscription**](enlistment-access-masks.md) répertorient les droits d’accès spécifiques d’une inscription.

 

 
