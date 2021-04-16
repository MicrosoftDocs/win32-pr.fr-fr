---
title: Terminologie des canaux essentiels
description: Comme les autres types de paramètres pour les appels de procédure distante, les canaux peuvent être \ dans \ ou \ out \ Parameters.
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df183d18d7962ad0c63ecaa0d350006a4144f23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508069"
---
# <a name="essential-pipe-terminology"></a>Terminologie des canaux essentiels

Comme les autres types de paramètres pour les appels de procédure distante, les canaux peuvent être \[ [**des**](/windows/desktop/Midl/in) \] paramètres in ou \[ [**out**](/windows/desktop/Midl/out-idl) \] . Étant donné que le serveur contrôle le transfert de données via un canal, les canaux avec l' \[  \] attribut in sont dits pour *extraire* des données vers le serveur. De même, les canaux de sortie *poussent* les données du serveur vers le client. Les procédures de transfert de données sont appelées « *procédure pull* » et « *Push Procedure »*, respectivement.

Le compilateur MIDL génère les procédures push et pull pour le serveur. En outre, il gère l’allocation des tampons de données en mémoire. Toutefois, le client doit fournir ses propres procédures push et pull. Il doit également fournir une procédure pour l’allocation des mémoires tampons utilisées par le canal. Celles-ci sont appelées automatiquement au moment approprié par le stub client. La procédure d’allocation est souvent appelée procédure Alloc ou Alloc.

 

 