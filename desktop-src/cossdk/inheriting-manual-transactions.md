---
description: Héritage de transactions manuelles
ms.assetid: 3616275c-1e2d-4f9d-8adf-11ac9be132f1
title: Héritage de transactions manuelles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0042b7bb1e1545c44c44149c4605c9aabcbcc12fecebb974eb97f95da087b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896009"
---
# <a name="inheriting-manual-transactions"></a>Héritage de transactions manuelles

Si un objet avec une transaction BYOT dans son contexte crée un deuxième objet, l’objet en aval peut hériter de la transaction BYOT (si elle est configurée pour hériter des transactions). Le premier objet créé à l’aide de la passerelle BYOT doit être configuré pour « exiger » ou « prendre en charge » les transactions. Les objets suivants dans l’activité peuvent être configurés en fonction des spécifications de l’application.

Pour les transactions automatiques, le runtime COM+ ne tente pas de valider la transaction jusqu’à ce que l’objet racine indique qu’elle est prête (en appelant [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) avant de retourner un appel). Les utilisateurs doivent savoir qu’une transaction BYOT peut être validée prématurément (dans le sens où le travail des objets enfants n’a pas été effectué), parce que la « racine » n’est pas exécutée dans l’environnement d’exécution COM+ et que la sémantique de validation n’est pas liée à la durée de vie de l’objet. En général, l’utilisateur doit veiller à ne pas violer la limite de synchronisation de la transaction.

Dans le cas contraire, les sémantiques de validation COM+ s’appliquent. COM+ ne tente pas de valider une transaction alors qu’un objet dans une limite de synchronisation est en cours d’appel. En outre, les objets peuvent indiquer leur cohérence à l’aide de [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit). Si une tentative est effectuée pour valider une transaction qui inclut le travail d’un objet appelé **DisableCommit**, la transaction est abandonnée.

 

 



