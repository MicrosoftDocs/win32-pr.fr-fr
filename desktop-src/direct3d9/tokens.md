---
description: Les jetons sont écrits sous la forme de mots de poids faible (Little endian). La liste suivante de valeurs de jeton est divisée en jetons d’enregistrement et en jetons autonomes.
ms.assetid: vs|directx_sdk|~\tokens.htm
title: Jetons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df253327b1256ea5e04f8b80b7e1da89f13e32c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918219"
---
# <a name="tokens"></a>Jetons

Les jetons sont écrits sous la forme de mots de poids faible (Little endian). La liste suivante de valeurs de jeton est divisée en jetons d’enregistrement et en jetons autonomes.

Les jetons d’enregistrement sont définis comme suit.


```
#define TOKEN_NAME         1
#define TOKEN_STRING       2
#define TOKEN_INTEGER      3
#define TOKEN_GUID         5
#define TOKEN_INTEGER_LIST 6
#define TOKEN_FLOAT_LIST   7
```



Les jetons autonomes sont définis comme suit.


```
#define TOKEN_OBRACE      10
#define TOKEN_CBRACE      11
#define TOKEN_OPAREN      12
#define TOKEN_CPAREN      13
#define TOKEN_OBRACKET    14
#define TOKEN_CBRACKET    15
#define TOKEN_OANGLE      16
#define TOKEN_CANGLE      17
#define TOKEN_DOT         18
#define TOKEN_COMMA       19
#define TOKEN_SEMICOLON   20
#define TOKEN_TEMPLATE    31
#define TOKEN_WORD        40
#define TOKEN_DWORD       41
#define TOKEN_FLOAT       42
#define TOKEN_DOUBLE      43
#define TOKEN_CHAR        44
#define TOKEN_UCHAR       45
#define TOKEN_SWORD       46
#define TOKEN_SDWORD      47
#define TOKEN_VOID        48
#define TOKEN_LPSTR       49
#define TOKEN_UNICODE     50
#define TOKEN_CSTRING     51
#define TOKEN_ARRAY       52
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Encodage Binaire](binary-encoding.md)
</dt> </dl>

 

 



