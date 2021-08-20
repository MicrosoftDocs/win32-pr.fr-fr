---
title: attribut const
description: Le mot clé const modifie le type d’une déclaration de type ou le type d’un paramètre de fonction, ce qui empêche la valeur de varier.
ms.assetid: 398fab76-93f3-4d5a-9223-1c57c612b2d7
keywords:
- attribut const, MIDL
topic_type:
- apiref
api_name:
- const
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115f8e5bbb34cff06b75447e863aeae0a6ec61f99064356b0600b261860f8568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991688"
---
# <a name="const-attribute"></a>attribut const

Le mot clé **const** modifie le type d’une déclaration de type ou le type d’un paramètre de fonction, ce qui empêche la valeur de varier.

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*const-type* 
</dt> <dd>

Spécifie un entier MIDL, un caractère, une chaîne ou un type booléen valide. Les types MIDL valides incluent [**Small**](small.md), [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), **\* charÂ* _, [_ *WCHAR \_ t* *](wchar-t.md), **WCHAR \_ t \**_, [_ *Byte* *](byte.md), **byteÂ \** _ et [_*voidÂ \**_](void.md). Les types entier et caractère peuvent être [_ *signés* *](signed.md) ou [**non signés**](unsigned.md).

</dd> <dt>

*identifier* 
</dt> <dd>

Spécifie un identificateur MIDL valide. Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.

</dd> <dt>

*const-expression* 
</dt> <dd>

Spécifie une expression, un identificateur ou une constante numérique ou caractère appropriée pour le type spécifié : littéraux entiers constants ou expressions entières constantes pour les constantes entières ; Expressions booléennes qui peuvent être calculées au moment de la compilation pour les types [**booléens**](boolean.md) ; constantes à caractère unique pour les types [**char**](char-idl.md) ; et constantes de chaîne pour les **\[** [](string.md) **\]** types chaîne. Le type [ * *voidÂ \** _](void.md) peut être initialisé uniquement à _ * null * *.

</dd> <dt>

*type-attribut-List* 
</dt> <dd>

Spécifie un ou plusieurs attributs qui s’appliquent au type.

</dd> <dt>

*type pointeur* 
</dt> <dd>

Spécifie un type de pointeur MIDL valide.

</dd> <dt>

*déclarateur et déclarateur-liste* 
</dt> <dd>

Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers). La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs, séparés par des virgules. L’identificateur de nom de paramètre dans le déclarateur de fonction est facultatif.

</dd> <dt>

*function-attr-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction. Les attributs de fonction valides sont **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**chaîne**](string.md) **\]** , **\[** [**Ignorer**](ignore.md) **\]** et **\[** [**\_ handle de contexte**](context-handle.md) **\]** .

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Spécifie [un \_ type de base](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md), un type [**enum**](enum.md) ou un identificateur de type. Une spécification de stockage facultative peut précéder *le type-specifier*.

</dd> <dt>

*pointeur-decl* 
</dt> <dd>

Spécifie zéro ou plusieurs déclarateurs de pointeur. Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C. Elle est construite à partir de l' **\* *indicateur _, de modificateurs tels que _* Far** et du qualificateur **const**.

</dd> <dt>

*function-name* 
</dt> <dd>

Spécifie le nom de la procédure distante.

</dd> <dt>

*Parameter-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs directionnels, attributs de champ, attributs d’utilisation et attributs de pointeur appropriés pour le type de paramètre spécifié. Séparez plusieurs attributs par des virgules.

</dd> </dl>

## <a name="remarks"></a>Remarques

MIDL vous permet de déclarer des types entier constant, caractère, chaîne et booléen dans le corps de l’interface du fichier IDL. Les déclarations de type **const** sont reproduites dans le fichier d’en-tête généré en tant que directives de **\# définition** .

Les compilateurs IDL DCE ne prennent pas en charge les expressions constantes. Par conséquent, cette fonctionnalité n’est pas disponible lorsque vous utilisez le commutateur [**/OSF**](-osf.md) du compilateur MIDL.

Une constante définie précédemment peut être utilisée comme valeur assignée d’une constante suivante. La valeur d’une expression intégrale constante est automatiquement convertie en type entier respectif conformément aux règles de conversion C.

La valeur d’une constante caractère doit être un caractère ASCII à guillemet simple. Lorsque la constante caractère est le caractère de guillemet simple ('), la barre oblique inverse ( \\ ) doit précéder le caractère de guillemet simple, comme dans \\ '.

La valeur d’une constante de chaîne de caractères doit être une chaîne entre guillemets doubles. Dans une chaîne, la barre oblique inverse ( **\\** ) doit précéder un caractère de guillemet double littéral ( **"** ), comme dans **\\ "**. Dans une chaîne, la barre oblique inverse ( **\\** ) représente un caractère d’échappement. Les constantes de chaîne peuvent comporter jusqu’à 255 caractères.

La valeur **null** est la seule valeur valide pour les constantes de type [ * *voidÂ \** _](void.md). Tous les attributs associés à la déclaration _ *const** sont ignorés.

Le compilateur MIDL ne vérifie pas les erreurs de plage dans l’initialisation **const** . Par exemple, lorsque vous spécifiez « const Short x = 0xFFFFFFFF ; », le compilateur MIDL ne signale pas d’erreur et l’initialiseur est reproduit dans le fichier d’en-tête généré.

## <a name="examples"></a>Exemples

``` syntax
const void *  p1        = NULL; 
const char    my_char1  = 'a'; 
const char    my_char2  = my_char1; 
const wchar_t my_wchar3 = L'a'; 
const wchar_t * pszNote = L"Note"; 
const unsigned short int x = 123; 
 
typedef [string] const char *LPCSTR; 
 
HRESULT GetName([out] wchar_t * const pszName );
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**tableaux**](arrays-1.md)
</dt> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**Boolean**](boolean.md)
</dt> <dt>

[**poids**](byte.md)
</dt> <dt>

[**rappel**](callback.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**handle de contexte \_**](context-handle.md)
</dt> <dt>

[**variables**](enum.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**tenir**](ignore.md)
</dt> <dt>

[**local**](local.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**abonné**](signed.md)
</dt> <dt>

[**Small**](small.md)
</dt> <dt>

[**chaîne**](string.md)
</dt> <dt>

[**modélis**](struct.md)
</dt> <dt>

[**union**](union.md)
</dt> <dt>

[**unique**](unique.md)
</dt> <dt>

[**non signé**](unsigned.md)
</dt> <dt>

[**nullité**](void.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 