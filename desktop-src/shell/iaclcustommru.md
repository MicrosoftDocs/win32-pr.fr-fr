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
ms.openlocfilehash: c4130ead959c326da55d2c02726c9db89ce363b616ea34cbfa545d179d1ee139
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937039"
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



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



 

 
