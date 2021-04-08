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
ms.openlocfilehash: b8183b8b91c4a061e6b91c67ab83bca6393751f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841322"
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

## <a name="remarks"></a>Notes

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

 

 




