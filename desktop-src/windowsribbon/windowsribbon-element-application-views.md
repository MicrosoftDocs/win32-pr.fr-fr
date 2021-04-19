---
title: Application. views, propriété
description: Représente un conteneur pour chaque vue de l’infrastructure du ruban, en particulier le ruban et le ContextPopup.
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- Ruban Windows de la propriété application. views
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e7d106d346a790ee3bd8879b2367f38341f0a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511153"
---
# <a name="applicationviews-property"></a>Application. views, propriété

Représente un conteneur pour chaque vue de l’infrastructure du ruban, en particulier le [**ruban**](windowsribbon-element-ribbon.md) et le [**ContextPopup**](windowsribbon-element-contextpopup.md).

## <a name="usage"></a>Utilisation

``` syntax
<Application.Views>
  child elements
</Application.Views>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                               | Description                                        |
|-----------------------------------------------------------------------|----------------------------------------------------|
| [**ContextPopup**](windowsribbon-element-contextpopup.md)<br/> | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**Ruban**](windowsribbon-element-ribbon.md)<br/>             | Doit se produire exactement une fois<br/> <br/>     |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                             |
|---------------------------------------------------------------------|
| [**Application**](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a>Notes

Obligatoire.

Doit se produire exactement une fois pour chaque élément d' [**application**](windowsribbon-element-application.md) .

## <a name="examples"></a>Exemples

L’exemple suivant montre un élément **application. views** qui contient un manifeste de contrôles de ruban, chacun avec une référence à une commande déclarée dans l’élément [**application. Commands**](windowsribbon-element-application-commands.md) .


```C++
<Application.Views>
  <Ribbon Name="ScenicRibbonSampleApp">
    <Ribbon.Tabs>
```




```C++
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```




```C++
    </Ribbon.Tabs>
  </Ribbon>
</Application.Views>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Application. commandes**](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 





