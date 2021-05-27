---
title: Interfaces de persistance
description: Interfaces de persistance
ms.assetid: a93582b3-bdbf-430d-b4a6-c0df7bc35dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e1acbd1074fd5fa4e87e571a1e21ab48d5d075
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550504"
---
# <a name="persistence-interfaces"></a>Interfaces de persistance

Les objets qui ont un état persistant de tout type doivent implémenter au moins une \* interface IPersist et, de préférence, plusieurs interfaces, afin de fournir au conteneur le choix le plus flexible pour enregistrer l’état d’un contrôle.

Si un contrôle n’a aucun état persistant, il doit, au minimum, implémenter [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) ou [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) (les deux sont mutuellement exclusifs et ne doivent pas être implémentés ensemble pour la plupart). Ce dernier est utilisé lorsqu’un contrôle souhaite savoir quand il est créé au lieu d’être rechargé à partir d’un état persistant existant (**IPersistStream** n’a pas la nouvelle fonctionnalité créée). L’existence de l’une ou l’autre des interfaces indique que le contrôle peut enregistrer et charger son état persistant dans un flux, autrement dit, une instance de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).

Au-delà de ces deux interfaces basées sur le flux, les \* interfaces IPersist listées dans le tableau suivant peuvent éventuellement être fournies afin de prendre en charge la persistance dans des emplacements autres qu’un [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)extensible.

Un ensemble de catégories de composants est identifié pour couvrir la prise en charge des interfaces persistances, consultez [catégories de composants](component-categories.md).



| Interface                                                              | Utilisation                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))<br/>           | L’objet peut enregistrer et charger son état dans un tableau d’octets séquentiels de longueur fixe (en mémoire).<br/>                                                                                                                                                                                                                                                    |
| [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/>                  | L’objet peut enregistrer et charger son état dans une instance [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) . Les contrôles qui souhaitent être marqués comme pouvant être insérés comme d’autres objets de document composés (pour l’insertion dans des conteneurs ne prenant pas en charge les contrôles) doivent prendre en charge cette interface.<br/>                                                                                               |
| [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)<br/> | L’objet peut enregistrer et charger son état en tant que propriétés individuelles écrites dans IPropertyBag que le conteneur implémente. Il est utilisé pour la fonctionnalité enregistrer en tant que texte dans certains conteneurs.<br/>                                                                                                                                                          |
| [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/>  | L’objet peut enregistrer et charger son état dans un emplacement nommé par un moniker. Le contrôle appelle [**IMoniker :: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) pour récupérer l’interface de stockage dont il a besoin, par exemple [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/objidl/nn-objidl-ilockbytes), [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject), etc.<br/> |



 

Alors que la prise en charge de [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) est facultative, il est fortement recommandé d’en faire une optimisation pour les conteneurs avec des fonctionnalités d’enregistrement sous forme de texte, telles que Visual Basic.

À l’exception de [**IPersistStream :: GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax), [**IPersistStreamInit :: GetSizeMax**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-getsizemax)et [**IPersistMemory :: GetSizeMax**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768208(v=vs.85)), toutes les méthodes de chaque interface doivent être entièrement implémentées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôles](controls.md)
</dt> </dl>

 

