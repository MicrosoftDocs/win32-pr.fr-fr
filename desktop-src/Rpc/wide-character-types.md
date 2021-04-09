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
# <a name="wide-character-types"></a>Types de Wide-Character

Microsoft RPC prend en charge le type de caractère étendu [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t). Le type à caractères larges utilise 2 octets pour chaque caractère. La définition du langage C ANSI vous permet d’initialiser des caractères longs et des chaînes longues comme suit :

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 