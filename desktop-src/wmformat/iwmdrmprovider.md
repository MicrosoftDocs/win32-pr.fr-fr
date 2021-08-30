---
title: Interface IWMDRMProvider
description: l’interface IWMDRMProvider fournit une méthode qui crée les autres objets des api étendues du Client Microsoft Windows Media DRM. vous pouvez obtenir un pointeur vers une instance de cette interface en appelant la fonction WMDRMCreateProvider.
ms.assetid: bcd346e3-a79f-49a8-b5f9-b9ae8b54527a
keywords:
- Format Windows Media de l’interface IWMDRMProvider
- Interface IWMDRMProvider format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMProvider
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bfe08a00d94914744f184ac4d0409fed24701985740006841f1d178cc39273e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930119"
---
# <a name="iwmdrmprovider-interface"></a>Interface IWMDRMProvider

l’interface **IWMDRMProvider** fournit une méthode qui crée les autres objets des api étendues du Client Microsoft Windows Media DRM.

Vous pouvez obtenir un pointeur vers une instance de cette interface en appelant la fonction [**WMDRMCreateProvider**](wmdrmcreateprovider.md) . Pour obtenir un pointeur vers une instance de cette interface qui peut créer des objets sécurisés, vous devez appeler la fonction [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) .

## <a name="members"></a>Membres

L’interface **IWMDRMProvider** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMProvider** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMDRMProvider** possède ces méthodes.



| Méthode                                              | Description                                                                                          |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**CreateObject**](iwmdrmprovider-createobject.md) | Récupère un pointeur vers une interface spécifiée, en créant l’objet d’implémentation, si nécessaire.<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

