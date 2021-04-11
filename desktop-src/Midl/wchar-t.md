---
title: attribut wchar_t
description: Le \_ mot clé WCHAR t désigne un type à caractères larges.
ms.assetid: e21b2587-909a-4e2b-8c6d-6cc570bf509f
keywords:
- wchar_t MIDL de l’attribut
topic_type:
- apiref
api_name:
- wchar_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0be9af276a8f87fe5ee7a4dfeb499b864de92f4
ms.sourcegitcommit: 686cb805bed0e89573fc68d145809f50c6b0e6d5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2020
ms.locfileid: "104030896"
---
# <a name="wchar_t-attribute"></a>WCHAR \_ t (attribut)

Le mot clé **WCHAR \_ t** désigne un type à caractères larges.

``` syntax
wchar_t identifier-name;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*identificateur-nom* 
</dt> <dd>

Spécifie un identificateur MIDL valide. Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.

</dd> </dl>

## <a name="remarks"></a>Notes

Le type de **WCHAR \_ t** est défini par MIDL comme un objet de données [**short**](short.md) (16 bits) [**non signé**](unsigned.md) .

Le compilateur MIDL permet la redéfinition de **WCHAR \_ t**, mais uniquement s’il est cohérent avec la définition précédente.

Le type à caractères larges est l’un des types prédéfinis de MIDL. Le type à caractères larges peut apparaître comme un spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type de retour de fonction et en tant que spécificateur de type de paramètre). Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).

L’attribut de **\[ chaîne \]** peut être appliqué à un pointeur ou à un tableau de type **WCHAR \_ t**.

Utilisez le caractère **l** avant un caractère ou une constante de chaîne pour désigner la constante de type à caractères larges.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**non signé**](unsigned.md)
</dt> </dl>

 

 




