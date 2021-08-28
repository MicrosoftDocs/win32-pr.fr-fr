---
title: Terminologie des canaux essentiels
description: Comme les autres types de paramètres pour les appels de procédure distante, les canaux peuvent être \ dans \ ou \ out \ Parameters.
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 389885f440faa477ab22f2100685e2955cbf9fb7ddc4ffcb6440dc4b6f68e003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930068"
---
# <a name="essential-pipe-terminology"></a>Terminologie des canaux essentiels

Comme les autres types de paramètres pour les appels de procédure distante, les canaux peuvent être \[ [**des**](/windows/desktop/Midl/in) \] paramètres in ou \[ [**out**](/windows/desktop/Midl/out-idl) \] . Étant donné que le serveur contrôle le transfert de données via un canal, les canaux avec l' \[  \] attribut in sont dits pour *extraire* des données vers le serveur. De même, les canaux de sortie *poussent* les données du serveur vers le client. Les procédures de transfert de données sont appelées « *procédure pull* » et « *Push Procedure »*, respectivement.

Le compilateur MIDL génère les procédures push et pull pour le serveur. En outre, il gère l’allocation des tampons de données en mémoire. Toutefois, le client doit fournir ses propres procédures push et pull. Il doit également fournir une procédure pour l’allocation des mémoires tampons utilisées par le canal. Celles-ci sont appelées automatiquement au moment approprié par le stub client. La procédure d’allocation est souvent appelée procédure Alloc ou Alloc.

 

 