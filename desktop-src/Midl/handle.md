---
title: handle (attribut)
description: L’attribut \ handle \ spécifie un défini par l’utilisateur ou \ 0034 ; personnalisé \ 0034 ; type de handle.
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- handle MIDL d’attribut
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4560de53bf3f24238e9ff96e01c74716729749
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842289"
---
# <a name="handle-attribute"></a>handle (attribut)

L' \[ attribut **handle** \] spécifie un type de handle défini par l’utilisateur ou « personnalisé ».

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*TypeName* 
</dt> <dd>

Spécifie le nom du type de handle de liaison défini par l’utilisateur.

</dd> </dl>

## <a name="remarks"></a>Notes

Les handles définis par l’utilisateur permettent aux développeurs de concevoir des handles significatifs pour l’application. Un descripteur défini par l’utilisateur ne peut être défini que dans une déclaration de type, et non dans un déclarateur de fonction.

Un paramètre d’un type défini par l' \[  \] attribut handle est utilisé pour déterminer la liaison de l’appel et est transmis à la procédure appelée.

L’utilisateur doit fournir des routines de liaison et d’annulation de liaison pour la conversion entre les types de handles primitifs et définis par l’utilisateur. À partir d’un handle défini par l’utilisateur de type *TypeName*, l’utilisateur doit fournir les routines *TypeName* \_ **Bind** et *TypeName* \_ **Unbind**. Par exemple, si le type de handle défini par l’utilisateur est nommé MYHANDLE, les routines sont nommées MYHANDLE \_ **Bind** et MYHANDLE \_ **Unbind**.

En cas de réussite, la routine de liaison *TypeName* \_  doit retourner un handle de liaison primitif valide. En cas d’échec, la routine doit retourner une **valeur null**. Si la routine retourne la **valeur null**, la routine *TypeName* \_ **Unbind** ne sera pas appelée. Si la routine de liaison retourne un handle de liaison non valide différent de **null**, le comportement de stub n’est pas défini.

Lorsque la procédure distante a un handle défini par l’utilisateur en tant que paramètre ou qu’un handle implicite, les stubs client appellent la routine de liaison avant d’appeler la procédure distante. Les stubs client appellent la routine d’annulation de liaison après l’appel distant.

Dans un IDL DCE, un paramètre avec l' \[  \] attribut handle doit apparaître comme premier paramètre dans la liste d’arguments de procédure distante. Les paramètres suivants, y compris les autres \[  \] attributs de handle, sont traités comme des paramètres ordinaires. Microsoft prend en charge une extension de l’IDL DCE qui permet d’afficher le paramètre de handle défini par l’utilisateur \[  \] dans des positions autres que le premier paramètre.

## <a name="examples"></a>Exemples

``` syntax
typedef [handle] struct 
{ 
    char machine[8]; 
    char nmpipe[256]; 
} h_service; 
 
handle_t __RPC_USER h_service_bind(h_service); 
void __RPC_USER h_service_unbind(h_service, handle_t);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liaison et Handles](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**handle implicite \_**](implicit-handle.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 