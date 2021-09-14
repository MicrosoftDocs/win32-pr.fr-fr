---
description: Le regroupement d’applications COM+ permet la mise à l’échelle des processus à thread unique, à l’instar de la façon dont le regroupement de threads permet la mise à l’échelle des objets à thread unique.
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: Concepts de regroupement d’applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a72f5681896e8ac0e6a50b3bddfc16cf4303f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923003"
---
# <a name="com-application-pooling-concepts"></a>Concepts de regroupement d’applications COM+

Le regroupement d’applications COM+ permet la mise à l’échelle des processus à thread unique, à l’instar de la façon dont le regroupement de threads permet la mise à l’échelle des objets à thread unique. Le regroupement d’applications peut également aider à récupérer suite à des défaillances dans des processus uniques en fournissant d’autres processus en cours d’exécution capables de gérer les activations.

> [!Note]  
> Les applications de bibliothèque disposent des propriétés de recyclage et de regroupement de leur processus hôte.

 

Toutes les méthodes de l’interface [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) prennent en charge le regroupement d’applications.

Le regroupement d’applications COM+ est configurable par application à l’aide de la propriété ConcurrentApps de l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection d' [**applications**](applications.md) . ConcurrentApps est une valeur entière qui spécifie le nombre maximal de processus Dllhost simultanés qui doivent être démarrés pour traiter des activations pour une application. Cette propriété peut être définie à l’aide de l’outil d’administration Services de composants ou par programme.

Si la propriété ConcurrentApps est définie sur 1, qui est la valeur par défaut, le service de mise en pool d’applications COM+ est désactivé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches de regroupement d’applications COM+](com--application-pooling-tasks.md)
</dt> <dt>

[Concepts de recyclage des applications COM+](com--application-recycling-concepts.md)
</dt> </dl>

 

 



