---
description: Répertorie et décrit les types d’accès de l’objet de stratégie.
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: Droits d’accès à l’objet de stratégie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5c762955a4c53015241086b2249c5edbc4f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529113"
---
# <a name="policy-object-access-rights"></a>Droits d’accès à l’objet de stratégie

L’objet de [**stratégie**](policy-object.md) a les types d’accès spécifiques aux objets suivants :



| Type d’accès                         | Description                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ informations locales sur l’affichage \_ de la stratégie    | Ce type d’accès est nécessaire pour lire les informations de stratégie de sécurité diverses du système cible. Cela comprend le quota par défaut, l’audit, l’état du serveur et les informations de rôle, ainsi que les informations d’approbation. Ce type d’accès est également nécessaire pour énumérer les domaines approuvés, les comptes et les [*privilèges*](/windows/desktop/SecGloss/p-gly). |
| \_ \_ informations confidentielles \_ sur la stratégie   | Ce type d’accès est nécessaire pour afficher des informations sensibles, telles que les noms de comptes établis pour les relations de domaine approuvées.                                                                                                                                                                                                                              |
| \_administrateur d’approbation de stratégie \_                | Ce type d’accès est nécessaire pour modifier le domaine du compte ou les informations du domaine principal.                                                                                                                                                                                                                                                                             |
| \_limites de \_ quota par défaut définies par la stratégie \_ \_ | Définissez les quotas système par défaut qui sont appliqués aux comptes d’utilisateur.                                                                                                                                                                                                                                                                                                   |
| \_clé de création de la stratégie \_              | Ce type d’accès est nécessaire pour créer un objet de données privées.                                                                                                                                                                                                                                                                                                    |
| \_créer un \_ compte de stratégie             | Ce type d’accès est nécessaire pour créer un nouvel objet de [**compte**](account-object.md) .                                                                                                                                                                                                                                                                               |
| \_ \_ exigences d’audit définies pour la stratégie \_    | Ce type d’accès est nécessaire pour mettre à jour les exigences d’audit du système.                                                                                                                                                                                                                                                                                      |
| \_administrateur du \_ Journal d’audit de stratégie \_           | Ce type d’accès est nécessaire pour modifier les caractéristiques de la piste d’audit, telles que sa taille maximale ou la période de rétention pour les enregistrements d’audit, ou pour effacer le journal.                                                                                                                                                                                               |
| \_ \_ informations d’audit d’affichage de stratégie \_    | Ce type d’accès est nécessaire pour afficher les informations sur la piste d’audit ou les exigences d’audit.                                                                                                                                                                                                                                                                                  |
| \_administrateur du serveur de stratégie \_               | Ce type d’accès est nécessaire pour modifier les informations sur l’état du serveur ou le rôle (maître/réplica). Il est également nécessaire de modifier la source du réplica et les informations du nom du compte.                                                                                                                                                                                           |
| \_noms de recherche de stratégie \_               | Ce type d’accès est nécessaire pour effectuer la conversion entre les noms et les SID.                                                                                                                                                                                                                                                                                                    |
| \_privilège de création de stratégie \_           | Pas encore pris en charge.                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a>Masques d’accès génériques

L’objet de [**stratégie**](policy-object.md) publie les mappages suivants à partir de types d’accès génériques vers des types d’accès spécifiques :

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                                        POLICY_SERVER_ADMIN

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_LOOKUP_NAMES
```

## <a name="standard-access-types"></a>Types d’accès standard

Cet objet ne prend pas en charge le type d’accès standard SYNCHRONIZE (facultatif). Tous les types d’accès requis sont pris en charge. Le masque de tous les types d’accès pris en charge pour ce type d’objet est :

``` syntax
    POLICY_ALL_ACCESS STANDARD_RIGHTS_REQUIRED |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                    POLICY_SERVER_ADMIN
                    POLICY_LOOKUP_NAMES
```

 

 
