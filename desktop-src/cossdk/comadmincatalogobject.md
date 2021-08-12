---
description: Représente des éléments dans les collections du catalogue COM+. Utilisez-le pour récupérer et modifier les propriétés exposées par un élément dans une collection.
ms.assetid: 1d7f248b-20ec-4b34-88ab-3c68bef72b5a
title: COMAdminCatalogObject, classe (comadmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogObject
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: bce57021774b3abc2f69a1120862912452629c3e70d9c8fd0ebcc5d39ce5203d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548586"
---
# <a name="comadmincatalogobject-class"></a>COMAdminCatalogObject, classe

Représente des éléments dans les collections du catalogue COM+. Utilisez-le pour récupérer et modifier les propriétés exposées par un élément dans une collection.

## <a name="when-to-implement"></a>Quand implémenter

Cette classe est implémentée par COM+.



| Condition requise | Valeur |
|------------|------------------------------------------|
| Interfaces | [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez les objets créés à partir de la classe **COMAdminCatalogObject** pour modifier les propriétés des éléments contenus dans les collections du catalogue com+. Ces éléments correspondent aux éléments affichés dans les dossiers de l’arborescence de la console de l’outil d’administration Services de composants. Les dossiers de l’outil d’administration Services de composants correspondent aux regroupements du catalogue, que vous pouvez représenter à l’aide d’objets créés à partir de la classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

Les collections et les éléments exposés via [**COMAdminCatalogCollection**](comadmincatalogcollection.md) et **COMAdminCatalogObject** ne sont pas tous disponibles dans l’outil d’administration Services de composants.

Pour plus d’informations sur des regroupements spécifiques et leurs propriétés, consultez [regroupements d’administration com+](com--administration-collections.md).

Pour une introduction à l’administration par programme de COM+, consultez automatisation de l' [administration com+](automating-com--administration.md).

## <a name="remarks"></a>Remarques

Vous ne pouvez pas créer directement un objet **COMAdminCatalogObject** . Pour utiliser les méthodes de cet objet, vous devez créer un objet [**COMAdminCatalog**](comadmincatalog.md) , obtenir une référence [**à ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), puis utiliser [**ICOMAdminCatalog :: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) pour obtenir une référence à une interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) qui représente une collection de niveau supérieur ou utiliser [**ICatalogCollection :: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) pour accéder aux collections qui ne sont pas de niveau supérieur.

Une fois que vous avez une référence à l’interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) de la collection qui vous intéresse, appelez [**ICatalogCollection ::P opulate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) pour remplir la collection avec tous ses éléments. Itérez au sein de chacun des éléments de la collection en appelant [**ICatalogCollection :: obtenir l' \_ élément**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) pour obtenir une référence à chaque interface [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) . Lorsque vous trouvez l’élément qui vous intéresse, vous pouvez modifier les propriétés de l’élément et quitter l’itération. Si vous apportez des modifications à des éléments d’une collection, vous devez appeler [**ICatalogCollection :: SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) pour enregistrer les modifications dans le catalogue com+.

Cela est illustré dans l’exemple suivant, où « la collection de la collection » doit être remplacée par le nom de l’une des collections d’administration COM+ de niveau supérieur ; « ItemName » doit être remplacé par le nom de l’élément qui vous intéresse ; « PropertyName » doit être remplacé par le nom de la propriété que vous modifiez dans l’élément ; et varNewProp doivent être remplacés par un VARIANT qui contient la nouvelle valeur de la propriété.


```C++
// Convert ItemName to a BSTR.
bstrItemName = SysAllocString(L"ItemName");
HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
  CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
  (void**)&pCatalog); 
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pCatalog->GetCollection(L"TopCollection", 
  (IDispatch**)&pTopColl);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Populate the TopCollection collection.
hr = pTopColl->Populate();
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Get the number of items in the collection.
hr = pTopColl->get_Count(&lCount);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
VARIANT varName;
VariantInit(&varName);
// Iterate through each item in the collection.
for (LONG lIdx = 0; lIdx < lCount; lIdx++) {
    hr = pTopColl->get_Item(lIdx, (IDispatch**)&pItem);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    hr = pItem->get_Name(&varName);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    // Compare the item name to bstrItemName.
    hr = VarBstrCmp(varName.bstrVal, bstrItemName, 1024L, NULL);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    if (VARCMP_EQ == hr) {  // The strings are equal.
        // Use the put_Value method to modify properties of the item.
        hr = pItem->put_Value(L"PropertyName", varNewProp);
        if (FAILED(hr)) exit(0);  // Replace with specific error handling.
        break;  // Exit the iteration.
    }
}
hr = pTopColl->SaveChanges(&lNum);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
SysFreeString(bstrItemName);


```



pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types d’administration COM+. Un objet COMAdminCatalogCollection peut être créé en appelant [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) sur un objet [**COMAdminCatalog**](comadmincatalog.md) ou [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

Appelez la méthode [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) pour remplir la collection avec tous ses éléments. Itérez au sein de chacun des éléments de la collection. Lorsque vous trouvez l’élément qui vous intéresse, vous pouvez modifier les propriétés de l’élément et quitter l’itération. Si vous apportez des modifications à des éléments d’une collection, vous devez appeler la méthode [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) de l’objet **COMAdminCatalogCollection** pour enregistrer les modifications apportées au catalogue com+.

Cela est illustré dans l’exemple suivant, où « la collection de la collection » doit être remplacée par le nom de l’une des collections d’administration COM+ de niveau supérieur ; « ItemName » doit être remplacé par le nom de l’élément qui vous intéresse ; « PropertyName » doit être remplacé par le nom de la propriété que vous modifiez dans l’élément ; et NewPropValue doivent être remplacés par la nouvelle valeur de la propriété.


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")
objTopCollection.Populate
Dim objItem As COMAdmin.COMAdminCatalogObject
For Each objItem in objTopCollection
    If objItem.Name = "ItemName" Then
        objItem.Value("PropertyName") = NewPropValue
        Exit For
    End If
Next
objAppCollection.SaveChanges

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

[**COMAdminCatalogCollection**](comadmincatalogcollection.md)
</dt> <dt>

[**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




