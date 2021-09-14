---
title: uuid (attribut)
description: L’attribut \ UUID \ interface désigne un identificateur universel unique (UUID) qui est affecté à l’interface et qui la distingue des autres interfaces.
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- UUID, attribut MIDL
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5688bafe8343bdc1ab508a4e65984cc15c88b124
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093078"
---
# <a name="uuid-attribute"></a>uuid (attribut)

L’attribut d’interface **\[ UUID \]** désigne un identificateur universel unique (UUID) qui est affecté à l’interface et qui la distingue des autres interfaces.

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*chaîne-UUID* 
</dt> <dd>

Spécifie une chaîne composée de 8 chiffres hexadécimaux suivis d’un trait d’Union, puis trois groupes de 4 chiffres hexadécimaux chacun suivi d’un trait d’Union, puis 12 chiffres hexadécimaux. Vous pouvez placer la chaîne UUID entre guillemets, sauf si vous utilisez le commutateur de compilateur MIDL [**/OSF**](-osf.md).

</dd> </dl>

## <a name="remarks"></a>Notes

La bibliothèque Runtime utilise l’UUID de l’interface que l’attribut **\[ UUID \]** désigne pour aider à établir la communication entre les applications client et serveur. L’attribut **\[ UUID \]** peut apparaître dans la liste des attributs de l’interface pour une interface RPC ou une interface com.

Pour une interface RPC, la liste des attributs d’interface doit inclure l’attribut **\[ UUID \]** ou l' **\[** [](local.md) **\]** attribut local, et celle que vous choisissez doit se produire exactement une fois. Si la liste inclut l’attribut **\[ UUID \]** , elle peut également inclure l' **\[** attribut [**version**](version.md) **\]** .

Pour une interface COM (identifiée par l’attribut interface de l' **\[** [**objet**](object.md) **\]** ), la liste des attributs de l’interface doit inclure l’attribut **\[ UUID \]** , mais elle ne peut pas inclure l’attribut **\[ version \]** . La liste d’une interface COM peut inclure l’attribut **\[ local \]** même si l’attribut **\[ UUID \]** est présent.

Microsoft RPC prend en charge une extension de l’IDL DCE qui autorise l’UUID à être placé entre guillemets doubles ("" "). La forme entre guillemets est nécessaire pour les préprocesseurs de compilateur C qui interprètent les valeurs UUID comme des nombres à virgule flottante.

Toutes les valeurs UUID doivent être générées par ordinateur pour garantir l’unicité. Utilisez l’utilitaire uuidgen pour générer des valeurs UUID uniques.

L’UUID et les numéros de version de l’interface sont utilisés pour déterminer si le client peut effectuer une liaison avec le serveur. Pour que le client se lie au serveur, l’UUID spécifié dans les interfaces client et serveur doit être identique.

Notez qu’une interface sans attributs peut être importée dans un fichier IDL de base. Toutefois, l’interface ne doit contenir que des types de données sans procédures. Si même une procédure est contenue dans l’interface, un attribut local ou UUID doit être spécifié.

## <a name="examples"></a>Exemples

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**localisé**](local.md)
</dt> <dt>

[**object**](object.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 




