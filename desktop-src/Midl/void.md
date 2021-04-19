---
title: void (attribut)
description: Le type de base void indique une procédure sans argument ou une procédure qui ne retourne pas de valeur de résultat.
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- MIDL d’attribut void
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b14a5ae4a2325f840d8a840cb0a1bc5283bb4a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106510239"
---
# <a name="void-attribute"></a>void (attribut)

Le type de base **void** indique une procédure sans argument ou une procédure qui ne retourne pas de valeur de résultat.

``` syntax
void function-name(parameter-list);

return-type function-name(void);

typedef [context_handle] void * context-handle-type;

return-type function-name(
    [context_handle] void * * context-handle-type
    , ...);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la procédure distante.

</dd> <dt>

*parameter-list* 
</dt> <dd>

Spécifie la liste des paramètres passés à la fonction, ainsi que les types de paramètres et attributs de paramètre associés.

</dd> <dt>

*type de retour* 
</dt> <dd>

Spécifie le nom du type retourné par la fonction.

</dd> <dt>

*Context-handle-type* 
</dt> <dd>

Spécifie le nom du type qui prend l' **\[** attribut de [**\_ handle de contexte**](context-handle.md) **\]** .

</dd> </dl>

## <a name="remarks"></a>Notes

Le type de **pointeur \* void**, qui en C décrit un pointeur générique qui peut être casté pour représenter un type pointeur, est limité en MIDL avec le mot clé de **\[ \_ handle \] de contexte** .

## <a name="examples"></a>Exemples

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**handle de contexte \_**](context-handle.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




