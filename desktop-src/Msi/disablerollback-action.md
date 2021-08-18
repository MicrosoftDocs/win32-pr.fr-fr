---
description: L’action DisableRollback désactive la restauration pour le reste de l’installation.
ms.assetid: 5510b393-1f2e-44ba-97f5-663674d55b20
title: Action DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbe500e3b810e5b06802e3a0face1da9b76441099a407882da08d5911a37d60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745369"
---
# <a name="disablerollback-action"></a>Action DisableRollback

L’action DisableRollback désactive la [restauration](rollback-installation.md) pour le reste de l’installation. La restauration est désactivée uniquement pour les actions qui sont séquencées après l’action DisableRollback dans les tables de séquence. La restauration est désactivée pour l’ensemble de l’installation si l’action DisableRollback est séquencée avant l' [action InstallInitialize](installinitialize-action.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

Il n’existe aucune restriction de séquence.

## <a name="actiondata-message"></a>Message ActionData

Il n’y a aucun message ActionData.

 

 



