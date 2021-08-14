---
title: usesgetlasterror (attribut)
description: L’attribut \ usesgetlasterror \ signale à l’appelant qu’il peut appeler GetLastError pour récupérer le code d’erreur.
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- MIDL de l’attribut usesgetlasterror
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239486792eb218d51c305f9955331e90c6c165586153dab167f2e19d3a0324e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641034"
---
# <a name="usesgetlasterror-attribute"></a>usesgetlasterror (attribut)

L’attribut **\[ \] usesgetlasterror** signale à l’appelant qu’il peut appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour récupérer le code d’erreur.

``` syntax
[
    module-attributes
]
module module-name
{
    [entry(entry-id), usesgetlasterror [, other-attributes]] return-type function-name(param-list);
};
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*module-attributs* 
</dt> <dd>

Zéro, un ou plusieurs attributs MIDL qui seront appliqués au [**module**](module.md).

</dd> <dt>

*nom du module* 
</dt> <dd>

Nom de l’identificateur du [**module**](module.md).

</dd> <dt>

*ID d’entrée* 
</dt> <dd>

Spécifie le point d’entrée de module (nom de fonction ou numéro d’identification d’entier).

</dd> <dt>

*autres attributs* 
</dt> <dd>

Zéro, un ou plusieurs attributs MIDL qui seront appliqués à la procédure distante.

</dd> <dt>

*type de retour* 
</dt> <dd>

Type des données retournées par la procédure distante à la fin de l’opération.

</dd> <dt>

*function-name* 
</dt> <dd>

Nom de la procédure distante tel que défini dans le fichier IDL.

</dd> <dt>

*Param-liste* 
</dt> <dd>

Zéro, un ou plusieurs paramètres à la procédure distante.

</dd> </dl>

## <a name="remarks"></a>Remarques

l’attribut **\[ \] usesgetlasterror** peut être défini sur un point d’entrée de module, si ce point d’entrée utilise la fonction Windows [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) pour retourner des codes d’erreur. L’attribut indique à l’appelant que, en cas d’erreur lors de l’appel de cette fonction, l’appelant peut ensuite appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour récupérer le code d’erreur.

## <a name="examples"></a>Exemples

``` syntax
[
    dllname("MyOwn.dll")
] 
module MyModule
{
    [entry("One"), usesgetlasterror, bindable, requestedit,
     propputref, defaultbind] HRESULT Func1(
         [in]IUnknown * iParam1, 
         [out] long * Param2) ;
    [entry("TwentyOne"), usesgetlasterror, 
     hidden, vararg] SAFEARRAY (int) Func2(
         [in, out] SAFEARRAY (variant) *varP) ;

    // Other module definition statements.
};
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 