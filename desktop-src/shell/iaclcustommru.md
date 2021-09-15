---
description: Expose les méthodes utilisées pour initialiser une liste des derniers fichiers utilisés pour un objet de saisie semi-automatique.
title: Interface IACLCustomMRU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU
api_type:
- COM
api_location: ''
ms.assetid: 6ebf64da-9eba-4ea7-91aa-242474097be1
ms.openlocfilehash: f47a9df320da5c710c21ddbab83ca87b49c28e12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523364"
---
# <a name="iaclcustommru-interface"></a>Interface IACLCustomMRU

Expose les méthodes utilisées pour initialiser une liste des derniers fichiers utilisés pour un objet de saisie semi-automatique.

## <a name="members"></a>Membres

L’interface **IACLCustomMRU** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IACLCustomMRU** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IACLCustomMRU** possède ces méthodes.



| Méthode                                             | Description                                                             |
|:---------------------------------------------------|:------------------------------------------------------------------------|
| [**AddMRUString**](iaclcustommru-addmrustring.md) | Ajoute une entrée à la liste MRU.<br/>                               |
| [**Initialiser**](iaclcustommru-initialize.md)     | Charge une liste de chaînes dans la liste MRU à partir du Registre.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



 

 
