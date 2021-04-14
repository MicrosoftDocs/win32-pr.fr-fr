---
description: Lie un objet managé à un domaine d’application, qui est un environnement isolé dans lequel les applications s’exécutent.
ms.assetid: 9357ea5d-6f86-4747-a923-16575ff13122
title: AppDomainHelper, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AppDomainHelper
api_type:
- COM
ms.openlocfilehash: 6b4fbedbca631ec49dc2e416d939abdeb239e5b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523444"
---
# <a name="appdomainhelper-class"></a>AppDomainHelper, classe

Lie un objet managé à un domaine d’application, qui est un environnement isolé dans lequel les applications s’exécutent.

## <a name="when-to-implement"></a>Quand implémenter

Cette classe est implémentée par COM+.



| Condition requise | Valeur |
|------------|-------------------------------------------------------|
| CLSID      | GUID \_ AppDomainHelper                                 |
| ProgID     | L "System. EnterpriseServices. Internal. AppDomainHelper" |
| Interfaces | [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)          |



 

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez cette classe pour accéder aux méthodes de [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).

## <a name="remarks"></a>Notes

Pour créer cet objet, appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+. Un objet AppDomainHelper peut être déclaré à l’aide de « COMSVCSLib. AppDomainHelper » comme nom de classe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)
</dt> </dl>

 

