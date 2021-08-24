---
description: Un gestionnaire de ressources s’inscrit dans une transaction lorsqu’il commence la participation à cette transaction particulière.
ms.assetid: 9c201699-c00b-4efe-9f30-8d4e182de785
title: Inscriptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c19fea9c19da9bb16f81bd417e22c943876997ac224e3823020e5660218dfa5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146582"
---
# <a name="enlistments"></a>Inscriptions

Un gestionnaire de ressources s’inscrit dans une transaction lorsqu’il commence la participation à cette transaction particulière. L’inscription définit les notifications acceptées par le gestionnaire de ressources. Un gestionnaire des ressources crée un objet d’inscription lorsqu’il s’inscrit dans une transaction. Cet objet signale à KTM que le gestionnaire de ressources (RM) demande des notifications sur la transaction spécifiée.

Le RM fournit une structure de [**\_ masque de notification**](notification-mask.md) qui détaille les notifications qu’il demande.

## <a name="enlistment-functions"></a>Fonctions d’inscription

Les fonctions suivantes sont utilisées avec les enlistes.



| Fonction                                                                          | Description                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Indique qu’un gestionnaire de ressources a terminé la validation d’une transaction qui a été demandée par le gestionnaire de transactions (TM).                                                                                                                                                                                                                                                                        |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Crée une inscription, définit son état initial et ouvre un handle vers l’inscription avec l’accès spécifié.                                                                                                                                                                                                                                                                                          |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Récupère une structure opaque de données de récupération à partir de KTM. Les informations de récupération sont stockées dans un journal au nom d’un gestionnaire de ressources (RM) en appelant la fonction [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) . Après une défaillance, le gestionnaire de données peut utiliser la fonction [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) pour récupérer les informations. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Ouvre un objet d’inscription existant et retourne un handle à l’inscription.                                                                                                                                                                                                                                                                                                                            |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Demande que l’inscription spécifiée soit convertie en une inscription en lecture seule. Une inscription en lecture seule ne peut pas participer au résultat de la transaction et n’est pas enregistrée de façon durable pour la récupération.                                                                                                                                                                                                    |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Restaure la transaction spécifiée associée à une inscription. Cette fonction ne peut pas être appelée pour des enrôlements en lecture seule.                                                                                                                                                                                                                                                                   |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Définit une structure opaque, définie par l’utilisateur, des données de récupération à partir de KTM. Les informations de récupération sont stockées dans un journal au nom d’un gestionnaire de ressources (RM) en appelant [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation). Après une défaillance, le gestionnaire de données peut utiliser [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) pour récupérer les informations.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Indique que le gestionnaire de ressources (RM) refuse une demande en une seule phase. Lorsqu’un gestionnaire de transactions reçoit cet appel, il Initialise une validation en deux phases et envoie une demande de préparation à tous les services RMs inscrites.                                                                                                                                                                                       |



 

 

 



