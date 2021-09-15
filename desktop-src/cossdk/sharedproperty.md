---
description: Définit ou récupère la valeur d’une propriété partagée.
ms.assetid: 19ed8d50-3ac1-408e-9f25-09f284d025f1
title: SharedProperty, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedProperty
api_type:
- COM
ms.openlocfilehash: a7a7857ad280ad722601bdced6c25d04b03dc0b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310961"
---
# <a name="sharedproperty-class"></a>SharedProperty, classe

Définit ou récupère la valeur d’une propriété partagée.

Pour obtenir des informations générales sur l’utilisation de l’Gestionnaire de propriétés partagé dans COM+, consultez [Gestionnaire de propriétés partagées com+](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Quand implémenter

Cette classe est implémentée par COM+.



| Condition requise | Valeur |
|------------|--------------------------------------------|
| Interfaces | [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) |



 

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez cette classe pour accéder aux méthodes de [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty).

## <a name="remarks"></a>Notes

Vous pouvez créer un objet **SharedProperty** à l’aide des méthodes [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) ou [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) de [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).

pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des Services COM+. Un objet SharedProperty est créé en appelant les méthodes [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) ou [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) de l’objet [**SharedPropertyGroup**](sharedpropertygroup.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)
</dt> <dt>

[**SharedPropertyGroup**](sharedpropertygroup.md)
</dt> <dt>

[**SharedPropertyGroupManager**](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




