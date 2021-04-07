---
title: Gestionnaire par défaut et gestionnaires personnalisés
description: Gestionnaire par défaut et gestionnaires personnalisés
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dfd152a9f7b20b8ba1553db4efc9b57bffef60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939787"
---
# <a name="the-default-handler-and-custom-handlers"></a>Gestionnaire par défaut et gestionnaires personnalisés

Le gestionnaire par défaut, une implémentation fournie par OLE, est utilisé par la plupart des applications comme gestionnaire. Une application implémente un gestionnaire personnalisé lorsque les fonctionnalités du gestionnaire par défaut sont insuffisantes. Un gestionnaire personnalisé peut remplacer complètement le gestionnaire par défaut ou utiliser des parties de la fonctionnalité qu’il fournit, le cas échéant. Dans ce dernier cas, le gestionnaire d’application est implémenté comme un objet d’agrégation composé d’un nouvel objet de contrôle et du gestionnaire par défaut. Les gestionnaires d’applications/par défaut combinés sont également appelés *gestionnaires in-process*. Le *Gestionnaire de communication à distance* est utilisé pour les objets qui ne sont pas affectés à un CLSID dans le registre système ou qui n’ont pas de gestionnaire spécifié. Tout ce qui est nécessaire à partir d’un gestionnaire pour ces types d’objets est qu’ils passent des informations à travers la limite de processus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaires d’objets](object-handlers.md)
</dt> </dl>

 

 




