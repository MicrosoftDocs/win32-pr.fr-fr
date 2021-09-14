---
description: récupère des informations sur un assembly lors de l’utilisation du code managé dans le common language runtime .NET Framework.
ms.assetid: 45dcdc6a-74df-4763-ba8b-82f604db78d4
title: ClrAssemblyLocator, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClrAssemblyLocator
api_type:
- COM
ms.openlocfilehash: ff5c1d21525a950208c1b919d4dee0e2122d2e50
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923024"
---
# <a name="clrassemblylocator-class"></a>ClrAssemblyLocator, classe

récupère des informations sur un assembly lors de l’utilisation du code managé dans le common language runtime .NET Framework.

## <a name="when-to-implement"></a>Quand implémenter

Cette classe est implémentée par COM+.



| Condition requise | Valeur |
|------------|-------------------------------------------------------|
| CLSID      | GUID \_ AssemblyLocator                                 |
| ProgID     | L "System. EnterpriseServices. Internal. AssemblyLocator" |
| Interfaces | [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)          |



 

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez cette classe pour accéder aux méthodes de [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).

## <a name="remarks"></a>Notes

Pour créer cet objet, appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des Services COM+. Un objet ClrAssemblyLocator peut être déclaré à l’aide de « COMSVCSLib. ClrAssemblyLocator » comme nom de classe.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                 |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



 

