---
title: Stockage Interface
description: Stockage Interface
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ad0cc646d45ca0b77a70ecaf47d28eadb4d136
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404593"
---
# <a name="storage-interfaces"></a>Stockage Interface

Les conteneurs de contrôle doivent être en mesure de prendre en charge les contrôles qui implémentent [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)ou [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit). Un conteneur peut éventuellement prendre en charge d’autres interfaces de persistance, telles que [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)et [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) , pour les contrôles qui assurent la prise en charge.

une fois qu’un conteneur de contrôle ActiveX a choisi et initialisé une interface de stockage à utiliser ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc.), cette interface de stockage restera l’interface de stockage principal pour la durée de vie du contrôle, c’est-à-dire que le contrôle restera en possession du stockage. Cela n’empêche pas le conteneur d’enregistrer dans d’autres interfaces de stockage.

les conteneurs de contrôle ActiveX n’ont pas besoin de prendre en charge un mécanisme d’enregistrement en tant que texte. par conséquent, l’utilisation de [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) et des [**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) d’interface côté conteneur associés sont facultatives.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Containers](containers.md)
</dt> </dl>

 

 