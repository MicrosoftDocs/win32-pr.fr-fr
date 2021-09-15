---
title: Utiliser QueryService pour récupérer une interface native pour un objet IAccessible
description: Les développeurs de serveurs peuvent utiliser cette technique pour exposer un pointeur vers un nœud de document personnalisé pour un objet IAccessible. Cela suppose que vous exposez déjà des objets IAccessible. Cette technique permet aux clients d’obtenir un objet personnalisé à partir d’un objet IAccessible.
ms.assetid: aaa0e840-f8c2-4f3d-9d97-1910f00c1041
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d971462154eb12789a74e8cc6edb5aed68c84b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522749"
---
# <a name="use-queryservice-to-retrieve-a-native-interface-for-an-iaccessible-object"></a>Utiliser QueryService pour récupérer une interface native pour un objet IAccessible

Les développeurs de serveurs peuvent utiliser cette technique pour exposer un pointeur vers un nœud de document personnalisé pour un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Cela suppose que vous exposez déjà des objets **IAccessible** . Cette technique permet aux clients d’obtenir un objet personnalisé à partir d’un objet **IAccessible** .

**Pour exposer un modèle objet natif pour un IAccessible (serveurs)**

1.  Ajoutez la prise en charge de l’interface **IServiceProvider** sur votre objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
2.  Définissez un GUID qui représente les fonctionnalités d’obtention de l’interface personnalisée à partir d’un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . C’est ce que l’on appelle un ID de service. Vous pouvez utiliser GUIDGEN.EXE pour générer un ID de service, ou réutiliser l’ID d’interface si vous disposez d’une interface personnalisée.
3.  Implémentez la méthode **IServiceProvider :: QueryService** afin qu’elle retourne un pointeur vers l’interface personnalisée quand elle est appelée avec l’ID de service défini précédemment dans cette procédure. **QueryService** doit retourner la **valeur null** pour toutes les autres valeurs d’ID de service.
4.  Publiez l’ID de service afin que les clients puissent l’utiliser.

Les clients peuvent utiliser cette fonctionnalité pour obtenir un pointeur vers l’objet personnalisé à partir d’un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

**Pour obtenir un pointeur vers un objet personnalisé à partir d’un IAccessible (clients)**

1.  Appelez [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))(IID \_ IServiceProvider) sur un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour obtenir un pointeur d’interface **IServiceProvider** .
2.  Appelez **IServiceProvider :: QueryService** avec l’ID de service publié pour obtenir un pointeur vers l’objet personnalisé pour [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).
3.  Libérez l’interface **IServiceProvider** si elle n’est plus nécessaire.

Pour être utilisables dans plusieurs processus, les serveurs devront peut-être inscrire l’interface retournée avec le modèle COM (Component Object Model).

Cette technique est utilisée par Microsoft Internet Explorer 4,0 et versions ultérieures. Elle permet aux clients d’obtenir un pointeur d’interface **IHTMLElement2** qui correspond à un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

 

 