---
description: Accède aux données stockées dans le catalogue COM+.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: COMAdminCatalog, classe (comadmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalog
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 8be3f0f3f9aa59c2199c50b73b8a4d4488b0c9a65d3e0679b65350d6b8b07fd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128991"
---
# <a name="comadmincatalog-class"></a>COMAdminCatalog, classe

Accède aux données stockées dans le catalogue COM+.

## <a name="when-to-implement"></a>Quand implémenter

Cette classe est implémentée par COM+.



| Condition requise | Valeur |
|------------|-------------------------------------------------------------------------------------------------------------------|
| CLSID      | CLSID \_ COMAdminCatalog                                                                                            |
| ProgID     | L « comadmin. COMAdminCatalog »                                                                                       |
| Interfaces | [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a>Quand l’utiliser

Vous utilisez les objets créés à partir de la classe **COMAdminCatalog** pour commencer l’accès par programme aux données de configuration com+ stockées dans le catalogue com+. Ces informations sous-tendent les dossiers et les éléments de l’arborescence de la console de l’outil d’administration Services de composants. La classe **COMAdminCatalog** vous permet d’accéder à des regroupements dans le catalogue, d’installer des applications et des composants com+, de démarrer et d’arrêter des services et de se connecter à des serveurs distants et de les administrer.

Les dossiers de l’outil d’administration Services de composants correspondent aux regroupements du catalogue, que vous pouvez représenter à l’aide d’objets créés à partir de la classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) . Les éléments des dossiers correspondent aux éléments des collections, que vous pouvez représenter à l’aide d’objets créés à partir de la classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .

Les collections et les éléments exposés via [**COMAdminCatalogCollection**](comadmincatalogcollection.md) et [**COMAdminCatalogObject**](comadmincatalogobject.md) ne sont pas tous disponibles dans l’outil d’administration Services de composants.

Pour plus d’informations sur des regroupements spécifiques et leurs propriétés, consultez [regroupements d’administration com+](com--administration-collections.md).

Pour une introduction à l’administration par programme de COM+, consultez automatisation de l' [administration com+](automating-com--administration.md).

## <a name="remarks"></a>Remarques

Pour créer cet objet, appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types d’administration COM+. Un objet COMAdminCatalog peut être déclaré à l’aide de « comadmin. COMAdminCatalog » comme nom de classe.

dans COM+ 1,5, fourni avec Windows XP, la classe **COMAdminCatalog** implémente l’interface [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) . toutefois, dans COM+ 1,0, fourni avec Windows 2000, la classe **COMAdminCatalog** implémente uniquement l’interface [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Comadmin. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Comadmin. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COMAdminCatalogCollection**](comadmincatalogcollection.md)
</dt> <dt>

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
</dt> <dt>

[**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
</dt> </dl>

 

