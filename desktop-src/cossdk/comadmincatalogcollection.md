---
description: Représente n’importe quelle collection dans le catalogue COM+. Utilisez-le pour énumérer, ajouter, supprimer et récupérer des éléments dans une collection et pour accéder aux regroupements associés.
ms.assetid: 2530e44f-c428-4baa-88e1-8d01eaf234cc
title: COMAdminCatalogCollection, classe (comadmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogCollection
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 985a6b947708542ec3ce1dc6ecc835c94259b315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748661"
---
# <a name="comadmincatalogcollection-class"></a>COMAdminCatalogCollection, classe

Représente n’importe quelle collection dans le catalogue COM+. Utilisez-le pour énumérer, ajouter, supprimer et récupérer des éléments dans une collection et pour accéder aux regroupements associés.

## <a name="when-to-implement"></a>Quand implémenter

Cette classe est implémentée par COM+.



| Condition requise | Valeur |
|------------|--------------------------------------------------|
| Interfaces | [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez des objets créés à partir de la classe **COMAdminCatalogCollection** lorsque vous souhaitez manipuler par programmation une collection dans le catalogue com+. Ces regroupements correspondent aux dossiers de l’outil d’administration Services de composants. Les éléments contenus dans les dossiers correspondent à des éléments dans des collections, que vous pouvez représenter à l’aide d’objets créés à partir de la classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .

Pour plus d’informations sur les regroupements du catalogue et leurs propriétés, consultez [regroupements d’administration com+](com--administration-collections.md).

Pour une introduction à l’administration par programme de COM+, consultez automatisation de l' [administration com+](automating-com--administration.md).

## <a name="remarks"></a>Notes

Vous ne pouvez pas créer directement un objet **COMAdminCatalogCollection** . Pour utiliser les méthodes de cet objet, vous devez créer un objet [**COMAdminCatalog**](comadmincatalog.md) , obtenir une référence à [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), puis utiliser [**ICOMAdminCatalog :: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) pour obtenir une référence à une interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) qui représente une collection de niveau supérieur. Cela est illustré dans l’exemple suivant, où « cocollection » doit être remplacé par le nom de l’une des collections d’administration COM+ de niveau supérieur.


```C++
    HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pCatalog->GetCollection(L"TopCollection", 
      (IDispatch**)&pTopColl);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
```



Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types d’administration COM+. Un objet COMAdminCatalogCollection peut être créé en appelant [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) sur un objet [**COMAdminCatalog**](comadmincatalog.md) . Cela est illustré dans l’exemple suivant, où « cocollection » doit être remplacé par le nom de l’une des collections d’administration COM+ de niveau supérieur.


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Comadmin. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Comadmin. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COMAdminCatalog**](comadmincatalog.md)
</dt> <dt>

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




