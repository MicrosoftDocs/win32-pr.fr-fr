---
description: La méthode SelectDefaultSubpictureLanguage définit la langue de sous-image par défaut actuelle dans l’objet MSWebDVD.
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: Méthode SelectDefaultSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d7dd4d66ae9d0580bf863ede9fff1e51d373e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746245"
---
# <a name="selectdefaultsubpicturelanguage-method"></a>Méthode SelectDefaultSubpictureLanguage

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `SelectDefaultSubpictureLanguage` méthode définit la langue de sous-image par défaut actuelle dans l’objet **mswebdvd** .

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*
</dt> <dd>

Spécifie la langue sous la forme d’un entier.

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*
</dt> <dd>

Spécifie l’extension de langage de sous-image sous la forme d’un entier.



| Valeur | Description                    |
|-------|--------------------------------|
| 0     | Extension non spécifiée        |
| 1     | Légendes normales                |
| 2     | Grandes légendes                   |
| 3     | Légendes des enfants            |
| 5     | Sous-titres normaux         |
| 6     | Légendes volumineuses fermées            |
| 7     | Sous-titres des enfants fermés     |
| 9     | Forcé                         |
| 13    | Commentaires du directeur normal     |
| 14    | Commentaires du grand directeur        |
| 15    | Commentaires Director’s des enfants |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

L’extension du langage de sous-image fournit des informations supplémentaires sur la sous-image.

 

 



