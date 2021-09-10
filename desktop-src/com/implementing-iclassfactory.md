---
title: Implémentation de IClassFactory
description: Implémentation de IClassFactory
ms.assetid: 96466756-c135-4ee5-a48c-f31129878473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b057657508b3060506c15c68308ea6a5332e5099
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363371"
---
# <a name="implementing-iclassfactory"></a>Implémentation de IClassFactory

Lorsqu’un client utilise un CLSID pour demander la création d’une instance d’objet, la première étape est la création d’un objet de classe, un objet intermédiaire qui contient une implémentation des méthodes de l’interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) . Bien que COM fournisse plusieurs fonctions de création d’instance, la première étape de l’implémentation de ces fonctions est la création d’un objet de classe.

Par conséquent, tous les serveurs doivent implémenter les méthodes de l’interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , qui contient deux méthodes :

-   [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance). Cette méthode doit créer une instance non initialisée de l’objet et retourner un pointeur vers une interface demandée sur l’objet.
-   [**LockServer,**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver). Cette méthode incrémente simplement le nombre de références sur l’objet de classe pour s’assurer que le serveur reste en mémoire et ne s’arrête pas avant que le client ne soit prêt à le faire.

Pour permettre à un serveur d’être responsable de sa propre licence, COM définit [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), qui hérite sa définition d' [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Ainsi, un serveur qui implémente **IClassFactory2** doit, par définition, implémenter les méthodes d' **IClassFactory**.

COM fournit également des fonctions d’assistance pour l’implémentation de serveurs hors processus. Pour plus d’informations, consultez [assistance pour l’implémentation du serveur out-of-process](out-of-process-server-implementation-helpers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Responsabilités du serveur COM](com-server-responsibilities.md)
</dt> <dt>

[Licences et IClassFactory2](licensing-and-iclassfactory2.md)
</dt> </dl>

 

 