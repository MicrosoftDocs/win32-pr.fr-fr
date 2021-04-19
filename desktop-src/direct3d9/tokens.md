---
description: Les jetons sont écrits sous la forme de mots de poids faible (Little endian). La liste suivante de valeurs de jeton est divisée en jetons d’enregistrement et en jetons autonomes.
ms.assetid: vs|directx_sdk|~\tokens.htm
title: Jetons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df253327b1256ea5e04f8b80b7e1da89f13e32c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515332"
---
# <a name="tokens"></a><span data-ttu-id="a06b3-104">Jetons</span><span class="sxs-lookup"><span data-stu-id="a06b3-104">Tokens</span></span>

<span data-ttu-id="a06b3-105">Les jetons sont écrits sous la forme de mots de poids faible (Little endian).</span><span class="sxs-lookup"><span data-stu-id="a06b3-105">Tokens are written as little-endian WORDs.</span></span> <span data-ttu-id="a06b3-106">La liste suivante de valeurs de jeton est divisée en jetons d’enregistrement et en jetons autonomes.</span><span class="sxs-lookup"><span data-stu-id="a06b3-106">The following list of token values is divided into record-bearing and stand-alone tokens.</span></span>

<span data-ttu-id="a06b3-107">Les jetons d’enregistrement sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="a06b3-107">The record-bearing tokens are defined as follows.</span></span>


```
#define TOKEN_NAME         1
#define TOKEN_STRING       2
#define TOKEN_INTEGER      3
#define TOKEN_GUID         5
#define TOKEN_INTEGER_LIST 6
#define TOKEN_FLOAT_LIST   7
```



<span data-ttu-id="a06b3-108">Les jetons autonomes sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="a06b3-108">The stand-alone tokens are defined as follows.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a06b3-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a06b3-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a06b3-110">Encodage Binaire</span><span class="sxs-lookup"><span data-stu-id="a06b3-110">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 



