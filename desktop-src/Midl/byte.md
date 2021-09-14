---
title: attribut d’octet
description: Le mot clé Byte spécifie un élément de données de 8 bits.
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- MIDL d’attribut d’octet
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 347b1f22f06431c5490d4fdac15cdb22b25da69e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093750"
---
# <a name="byte-attribute"></a>attribut d’octet

Le mot clé **Byte** spécifie un élément de données de 8 bits.

``` syntax
byte identifier-name;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*identificateur-nom* 
</dt> <dd>

Spécifie un identificateur MIDL valide. Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.

</dd> </dl>

## <a name="remarks"></a>Notes

Un élément de données **Byte** ne subit pas de conversion pour la transmission sur le réseau en tant que type [**char**](char-idl.md) .

Le type **Byte** est l’un des types de base du langage IDL (Interface Definition Language). Le type d' **octet** peut apparaître comme un spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type fonction-retour et en tant que spécificateur de type paramètre). Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




