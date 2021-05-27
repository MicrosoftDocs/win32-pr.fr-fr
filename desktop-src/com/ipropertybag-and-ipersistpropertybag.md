---
title: IPropertyBag et IPersistPropertyBag
description: IPropertyBag et IPersistPropertyBag
ms.assetid: 128e847b-99f9-44a3-9176-56eb34f3dddc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a012fb2c202d93bcf4f4c8fa477133e841740b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549064"
---
# <a name="ipropertybag-and-ipersistpropertybag"></a>IPropertyBag et IPersistPropertyBag

[**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) et [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) optimisent les mécanismes d’enregistrement en tant que texte, et sont donc recommandés pour les conteneurs de contrôles ActiveX qui implémentent un mécanisme d’enregistrement en tant que texte. **IPropertyBag** est implémenté par un conteneur et est approximativement analogue à [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). **IPersistPropertyBag** est implémenté par les contrôles et est à peu près analogue à [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream).

 

 