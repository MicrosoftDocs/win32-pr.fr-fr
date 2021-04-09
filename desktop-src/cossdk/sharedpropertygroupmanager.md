---
description: Crée des groupes de propriétés partagées et pour obtenir l’accès aux groupes de propriétés partagés existants.
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: SharedPropertyGroupManager, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: 680c5caef996d329e18192193f30841f61f02f27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860977"
---
# <a name="sharedpropertygroupmanager-class"></a>SharedPropertyGroupManager, classe

Crée des groupes de propriétés partagées et pour obtenir l’accès aux groupes de propriétés partagés existants.

Pour plus d’informations sur l’utilisation de l’Gestionnaire de propriétés partagé dans COM+, consultez [Gestionnaire de propriétés partagées com+](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Quand implémenter

Cette classe est implémentée par COM+.



| Condition requise | Valeur |
|------------|--------------------------------------------------------------------|
| CLSID      | CLSID \_ SharedPropertyGroupManager                                  |
| ProgID     | L "MTxSpm. SharedPropertyGroupManager"                               |
| Interfaces | [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez cette classe pour accéder aux méthodes de [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).

## <a name="remarks"></a>Notes

Pour créer cet objet, appelez [**IObjectContext :: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+. Un objet SharedPropertyGroupManager peut être déclaré à l’aide de « COMSVCSLib. SharedPropertyGroupManager » comme nom de classe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[**SharedProperty**](sharedproperty.md)
</dt> <dt>

[**SharedPropertyGroup**](sharedpropertygroup.md)
</dt> </dl>

 

 




