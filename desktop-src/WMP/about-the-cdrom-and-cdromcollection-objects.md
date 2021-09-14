---
title: À propos des objets cdrom et CdromCollection
description: À propos des objets cdrom et CdromCollection
ms.assetid: b764806b-d9e1-4c36-b86b-24613501c926
keywords:
- Lecteur Windows Media, objet Cdrom
- Lecteur Windows Media modèle objet, objet Cdrom
- modèle objet, objet cdrom
- Lecteur Windows Media ActiveX contrôle, objet Cdrom
- contrôle ActiveX, objet Cdrom
- Lecteur Windows Media contrôle Mobile ActiveX, objet Cdrom
- Lecteur Windows Media Mobile, objet cdrom
- Objet cdrom
- Lecteur Windows Media, objet CdromCollection
- Lecteur Windows Media modèle objet, objet CdromCollection
- modèle objet, objet CdromCollection
- Lecteur Windows Media ActiveX contrôle, objet CdromCollection
- contrôle ActiveX, objet CdromCollection
- Lecteur Windows Media contrôle Mobile ActiveX, objet CdromCollection
- Lecteur Windows Media Mobile, objet CdromCollection
- Objet CdromCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8fca9f7097f67226e31173670ca2935969704a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232943"
---
# <a name="about-the-cdrom-and-cdromcollection-objects"></a>À propos des objets cdrom et CdromCollection

Les objets **cdrom** et **CdromCollection** régissent l’interface des lecteurs de CD sur votre ordinateur pour la lecture et la lecture de CD.

L’objet **CdromCollection** est accessible uniquement par le biais de la propriété **CdromCollection** de l’objet **Player** . La propriété **cdromCollection** retourne l’objet **cdromCollection** . Vous pouvez uniquement accéder aux propriétés de l’objet **CdromCollection** après l’avoir créé. Par exemple, pour utiliser la propriété **Count** , vous devez utiliser le code suivant :


```C++
mycount = player.cdromcollection.count;
```



Vous pouvez accéder à l’objet **cdrom** uniquement par le biais de l’objet **CdromCollection** . Par exemple, pour éjecter le CD à l’aide de la méthode **EJECT** , vous devez d’abord créer l’objet collection, puis un élément dans l’objet. Pour éjecter le CD, utilisez le code suivant :


```C++
player.cdromcollection.item(0).eject();
```



Dans les deux cas, vous créez d’abord l’objet de collection (**CdromCollection**), puis vous obtenez un objet spécifique de cette collection. L’objet est le premier élément de la collection, **Item**(0), qui correspond au premier lecteur de CD. Vous appelez ensuite une méthode, **éjecter**, sur cet élément.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objet cdrom**](cdrom-object.md)
</dt> <dt>

[**Objet CdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Modèle objet de lecteur pour les langages de script**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




