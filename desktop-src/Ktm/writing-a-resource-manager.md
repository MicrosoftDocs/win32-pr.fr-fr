---
description: Si vous écrivez un service ou un composant et que vous devez utiliser des services transactionnels ou si vous devez surveiller l’état d’une transaction de noyau, vous devez créer un gestionnaire de ressources (RM).
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Écriture d’un Gestionnaire des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c47f9a0704f6edaea02d752fe39f01fce61c0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517802"
---
# <a name="writing-a-resource-manager"></a>Écriture d’un Gestionnaire des ressources

Si vous écrivez un service ou un composant et que vous devez utiliser des services transactionnels ou si vous devez surveiller l’état d’une transaction de noyau, vous devez créer un gestionnaire de ressources (RM).

Pour écrire un gestionnaire de ressources, vous devez créer plusieurs objets de noyau. Les objets utilisés par un RM sont les suivants :

-   Objets du gestionnaire de transactions (TM)
-   Objets Gestionnaire des ressources
-   Objets d’inscription

Tout d’abord, créez un objet TM. Il existe deux types de TMs :

-   Volatile : ces TMs n’ont pas de journal et ne peuvent pas récupérer leur état
-   Durable : ces TMs ont un journal

Pour créer un TM durable, vous devez créer un journal CLFS et appeler [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) ou faire en sorte que KTM le crée pour vous. Après la création d’un TM fiable, vous devez d’abord récupérer le TM en appelant [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager). Une fois le TM récupéré, il peut être utilisé.

Si vous récupérez une TM existante, tous les services RMs associés à ce TM commencent à recevoir des messages de récupération. Pour plus d’informations, consultez traitement de la [récupération](recovery-processing.md).

Ensuite, vous créez un gestionnaire de ressources en appelant [**CreateResourceManager,**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) avec le handle TM. Le RM peut être volatile ou durable. Seul TMs durable peut être utilisé avec le RMs durable.

Lorsque vous travaillez de façon transactionnelle, vous vous inscrivez à la transaction en appelant [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)et en spécifiant les notifications à recevoir.

**Remarque**  Vous pouvez commencer à recevoir des notifications avant la fin de l’appel à [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) .

Quand vous recevez une notification, appelez la fonction « Complete \* » appropriée quand une tâche associée au traitement de la notification est terminée. Les fonctions complètes sont les suivantes :

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PreprepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

Si, à un moment donné, un gestionnaire de ressources n’est pas en mesure de terminer le travail de la transaction, ou si la poursuite du rendu de votre application ne peut pas annuler le travail effectué dans la transaction, vous devez restaurer la transaction en appelant [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).

 

 



