---
title: Interfaces de stockage
description: Interfaces de stockage
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ad0cc646d45ca0b77a70ecaf47d28eadb4d136
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549264"
---
# <a name="storage-interfaces"></a>Interfaces de stockage

Les conteneurs de contrôle doivent être en mesure de prendre en charge les contrôles qui implémentent [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)ou [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit). Un conteneur peut éventuellement prendre en charge d’autres interfaces de persistance, telles que [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)et [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) , pour les contrôles qui assurent la prise en charge.

Une fois qu’un conteneur de contrôles ActiveX a choisi et initialisé une interface de stockage à utiliser ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc.), cette interface de stockage restera l’interface de stockage principal pour la durée de vie du contrôle, c’est-à-dire que le contrôle restera en possession du stockage. Cela n’empêche pas le conteneur d’enregistrer dans d’autres interfaces de stockage.

Les conteneurs de contrôles ActiveX n’ont pas besoin de prendre en charge un mécanisme d’enregistrement en tant que texte. par conséquent, l’utilisation de [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) et de l’interface côté conteneur associée [**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) est facultative.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Containers](containers.md)
</dt> </dl>

 

 