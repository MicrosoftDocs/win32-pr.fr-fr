---
description: L’action DisableRollback désactive la restauration pour le reste de l’installation.
ms.assetid: 5510b393-1f2e-44ba-97f5-663674d55b20
title: Action DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740e838a6dca2d97db616703faf24c590ab69bc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113866"
---
# <a name="disablerollback-action"></a>Action DisableRollback

L’action DisableRollback désactive la [restauration](rollback-installation.md) pour le reste de l’installation. La restauration est désactivée uniquement pour les actions qui sont séquencées après l’action DisableRollback dans les tables de séquence. La restauration est désactivée pour l’ensemble de l’installation si l’action DisableRollback est séquencée avant l' [action InstallInitialize](installinitialize-action.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

Il n’existe aucune restriction de séquence.

## <a name="actiondata-message"></a>Message ActionData

Il n’y a aucun message ActionData.

 

 



