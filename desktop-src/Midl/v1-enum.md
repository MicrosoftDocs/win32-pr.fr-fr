---
title: v1_enum (attribut)
description: L’attribut \ v1 \_ enum \ indique que le type énuméré spécifié doit être transmis en tant qu’entité 32 bits, plutôt que la valeur par défaut 16 bits.
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- v1_enum MIDL de l’attribut
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d7afb814cde879f0ada5124b1a19d8ac8b8c851deafcda7e75295a6e5338f68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382783"
---
# <a name="v1_enum-attribute"></a>\_attribut enum v1

L’attribut **\[ \_ enum \] v1** indique que le type énuméré spécifié doit être transmis en tant qu’entité 32 bits, plutôt que la valeur par défaut 16 bits.

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a>Paramètres

Cet attribut n’a aucun paramètre.

## <a name="remarks"></a>Remarques

L’utilisation de l’attribut **\[ \_ enum \] v1** pour transmettre un type énuméré en tant qu’entité 32 bits augmente l’efficacité du marshaling et du démarshaling des données lorsqu’une telle énumération est incorporée dans les structures ou les unions.

Pour améliorer les performances, nous vous recommandons d’appliquer l’attribut **\[ \_ enum \] v1** aux énumérateurs dans les applications 32 bits. Gardez toutefois à l’esprit que sur les plateformes 16 bits, le compilateur C traite un type énuméré comme un [**entier**](int.md)16 bits. Par conséquent, les applications clientes 16 bits doivent convertir les types [**enum**](enum.md) en [**long**](long.md) pour la transmission à distance afin d’éviter de remplacer les données ou d’envoyer des valeurs incorrectes.

## <a name="examples"></a>Exemples

``` syntax
typedef [v1_enum] enum 
{
    value1, 
    value2, ...
};
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**variables**](enum.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> </dl>

 

 




