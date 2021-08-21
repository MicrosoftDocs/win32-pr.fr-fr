---
title: Propriétés ITsSbTaskInfo
description: L’interface ITsSbTaskInfo expose les propriétés suivantes.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d91b24b95b6b19cb439350c0c6823306c66a8fab5fe47f0f9e9fb739df64e3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128067"
---
# <a name="itssbtaskinfo-properties"></a>Propriétés ITsSbTaskInfo

L’interface [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) expose les propriétés suivantes.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**Propriété de contexte**](itssbtaskinfo-context.md)
</dt> <dd>

Récupère les octets de contexte associés à la tâche.

</dd> <dt>

[**Propriété échéance**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

Récupère l’heure à laquelle la tâche doit être lancée. Cela permet de hiérarchiser les correctifs. Le correctif avec l’échéance la plus proche sera initié en premier.

</dd> <dt>

[**EndTime, propriété**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

Récupère la dernière heure à laquelle l’agent de tâche peut démarrer la tâche.

</dd> <dt>

[**Propriété Identificateur**](itssbtaskinfo-identifier.md)
</dt> <dd>

Récupère un GUID utilisé en tant qu’identificateur unique par l’agent de tâche.

</dd> <dt>

[**propriété Label**](itssbtaskinfo-label.md)
</dt> <dd>

Récupère l’étiquette qui décrit l’objectif de la tâche.

</dd> <dt>

[**Propriété de plug-in**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

Récupère le nom complet de l’agent de tâche.

</dd> <dt>

[**StartTime, propriété**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

Récupère le moment où l’agent de tâche peut démarrer la tâche au plus tôt.

</dd> <dt>

[**Status (propriété)**](itssbtaskinfo-status.md)
</dt> <dd>

Récupère une valeur d’énumération de l' [**\_ \_ État de la tâche RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) qui représente l’état de la tâche.

</dd> <dt>

[**Propriété TargetId**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

Récupère l’identificateur cible.

</dd> </dl>

 

 




