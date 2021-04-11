---
description: Un objet de données a la définition de syntaxe suivante.
ms.assetid: e636c2eb-3c11-45bf-ab0b-a14ec878742c
title: Données (format de fichier X)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efdf799b9f7f155c8d2a0e883c8d5e79f8091156
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108411"
---
# <a name="data-x-file-format-binary-encoding"></a>Données (format de fichier X, encodage binaire)

Un objet de données a la définition de syntaxe suivante.


```
object                : identifier optional_name TOKEN_OBRACE
                            optional_class_id
                            data_parts_list
                            TOKEN_CBRACE

data_parts_list       : data_part
                      | data_parts_list data_part

data_part             : data_reference
                      | object
                      | number_list
                      | float_list
                      | string_list

number_list           : TOKEN_INTEGER_LIST

float_list            : TOKEN_FLOAT_LIST

string_list           : string_list_1 list_separator

string_list_1         : string
                      | string_list_1 list_separator string

list_separator        : comma
                      | semicolon

string                : token_string

identifier            : name
                      | primitive_type

data_reference        : TOKEN_OBRACE name optional_class_id TOKEN_CBRACE
```



Notez que dans la \_ liste des nombres et les \_ données de liste flottante dans les fichiers binaires, les \_ virgules et les \_ points-virgules de jeton ne sont pas utilisés. Les virgules et les points-virgules sont utilisés dans les données de liste de chaînes \_ . Notez également que vous pouvez uniquement utiliser la \_ référence de données pour les membres de données facultatifs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Encodage Binaire](binary-encoding.md)
</dt> </dl>

 

 



