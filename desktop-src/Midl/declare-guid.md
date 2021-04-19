---
title: declare_guid, mot clé
description: Le \_ mot clé Declare GUID demande à MIDL d’émettre une variable GUID dans le fichier d’en-tête généré.
keywords:
- declare_guid mot clé MIDL
topic_type:
- apiref
api_name:
- declare_guid
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 495acd64e79544d067ff124a88289219919a7fb6
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "106538248"
---
# <a name="declare_guid-keyword"></a>\_mot clé Declare GUID

Le mot clé **Declare \_ GUID** demande à MIDL d’émettre une variable GUID dans le fichier d’en-tête généré.

``` syntax
declare_guid(variable-name, guid)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*variable-nom* 
</dt> <dd>

Spécifie un nom de variable pour l’identificateur dans le fichier d’en-tête généré.

</dd> <dt>

*guid*
</dt> <dd>

Spécifie le [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) qui s’appliquera au nom de la variable dans le fichier d’en-tête généré.

</dd> </dl>

## <a name="examples"></a>Exemples

``` syntax
declare_guid(SID_Widget, 5144C348-169E-4359-A79D-5482461D9929)  
```

## <a name="remarks"></a>Notes

L’utilisation de équivaut `declare_guid` à l’utilisation de `cpp_quote` pour générer un appel de la `EXTERN_GUID` macro.

L’exemple ci-dessus donne la sortie suivante :

```C
cpp_quote("EXTERN_GUID(SID_Widget, 0x5144c348, 0x169e, 0x4359, 0xa7, 0x9d, 0x54, 0x82, 0x46, 0x1d, 0x99, 0x29);")
```

L' `declare_guid` instruction est fournie à titre de commodité. Elle présente l’avantage d’utiliser la même syntaxe de GUID que l' [ `uuid` attribut](uuid.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**cpp_quote**](cpp-quote.md)
</dt> <dt>

[**uuid (attribut)**](uuid.md)
</dt> <dt>

[**Structure GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)
</dt> </dl>
