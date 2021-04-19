---
title: attribut local
description: L’attribut \ local \ spécifie au compilateur MIDL qu’une interface ou une fonction n’est pas distante.
ms.assetid: 17ad3d87-4ca4-4e9b-91bc-280c03830f54
keywords:
- MIDL de l’attribut local
topic_type:
- apiref
api_name:
- local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40b1842bf637d3b7fcaab7a0c13319def1d1663
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106513498"
---
# <a name="local-attribute"></a>attribut local

L’attribut **\[ local \]** spécifie au compilateur MIDL qu’une interface ou une fonction n’est pas distante.

``` syntax
[ 
    local 
    [, interface-attribute-list] 
] 
interface interface-name
{
}

[ 
    object, 
    uuid(string-uuid), 
    local [, interface-attribute-list] 
]
interface interface-name
{
}

[ local [, function-attribute-list] ] function-declarator ;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*interface-attribut-List* 
</dt> <dd>

Spécifie d’autres attributs qui s’appliquent à l’ensemble de l’interface. Le point de terminaison des attributs **\[** [](endpoint.md) **\]** , la **\[** [**version**](version.md) **\]** et le **\[** [**pointeur \_ par défaut**](pointer-default.md) **\]** sont facultatifs. Quand vous compilez avec le commutateur de [**\_ configuration/App**](-app-config.md) , il est **\[** également possible de présenter un [**\_ handle implicite**](implicit-handle.md) **\]** ou un **\[** [**\_ handle automatique**](auto-handle.md) **\]** . Séparez plusieurs attributs par des virgules.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom par lequel les composants logiciels peuvent décourber l’interface.

</dd> <dt>

*chaîne-UUID* 
</dt> <dd>

Spécifie une chaîne UUID générée par l’utilitaire uuidgen. Si vous n’utilisez pas le commutateur MIDL du compilateur [**/OSF**](-osf.md), vous pouvez placer la chaîne UUID entre guillemets.

</dd> <dt>

*function-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction. Les attributs de fonction valides sont **\[** [**callback**](callback.md) **\]** ; l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**chaîne**](string.md) **\]** , **\[** [**Ignorer**](ignore.md) **\]** et **\[** [**\_ handle de contexte**](context-handle.md) **\]** . Séparez plusieurs attributs par des virgules.

</dd> <dt>

*déclarateur de fonction* 
</dt> <dd>

Spécifie le spécificateur de type, le nom de fonction et la liste de paramètres pour la fonction.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ local \]** peut être appliqué à des fonctions individuelles ou à l’interface dans son ensemble.

Lorsqu’il est utilisé dans l’en-tête d’interface, l’attribut **\[ local \]** vous permet d’utiliser le compilateur MIDL comme générateur d’en-tête. Le compilateur ne génère pas de stub pour les fonctions et ne garantit pas que l’en-tête peut être transmis.

Pour une interface RPC, l’attribut **\[ local \]** ne peut pas être utilisé en même temps que l' **\[** attribut [**UUID**](uuid.md) **\]** . **\[ UUID \]** ou **\[ local \]** doit être présent dans l’en-tête d’interface, et celui que vous choisissez doit se produire exactement une fois.

Pour une interface COM (identifiée par l’attribut interface de l' **\[** [**objet**](object.md) **\]** ), la liste des attributs de l’interface peut inclure l’attribut **\[ \] local** même si l' **\[** attribut [**UUID**](uuid.md) **\]** est présent.

Lorsqu’il est utilisé dans une fonction individuelle, l’attribut **\[ local \]** désigne une procédure locale pour laquelle aucun stub n’est généré. L’utilisation de l’attribut **\[ local \]** en tant qu’attribut de fonction est une extension Microsoft de l’IDL DCE. Par conséquent, cet attribut n’est pas disponible quand vous compilez à l’aide du commutateur MIDL [**/OSF**](-osf.md) .

Notez qu’une interface sans attributs peut être importée dans un fichier IDL de base. Toutefois, l’interface ne doit contenir que des types de données sans procédures. Si même une procédure est contenue dans l’interface, un attribut local ou UUID doit être spécifié.

## <a name="examples"></a>Exemples

``` syntax
/* IDL file #1 */ 
[
    local
] 
interface local_procs 
{ 
    void MyLocalProc(void);
} 
 
/* IDL file #2 */ 
[
    object, 
    uuid(12345678-1234-1234-123456789ABC), 
    local
] 
interface local_object_procs : IUnknown
{ 
    void MyLocalObjectProc(void);
} 
 
/* IDL file #3 */ 
[
    uuid(87654321-1234-1234-123456789ABC)
] 
interface mixed_procs 
{ 
    [local] void MyLocalProc(void); 
    HRESULT MyRemoteProc([in] short sParam); 
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**configuration de/App \_**](-app-config.md)
</dt> <dt>

[**\_handle automatique**](auto-handle.md)
</dt> <dt>

[**rappel**](callback.md)
</dt> <dt>

[**handle de contexte \_**](context-handle.md)
</dt> <dt>

[**poste**](endpoint.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**tenir**](ignore.md)
</dt> <dt>

[**handle implicite \_**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**object**](object.md)
</dt> <dt>

[**pointeur \_ par défaut**](pointer-default.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**chaîne**](string.md)
</dt> <dt>

[**unique**](unique.md)
</dt> <dt>

[**universel**](uuid.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 




