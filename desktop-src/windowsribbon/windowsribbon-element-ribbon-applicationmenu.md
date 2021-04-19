---
title: Propriété Ribbon. ApplicationMenu
description: Représente le menu de l’application. | Propriété Ribbon. ApplicationMenu
ms.assetid: 6945e976-8ac8-40fa-8e71-31812871b496
keywords:
- Ruban de la propriété Ribbon. ApplicationMenu
topic_type:
- apiref
api_name:
- Ribbon.ApplicationMenu
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71263a19057d3f66747b1a40aaa2d0a46528e9b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531303"
---
# <a name="ribbonapplicationmenu-property"></a>Propriété Ribbon. ApplicationMenu

Représente le menu de l’application.

## <a name="usage"></a>Utilisation

``` syntax
<Ribbon.ApplicationMenu>
  child elements
</Ribbon.ApplicationMenu>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                     | Description                                    |
|-----------------------------------------------------------------------------|------------------------------------------------|
| [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)<br/> | Doit se produire exactement une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                   |
|-----------------------------------------------------------|
| [**Ruban**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Notes

Obligatoire.

Peut se produire au plus une fois pour chaque [**ruban**](windowsribbon-element-ribbon.md).

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour l’élément **Ribbon. ApplicationMenu** .

Cette section de code affiche la déclaration de contrôle **Ribbon. ApplicationMenu** .


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



 

 





