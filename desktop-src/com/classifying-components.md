---
title: Classification des composants
description: Classification des composants
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e8382c1cbada72c2a8ab480ded78702424736850299b9e5e9fad7b328e3280
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048707"
---
# <a name="classifying-components"></a>Classification des composants

Lorsqu’un client peut parcourir la liste des CLSID du Registre et sélectionner un composant à utiliser, le chargement de chaque composant dans le registre et l’interrogation de ses interfaces prises en charge sont très longs. Pour déterminer si un composant prend en charge les interfaces requises avant de créer une instance du composant, une méthode de classification des composants en catégories a été développée.

Une catégorie de composant est un ensemble d’interfaces auxquelles un GUID nommé CATID a été affecté. Les composants qui implémentent toutes les interfaces dans une catégorie de composant s’inscrivent en tant que membres de cette catégorie de composant. Vous pouvez ensuite sélectionner des composants appartenant à une certaine catégorie de composants dans le registre. En s’inscrivant lui-même en tant que membre d’une catégorie de composant, le composant garantit qu’il prend en charge toutes les interfaces membres dans la catégorie de composant.

Un composant peut être membre de nombreuses catégories. Elle n’est pas limitée à la prise en charge des interfaces dans une catégorie de composant. Elle peut prendre en charge n’importe quelle interface, en plus de celles qui se trouvent dans une catégorie de composant.

Contrairement à l’inscription standard des composants, dans laquelle les développeurs doivent écrire du code qui enregistre manuellement les objets, les catégories de composants automatisent la majeure partie de ce travail. Les six méthodes de l’interface [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) définissent les catégories de composants et inscrivent les objets qui les implémentent ou les nécessitent. L’objet [Gestionnaire de catégories de composants](the-component-categories-manager.md) implémente cette interface. Pour plus d’informations sur l’utilisation des catégories de composants, consultez **ICatRegister** et [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription des applications COM](registering-com-applications.md)
</dt> </dl>

 

 




