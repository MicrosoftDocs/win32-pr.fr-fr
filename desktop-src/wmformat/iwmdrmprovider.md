---
title: Interface IWMDRMProvider
description: L’interface IWMDRMProvider fournit une méthode qui crée les autres objets des API étendues du client Microsoft Windows Media DRM. vous pouvez obtenir un pointeur vers une instance de cette interface en appelant la fonction WMDRMCreateProvider.
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
ms.openlocfilehash: 9653bc612cdbc865d8e77cb7916b0b8f54d0fd0e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729213"
---
# <a name="iwmdrmprovider-interface"></a>Interface IWMDRMProvider

L’interface **IWMDRMProvider** fournit une méthode qui crée les autres objets des API étendues du client Microsoft Windows Media DRM.

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

 

