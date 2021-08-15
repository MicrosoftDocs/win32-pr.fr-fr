---
description: Le système utilise des objets et des handles pour réguler l’accès aux ressources système pour deux raisons principales.
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: À propos des handles et des objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eee99e0568a0535462e89bfd5de71e12cfaf4a588a605f190dba41ce0ef2535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959047"
---
# <a name="about-handles-and-objects"></a>À propos des handles et des objets

Le système utilise des objets et des handles pour réguler l’accès aux ressources système pour deux raisons principales. Tout d’abord, l’utilisation des objets garantit que Microsoft peut mettre à jour les fonctionnalités du système, tant que l’interface d’objet d’origine est conservée. Lorsque des versions ultérieures du système sont publiées, vous pouvez utiliser l’objet mis à jour avec peu ou pas de travail supplémentaire.

deuxièmement, l’utilisation d’objets vous permet de tirer parti de la sécurité Windows. Chaque objet possède sa propre liste de contrôle d’accès (ACL) qui spécifie les actions qu’un processus peut effectuer sur l’objet. Le système examine l’ACL d’un objet chaque fois qu’une application crée un handle pour l’objet. Pour obtenir plus d'informations, voir [Contrôle d'accès](/windows/desktop/SecAuthZ/access-control).

-   [Gestionnaire d’objets](object-manager.md)
-   [Interface d’objet](object-interface.md)
-   [Espaces de noms d’objets](/windows/desktop/Sync/object-namespaces)
-   [Limitations des handles](handle-limitations.md)
-   [Gérer l’héritage](handle-inheritance.md)

 

 
