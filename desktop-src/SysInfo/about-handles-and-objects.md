---
description: Le système utilise des objets et des handles pour réguler l’accès aux ressources système pour deux raisons principales.
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: À propos des handles et des objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7474c11298166cc8d63032c6e1d8f84e6db249
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013531"
---
# <a name="about-handles-and-objects"></a>À propos des handles et des objets

Le système utilise des objets et des handles pour réguler l’accès aux ressources système pour deux raisons principales. Tout d’abord, l’utilisation des objets garantit que Microsoft peut mettre à jour les fonctionnalités du système, tant que l’interface d’objet d’origine est conservée. Lorsque des versions ultérieures du système sont publiées, vous pouvez utiliser l’objet mis à jour avec peu ou pas de travail supplémentaire.

deuxièmement, l’utilisation d’objets vous permet de tirer parti de la sécurité Windows. Chaque objet possède sa propre liste de contrôle d’accès (ACL) qui spécifie les actions qu’un processus peut effectuer sur l’objet. Le système examine l’ACL d’un objet chaque fois qu’une application crée un handle pour l’objet. Pour obtenir plus d'informations, voir [Contrôle d'accès](/windows/desktop/SecAuthZ/access-control).

-   [Gestionnaire d’objets](object-manager.md)
-   [Interface d’objet](object-interface.md)
-   [Espaces de noms d’objets](/windows/desktop/Sync/object-namespaces)
-   [Limitations des handles](handle-limitations.md)
-   [Gérer l’héritage](handle-inheritance.md)

 

 
