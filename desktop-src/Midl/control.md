---
title: attribut de contrôle
description: L’attribut \ Control \ identifie une coclasse ou une bibliothèque comme un contrôle COM, à partir duquel un site conteneur dérivera des bibliothèques de types ou des classes d’objets composant supplémentaires.
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- attribut de contrôle MIDL
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6372ffb7f7d9f19769e419b12c0b109736a9867360224e023f1b622c653854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643678"
---
# <a name="control-attribute"></a>attribut de contrôle

L’attribut **\[ Control \]** identifie une [**coclasse**](coclass.md) ou une [**bibliothèque**](library.md) comme un contrôle com, à partir duquel un site conteneur dérivera des bibliothèques de types ou des classes d’objets composant supplémentaires.

``` syntax
[
    uuid, 
    control 
    [, attribute-list]
] 
library | coclass lib-or-coclassname 
{ 
    definitions 
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*liste d’attributs* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la [**bibliothèque**](library.md) ou à l’instruction de [**coclasse**](coclass.md) . Séparez plusieurs attributs par des virgules.

</dd> <dt>

*lib-or-NomCoclasse* 
</dt> <dd>

Spécifie le nom de la [**bibliothèque**](library.md) ou de la [**coclasse**](coclass.md).

</dd> <dt>

*Description* 
</dt> <dd>

Instructions MIDL qui spécifient les membres de la [**bibliothèque**](library.md) ou de la [**coclasse**](coclass.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

Cet attribut vous permet de marquer des bibliothèques de types qui décrivent des contrôles afin qu’elles ne soient pas affichées dans les navigateurs de type destinés aux objets non visuels.

### <a name="flags"></a>Indicateurs

TYPEFLAG \_ FCONTROL, libflag \_ FCONTROL

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("Hello 2.1 COM Control Library"), 
    control,version(2.1)
] 
library Hello 
{ 
    /* library definitions */
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**coclasse**](coclass.md)
</dt> <dt>

[**Bibliothèque**](library.md)
</dt> </dl>

 

 