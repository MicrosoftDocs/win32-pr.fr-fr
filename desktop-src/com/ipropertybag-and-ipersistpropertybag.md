---
title: IPropertyBag et IPersistPropertyBag
description: IPropertyBag et IPersistPropertyBag
ms.assetid: 128e847b-99f9-44a3-9176-56eb34f3dddc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de08d8af50ae9a0b91166a4f41c8a11d8c6eb69c4ffd77f93b2566c901342ac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048087"
---
# <a name="ipropertybag-and-ipersistpropertybag"></a>IPropertyBag et IPersistPropertyBag

[**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) et [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) optimisent les mécanismes d’enregistrement en tant que texte. par conséquent, ils sont recommandés pour les conteneurs de contrôle ActiveX qui implémentent un mécanisme d’enregistrement en tant que texte. **IPropertyBag** est implémenté par un conteneur et est approximativement analogue à [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). **IPersistPropertyBag** est implémenté par les contrôles et est à peu près analogue à [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream).

 

 