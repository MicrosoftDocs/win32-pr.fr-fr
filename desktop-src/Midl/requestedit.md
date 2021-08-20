---
title: requestedit (attribut)
description: L’attribut \ modification \ indique que la propriété prend en charge la notification OnRequestEdit.
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- MIDL de l’attribut modification
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51a894e5d4a09e7535e10a73e1bd118245e5886e0cdbb23b0f0645e588ab4adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146352"
---
# <a name="requestedit-attribute"></a>requestedit (attribut)

L’attribut **\[ \] modification** indique que la propriété prend en charge la notification **OnRequestEdit** .

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*attributs facultatifs* 
</dt> <dd>

Zéro, un ou plusieurs attributs MIDL.

</dd> <dt>

*type de retour* 
</dt> <dd>

Spécifie le type de retour de la fonction.

</dd> <dt>

*function-name* 
</dt> <dd>

Spécifie le nom de la fonction dans le fichier IDL.

</dd> <dt>

*params* 
</dt> <dd>

Zéro, un ou plusieurs paramètres de fonction.

</dd> </dl>

## <a name="remarks"></a>Remarques

La prise en charge de la notification **OnRequestEdit** signifie qu’avant qu’une modification soit apportée, l’objet envoie au client une demande d’autorisation de modification d’une propriété. Un objet peut prendre en charge la liaison de données mais ne pas avoir cet attribut.

### <a name="flags"></a>Indicateurs

FUNCFLAG \_ FREQUESTEDIT, VARFLAG \_ FREQUESTEDIT

## <a name="examples"></a>Exemples

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 