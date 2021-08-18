---
title: Types de Wide-Character
description: Microsoft RPC prend en charge le type de caractère étendu WCHAR \_ t.
ms.assetid: 1a601461-df34-456d-93e8-4cf0b655cf2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eff57cf22e4836032acb59e1585da15285f55718b6c5b91733b1955ea85072a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010397"
---
# <a name="wide-character-types"></a>Types de Wide-Character

Microsoft RPC prend en charge le type de caractère étendu [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t). Le type à caractères larges utilise 2 octets pour chaque caractère. La définition du langage C ANSI vous permet d’initialiser des caractères longs et des chaînes longues comme suit :

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 