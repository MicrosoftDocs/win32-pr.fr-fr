---
title: Types de Wide-Character
description: Microsoft RPC prend en charge le type de caractère étendu WCHAR \_ t.
ms.assetid: 1a601461-df34-456d-93e8-4cf0b655cf2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 821d69999a0ec7e175409120f223721defd6cd10
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102029"
---
# <a name="wide-character-types"></a><span data-ttu-id="37de7-103">Types de Wide-Character</span><span class="sxs-lookup"><span data-stu-id="37de7-103">Wide-Character Types</span></span>

<span data-ttu-id="37de7-104">Microsoft RPC prend en charge le type de caractère étendu [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t).</span><span class="sxs-lookup"><span data-stu-id="37de7-104">Microsoft RPC supports the wide-character type [**wchar\_t**](/windows/desktop/Midl/wchar-t).</span></span> <span data-ttu-id="37de7-105">Le type à caractères larges utilise 2 octets pour chaque caractère.</span><span class="sxs-lookup"><span data-stu-id="37de7-105">The wide-character type uses 2 bytes for each character.</span></span> <span data-ttu-id="37de7-106">La définition du langage C ANSI vous permet d’initialiser des caractères longs et des chaînes longues comme suit :</span><span class="sxs-lookup"><span data-stu-id="37de7-106">The ANSI C-language definition allows you to initialize long characters and long strings as:</span></span>

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 