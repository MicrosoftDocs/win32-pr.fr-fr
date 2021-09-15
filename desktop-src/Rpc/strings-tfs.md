---
title: Chaînes (RPC)
description: Trois types de chaînes et appel de procédure distante (RPC).
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207e20b1c343ded17b5d62db2321bee380463f20
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413496"
---
# <a name="strings-rpc"></a>Chaînes (RPC)

Il existe trois types de chaînes dénotés par les sous-chaînes de fin suivantes dans le caractère de format.



| Type                  | Substring |
|-----------------------|-----------|
| Chaîne de caractères      | CSTRING   |
| Chaîne de caractères larges | WSTRING   |
| Structure de chaîne pouvant être | SSTRING   |



 

### <a name="nonconformant-strings"></a>Chaînes non conformes

Un exemple de chaîne non conforme est une **\[ chaîne \]** sur un tableau de taille fixe.

``` syntax
FC_CSTRING | FC _WSTRING 
FC_PAD 
string_size<2>
```

### <a name="conformant-strings"></a>Chaînes conformes

``` syntax
FC_C_CSTRING | FC_C_WSTRING
FC_PAD 
```

–ou–

``` syntax
FC_C_CSTRING | FC_C_WSTRING 
FC_STRING_SIZED 
conformance_description<> 
```

Le premier format décrit les chaînes courantes, comme un argument de **\[ type \] chaîne** \* . Une chaîne conforme dimensionnée possède la dernière Description.

La description de la conformité \_<> est un descripteur de corrélation et contient 4 ou 6 octets selon que [**/Robust**](/windows/desktop/Midl/-robust) est utilisé ou non.

### <a name="structure-strings"></a>Chaînes de structure

Voici une structure de chaîne pouvant être non conforme :

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

Structure pouvant être convertie en chaîne :

``` syntax
FC_C_SSTRING 
element_size<1>
```

ni

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

Cette dernière Description est destinée à une structure de chaîne pouvant être dimensionnée.

 

 