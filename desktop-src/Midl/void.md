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
ms.openlocfilehash: 7ad758ba334114e13493e7b082f45f37dc6e68efba16dc3a55f14fa57a772d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382435"
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

## <a name="remarks"></a>Remarques

Le type **de pointeur void \* *_, qui, dans C, décrit un pointeur générique qui peut être casté pour représenter tout type pointeur, est limité en MIDL à son utilisation avec le* mot clé de \[ \_ handle \] de contexte _** .

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

 

 




