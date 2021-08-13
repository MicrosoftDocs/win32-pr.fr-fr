---
title: attribut enum
description: Le mot clé enum identifie un type énuméré.
ms.assetid: 1aaa3c36-17f7-42ff-8f4c-66133fcf4a1a
keywords:
- énumération MIDL d’attribut
topic_type:
- apiref
api_name:
- enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1519e6208e8bccae0288d6e0b31d7897faba4e1c9c7add8987f5dd493f4f5f3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384488"
---
# <a name="enum-attribute"></a>attribut enum

Le mot clé **enum** identifie un type énuméré.

``` syntax
enum [tag ] 
{ 
    identifier [=integer-value ] 
    [ , ... ] 
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Référence* 
</dt> <dd>

Spécifie une balise facultative pour le type énuméré.

</dd> <dt>

*identifier* 
</dt> <dd>

Spécifie l’énumération particulière.

</dd> <dt>

*valeur entière* 
</dt> <dd>

Spécifie une valeur entière constante.

</dd> </dl>

## <a name="remarks"></a>Remarques

les types **enum** peuvent apparaître en tant que spécificateurs de type dans les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que fonction-Return-type ou en tant que spécificateur de type paramètre). Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).

Dans le mode par défaut du compilateur MIDL, vous pouvez assigner des valeurs entières à des énumérateurs. (Cette fonctionnalité n’est pas disponible quand vous compilez avec le commutateur [**/OSF**](-osf.md) .) Comme avec les énumérateurs de langage C, les noms d’énumérateur doivent être uniques, mais les valeurs d’énumérateur n’ont pas besoin d’être.

Lorsque les opérateurs d’assignation ne sont pas fournis, les identificateurs sont mappés à des entiers consécutifs de gauche à droite, en commençant par zéro. Lorsque des opérateurs d’assignation sont fournis, les valeurs affectées commencent à partir de la dernière valeur assignée.

Le nombre maximal d’identificateurs est 65 535.

Les objets de type **enum** sont des types [**int**](int.md) et leur taille est dépendante du système. Par défaut, les objets de types **enum** sont traités comme des objets 16 bits de type [**unsigned**](unsigned.md) [**short**](short.md) lorsqu’ils sont transmis sur un réseau. Les valeurs situées en dehors de la plage 0 à 32 767 provoquent la \_ valeur enum X RPC de l’exception Runtime \_ \_ \_ hors \_ \_ limites. Pour transmettre des objets en tant qu’entités 32 bits, appliquez l' **\[** attribut [**\_ enum v1**](v1-enum.md) **\]** au typedef **enum** .

## <a name="examples"></a>Exemples

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**non signé**](unsigned.md)
</dt> <dt>

[**\_enum v1**](v1-enum.md)
</dt> </dl>

 

 




