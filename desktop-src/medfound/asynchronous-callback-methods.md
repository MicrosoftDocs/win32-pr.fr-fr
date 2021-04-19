---
description: Méthodes de rappel asynchrones
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Méthodes de rappel asynchrones
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0064873a5b026b6910597ebc9911f56f00584b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515806"
---
# <a name="asynchronous-callback-methods"></a>Méthodes de rappel asynchrones

Media Foundation offre un moyen cohérent d’implémenter des méthodes asynchrones à l’aide d’une interface de rappel.

Cette section décrit comment implémenter l’interface de rappel et comment écrire des méthodes asynchrones qui utilisent cette interface. Elle contient les rubriques suivantes.



| Rubrique                                                                                | Description                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Appeler des méthodes asynchrones](calling-asynchronous-methods.md)                     | Comment appeler des méthodes asynchrones dans Media Foundation.                                               |
| [Implémentation du rappel asynchrone](implementing-the-asynchronous-callback.md) | Comment implémenter la méthode de rappel dans l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . |
| [Prise en charge de plusieurs rappels](supporting-multiple-callbacks.md)                   | Comment prendre en charge plusieurs rappels au sein de la même classe C++.                                        |
| [Files d’attente de travail](work-queues.md)                                                       | Les files d’attente de travail offrent un moyen efficace d’effectuer des opérations asynchrones sur un autre thread.          |
| [Écriture d’une méthode asynchrone](writing-an-asynchronous-method.md)                 | Comment implémenter des méthodes asynchrones dans Media Foundation.                                          |
| [Objets de résultats asynchrones personnalisés](custom-asynchronous-result-objects.md)         | Comment fournir une implémentation personnalisée de l’interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[**Interface IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[API de plateforme Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



