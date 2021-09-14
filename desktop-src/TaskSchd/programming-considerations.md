---
title: Considérations relatives à la programmation (Planificateur de tâches)
description: Lorsque vous développez des applications qui utilisent le Planificateur de tâches 1,0, gardez à l’esprit les problèmes de programmation suivants. Votre application doit s’assurer que le service Planificateur de tâches est en cours d’exécution avant d’essayer d’effectuer des appels à l’aide de l’API Planificateur de tâches. Lorsque vous récupérez des chaînes, veillez à appeler CoTaskMemFree pour libérer chaque chaîne une fois qu’elle n’est plus nécessaire. Lorsque vous récupérez des tableaux de chaînes, assurez-vous d’abord de libérer chaque chaîne dans le tableau, puis de libérer le tableau lui-même. Lors de la création ou de la modification d’un élément de travail, y compris les déclencheurs associés à un élément de travail, veillez à appeler IPersistFile Save pour enregistrer l’élément de travail sur le disque. Après avoir utilisé l’une des interfaces fournies par l’API Planificateur de tâches, veillez à appeler la version d’IUnknown pour libérer l’interface. IUnknown est pris en charge par chaque objet Planificateur de tâches.
ms.assetid: b9e1806c-acfa-4d44-a371-91bad788648c
keywords:
- démarrage de Planificateur de tâches
- considérations relatives à la programmation Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599652f4a25f3d99020eda0846c41904ee76e5cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122966"
---
# <a name="programming-considerations-task-scheduler"></a>Considérations relatives à la programmation (Planificateur de tâches)

Lorsque vous développez des applications qui utilisent le Planificateur de tâches 1,0, gardez à l’esprit les problèmes de programmation suivants.

-   Votre application doit s’assurer que le service Planificateur de tâches est en cours d’exécution avant d’essayer d’effectuer des appels à l’aide de l’API Planificateur de tâches.
-   Lorsque vous récupérez des chaînes, veillez à appeler [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer chaque chaîne une fois qu’elle n’est plus nécessaire. Lorsque vous récupérez des tableaux de chaînes, assurez-vous d’abord de libérer chaque chaîne dans le tableau, puis de libérer le tableau lui-même.
-   Lors de la création ou de la modification d’un élément de travail, y compris les déclencheurs associés à un élément de travail, veillez à appeler [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) pour enregistrer l’élément de travail sur le disque.
-   Après avoir utilisé l’une des interfaces fournies par l’API Planificateur de tâches, veillez à appeler [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour libérer l’interface. [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) est pris en charge par chaque objet planificateur de tâches.

La section utilisation de la documentation Planificateur de tâches fournit de nombreux exemples qui suivent ces instructions. Le tableau ci-dessous fournit des liens vers certains de ces exemples.

| Pour obtenir un exemple de         | Consultez                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------|
| Libérer des chaînes         | [Récupération d’exemples de propriétés d’élément de travail](retrieving-work-item-property-examples.md)       |
| Enregistrement des éléments de travail sur le disque | [Définition d’exemples de propriétés d’élément de travail](setting-work-item-property-examples.md)             |
| Libérer des interfaces      | [Exemple de création d’une tâche à l’aide de NewWorkItem](creating-a-task-using-newworkitem-example.md) |



 

 

 
