---
description: Crée les propriétés partagées et y accède dans un groupe de propriétés partagées.
ms.assetid: 20fd32f0-b2b2-4bed-8c59-1d1fdc8a399e
title: SharedPropertyGroup, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroup
api_type:
- COM
ms.openlocfilehash: a3fff14043d67b96db99334c7bec1afee2577f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748172"
---
# <a name="sharedpropertygroup-class"></a>SharedPropertyGroup, classe

Crée les propriétés partagées et y accède dans un groupe de propriétés partagées.

Pour plus d’informations sur l’utilisation de l’Gestionnaire de propriétés partagé dans COM+, consultez [Gestionnaire de propriétés partagées com+](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Quand implémenter

Cette classe est implémentée par COM+.



| Condition requise | Valeur |
|------------|------------------------------------------------------|
| Interfaces | [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) |



 

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez cette classe pour accéder aux méthodes de [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).

## <a name="remarks"></a>Notes

Vous pouvez créer un objet **SharedPropertyGroup** à l’aide de la méthode [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) de [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).

Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+. Un objet SharedPropertyGroup est créé en appelant la méthode [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) de l’objet [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)
</dt> <dt>

[**SharedProperty**](sharedproperty.md)
</dt> <dt>

[**SharedPropertyGroupManager**](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




