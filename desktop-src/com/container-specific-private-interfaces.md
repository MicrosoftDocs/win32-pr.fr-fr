---
title: Interfaces privées Container-Specific
description: Interfaces privées Container-Specific
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c6569a79e9f1801c6fd82543bc40408903c780
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311299"
---
# <a name="container-specific-private-interfaces"></a>Interfaces privées Container-Specific

Certains conteneurs fournissent des interfaces privées spécifiques au conteneur pour des fonctionnalités supplémentaires ou des performances améliorées. Les contrôles qui reposent sur ces interfaces spécifiques au conteneur doivent, si possible, travailler sans ces interfaces spécifiques au conteneur pour que le contrôle fonctionne dans différents conteneurs. Par exemple, Visual Basic implémente des interfaces privées qui fournissent des fonctionnalités de mise en forme de chaînes aux contrôles. Si un contrôle utilise ces interfaces de mise en forme privée, il doit pouvoir s’exécuter avec la prise en charge de la mise en forme par défaut si ces interfaces ne sont pas disponibles. Si le contrôle peut fonctionner sans les interfaces privées, il doit prendre les mesures appropriées (par exemple, avertir l’utilisateur de fonctionnalités réduites) tout en continuant à fonctionner. Si ce n’est pas le cas, une catégorie de composant doit être inscrite en fonction des besoins afin que seuls les conteneurs prenant en charge cette fonctionnalité puissent héberger ces contrôles.

 

 




