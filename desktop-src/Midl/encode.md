---
title: Encode (attribut)
description: L’attribut \ encode \ ACF spécifie qu’une procédure ou un type de données a besoin de la prise en charge de la sérialisation.
ms.assetid: 2661021d-8a26-4216-935b-ca40b6f8b9ec
keywords:
- code MIDL de l’attribut encode
topic_type:
- apiref
api_name:
- encode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2a35c6d6910229a9e14026f6727db5c3176050
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940871"
---
# <a name="encode-attribute"></a>Encode (attribut)

L’attribut **\[ encode \]** ACF spécifie qu’une procédure ou un type de données a besoin de la prise en charge de la sérialisation.

``` syntax
[ 
    encode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ encode [ , op-attribute-list] ] proc-name

typedef [encode [ , type-attribute-list] ] type-name
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*interface-attribut-List* 
</dt> <dd>

Spécifie d’autres attributs qui s’appliquent à l’ensemble de l’interface.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface.

</dd> <dt>

*définition d’interface* 
</dt> <dd>

Spécifie les instructions IDL qui forment la définition de l’interface.

</dd> <dt>

*op-attribut-List* 
</dt> <dd>

Spécifie d’autres attributs opérationnels qui s’appliquent à la procédure, tels que **\[** [**Decode**](decode.md) **\]** .

</dd> <dt>

*nom de la procédure* 
</dt> <dd>

Spécifie le nom de la procédure.

</dd> <dt>

*type-attribut-List* 
</dt> <dd>

Spécifie d’autres attributs qui s’appliquent au type, par exemple **\[** [**Decode**](decode.md) **\]** et **\[** [**allocate**](allocate.md) **\]** .

</dd> <dt>

*nom du type* 
</dt> <dd>

Spécifie un type défini dans le fichier IDL.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ encode \]** fait en sorte que le compilateur MIDL génère du code qu’une application peut utiliser pour sérialiser des données dans une mémoire tampon. L' **\[** attribut [**Decode**](decode.md) **\]** génère le code pour démarshaler les données d’une mémoire tampon.

Utilisez les attributs **\[ encode \]** et **\[** [**Decode**](decode.md) **\]** dans un CCP pour générer le code de sérialisation des procédures ou des types définis dans le fichier IDL d’une interface. Lorsqu’il est utilisé comme attribut d’interface, **\[ encode \]** s’applique à tous les types et procédures définis dans le fichier IDL. En cas d’utilisation comme attribut opérationnel, **\[ encode \]** s’applique uniquement à la procédure spécifiée. Lorsqu’il est utilisé en tant qu’attribut de type, **\[ encode \]** s’applique uniquement au type spécifié.

Lorsque l’attribut **\[ \] encode** ou **\[** [**Decode**](decode.md) **\]** est appliqué à une procédure, le compilateur MIDL génère un stub de sérialisation de la même façon que les stubs distants pour les routines distantes. Une procédure peut être une procédure distante ou de sérialisation, mais elle ne peut pas être à la fois. Le prototype de la routine générée est envoyé au STUB. Fichier H alors que le stub est placé dans le \_ fichier c. c du stub.

Le compilateur MIDL génère deux fonctions pour chaque type auquel s’applique l’attribut **\[ encode \]** et une fonction supplémentaire pour chaque type auquel **\[** s’applique l’attribut [**Decode**](decode.md) **\]** . Par exemple, pour un type défini par l’utilisateur nommé MyType, le compilateur génère du code pour les \_ fonctions de décodage MyType, MyType \_ et MyType \_ AlignSize. Pour ces fonctions, le compilateur écrit des prototypes dans STUB. H et code source pour STUB \_ C.C.

Pour plus d’informations sur les handles de sérialisation et l’encodage ou le décodage des données, consultez [services de sérialisation](/windows/desktop/Rpc/serialization-services).

## <a name="examples"></a>Exemples

``` syntax
/* 
    ACF file example; 
    Assumes MyType1, MyType2, MyType3, MyProc1, MyProc2, MyProc3 defined 
    in IDL file  
    MyType1, MyType2, MyProc1, MyProc2 have encode and decode 
    serialization support 
    MyType3 and MyProc3 have encode serialization support only 
*/ 
[ 
    encode, 
    implicit_handle(handle_t bh) 
]    
interface regress 
{ 
    typedef [ decode ] MyType1; 
    typedef [ encode, decode ] MyType2; 
    [ decode ] MyProcc1(); 
    [ encode ] MyProc2(); 
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**lui**](allocate.md)
</dt> <dt>

[**décoder**](decode.md)
</dt> </dl>

 

 