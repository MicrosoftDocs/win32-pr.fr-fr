---
description: Une application s’exécutant en tant qu’utilisateur standard effectue des opérations qui requièrent des privilèges d’administrateur en créant un objet de modèle d’objet de composant avec élévation de privilèges.
ms.assetid: 246fdf74-cc5b-47b1-b3a8-20441544e7be
title: Modèle d’objet COM administrateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b331d71f83428ad821bc1c2f9de24984025aaf7f95874c2203ee9fb1f9158a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784786"
---
# <a name="administrator-com-object-model"></a>Modèle d’objet COM administrateur

Dans le modèle objet COM de l’administrateur, une application qui s’exécute en tant qu’utilisateur standard effectue des opérations qui requièrent des privilèges d’administrateur en créant un objet de [modèle d’objet de composant](/windows/desktop/com/component-object-model--com--portal) avec élévation de privilèges. Pour plus d’informations sur la création d’un objet COM élevé, consultez [le moniker d’élévation com](../com/the-com-elevation-moniker.md).

L’un des inconvénients de l’utilisation du modèle d’objet COM administrateur est que l’utilisateur est invité à chaque fois qu’une opération privilégiée est effectuée.

Toute interface utilisateur qui peut contrôler l’objet COM doit être présentée par l’objet COM lui-même. Dans le cas contraire, un processus non privilégié peut entraîner l’exécution d’opérations privilégiées par l’objet COM élevé, sans que l’utilisateur soit invité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’applications nécessitant des privilèges d’administrateur](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modèle de Broker administrateur](administrator-broker-model.md)
</dt> <dt>

[Modèle de tâche avec élévation de privilèges](elevated-task-model.md)
</dt> <dt>

[Modèle de service du système d’exploitation](operating-system-service-model.md)
</dt> </dl>

 

 
