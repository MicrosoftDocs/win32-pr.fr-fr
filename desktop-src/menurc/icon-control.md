---
title: Contrôle ICON
description: Définit un contrôle d’icône. Ce contrôle est une icône affichée dans une boîte de dialogue.
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- Menus de contrôle d’icône et autres ressources
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4fc5191457996aabe4a70fefcf64235b3a9573cf12733f9ca7bff2ece6356e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034287"
---
# <a name="icon-control"></a>Contrôle ICON

Définit un contrôle d’icône. Ce contrôle est une icône affichée dans une boîte de dialogue.

L’instruction de contrôle **Icon** , que vous pouvez utiliser uniquement dans une instruction [**DIALOGEX**](dialogex-resource.md) , définit l’identificateur de ressource d’icône, l’identificateur de contrôle d’icône, la position et les attributs d’un contrôle.

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*financière*
</dt> <dd>

Nom d’une icône (pas un nom de fichier) définie ailleurs dans le fichier de ressources.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Largeur*
</dt> <dd>

Cette valeur est ignorée et doit être définie sur zéro.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*celle*
</dt> <dd>

Cette valeur est ignorée et doit être définie sur zéro.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Style de contrôle. Ce paramètre est facultatif. La seule valeur pouvant être spécifiée est le style **d' \_ icône SS** . Il s’agit du style par défaut, que ce paramètre soit spécifié ou non.

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="examples"></a>Exemples

Cet exemple définit un contrôle Icon dont l’identificateur d’icône est 901 et dont le nom est myicon :

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SITUÉE**](icon-resource.md)
</dt> </dl>

 

 




