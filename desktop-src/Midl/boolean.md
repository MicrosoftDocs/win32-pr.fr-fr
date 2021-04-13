---
title: attribut booléen
description: Le mot clé Boolean indique que l’expression ou l’expression constante associée à l’identificateur accepte uniquement les valeurs TRUE et FALSe.
ms.assetid: ed3b00a4-880f-4674-9f6d-8f5faf1eea66
keywords:
- attribut booléen MIDL
topic_type:
- apiref
api_name:
- boolean
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68959cabcef1f439ffb6df30b77aeee7056f4fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380857"
---
# <a name="boolean-attribute"></a>attribut booléen

Le mot clé **Boolean** indique que l’expression ou l’expression constante associée à l’identificateur accepte uniquement les valeurs **true** et **false**.

``` syntax
boolean identifier-name;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*identificateur-nom* 
</dt> <dd>

Spécifie un identificateur MIDL valide. Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.

</dd> </dl>

## <a name="remarks"></a>Notes

Le type **booléen** est l’un des types de base du langage IDL. Le type **booléen** peut apparaître comme un spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type fonction-retour et en tant que spécificateur de type de paramètre). Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).

> [!Note]  
> Le type de base **booléen** n’est pas compatible avec l’attribut [**oleautomation**](oleautomation.md) . Utilisez \_ la variante booléenne dans vos interfaces compatibles Automation.

 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




