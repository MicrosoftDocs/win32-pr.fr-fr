---
title: attribut de proxy
description: L’attribut \ proxy \ empêche Automation de s’inscrire en tant que gestionnaire proxy/stub pour une interface double.
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- MIDL, attribut de proxy
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37e81cb7f67f87153825db59d921b6ee9ec7df6cd334ed2228896c8dec5f9d5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641418"
---
# <a name="proxy-attribute"></a>attribut de proxy

L’attribut **\[ proxy \]** empêche l’inscription de l’Automation en tant que gestionnaire proxy/stub pour une interface double.

``` syntax
[ 
    proxy, 
    uuid(string-uuid <>)
    [ , interface-attribute-list <>] 
] 
interface interface-name <> : base-interface <>
{
    ...
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*chaîne-UUID* 
</dt> <dd>

Spécifie une chaîne composée de 8 chiffres hexadécimaux suivis d’un trait d’Union, puis trois groupes de 4 chiffres hexadécimaux chacun suivi d’un trait d’Union, puis 12 chiffres hexadécimaux. Vous pouvez placer la chaîne UUID entre guillemets, sauf si vous utilisez le commutateur de compilateur MIDL [**/OSF**](-osf.md).

</dd> <dt>

*interface-attribut-List* 
</dt> <dd>

Spécifie une liste de zéro ou plusieurs attributs IDL qui s’appliquent à l’ensemble de l’interface. Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Nom de l’interface.

</dd> <dt>

*interface de base* 
</dt> <dd>

Spécifie le nom d’une interface à partir de laquelle cette interface dérivée hérite des fonctions membres, des codes d’État et des attributs d’interface. L’interface dérivée n’hérite pas des définitions de type. Pour ce faire, utilisez le mot clé [**Import**](import.md) pour importer le fichier IDL de l’interface de base.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’utilisation \[  \] de l’attribut proxy pour une interface double empêche le TLB de prendre en charge des stubs générés. Si cet attribut est spécifié, le proxy de TypeLib ne doit pas être désinscrit lorsque la TypeLib est désinscrite.

### <a name="flags"></a>Indicateurs

<dl> <dt>

<span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>\_proxy TYPEFLAG
</dt> <dd>

Les interfaces peuvent être marquées avec l' \_ indicateur de proxy TYPEFLAG pour indiquer qu’elles utiliseront une bibliothèque de liens dynamiques proxy/stub. Cet indicateur spécifie que le proxy de TypeLib ne doit pas être désinscrit lorsque la TypeLib est désinscrite.

</dd> </dl>

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Génération d’une bibliothèque de types avec MIDL**](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**double**](dual.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 