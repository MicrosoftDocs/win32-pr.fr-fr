---
title: Nouveaux types de données
description: Trois classes de types de données ont été introduites pour les types de données de précision fixe Windows de 64 bits, les types de précision de pointeurs et les types spécifiques-pointeurs de précision.
ms.assetid: 016977d4-e7bf-463e-9755-7ef13f16e9e5
keywords:
- Guide de programmation Windows 64 bits-programmation Windows 64 bits, types de données
- types de données programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cf5960b5344da1d459d12dee96a2f67f2cfbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316217"
---
# <a name="the-new-data-types"></a>Nouveaux types de données

Trois classes de types de données ont été introduites pour Windows 64 bits : types de données à précision fixe, types de précision de pointeurs et types spécifiques-pointeurs-précision. Ces types ont été ajoutés à l’environnement de développement pour permettre aux développeurs de se préparer pour Windows 64 bits. Ces types sont dérivés de l’entier de base du langage C et des types longs. Par conséquent, vous pouvez utiliser ces types de données dans le code que vous compilez et testez sur Windows 32 bits, puis recompilez avec le compilateur 64 bits lors du ciblage de Windows 64 bits.

Même pour les applications qui ciblent uniquement Windows 32 bits, l’adoption de ces nouveaux types de données rend votre code plus robuste. Pour utiliser ces types de données, vous devez analyser votre code pour déterminer si l’utilisation du pointeur, le polymorphisme et les définitions de données peuvent être potentiellement dangereuses. Par exemple, lorsqu’une variable est de type **ULong \_ ptr**, il est clair qu’elle sera utilisée pour le cast des pointeurs pour les opérations arithmétiques ou le polymorphisme. Il n’est pas possible d’indiquer une telle utilisation directement à l’aide des types de données plus anciens. (Vous pouvez effectuer cette opération indirectement en utilisant le nommage de type dérivé ou la notation hongroise, mais les deux techniques sont sujettes aux erreurs.)

Tous ces types de données sont déclarés dans BaseTsd. h. Pour plus d’informations, notamment sur les définitions de ces types de données, consultez [types de données Windows](/windows/desktop/WinProg/windows-data-types).

## <a name="fixed-precision"></a>Précision fixe

Les types de données à précision fixe sont de la même longueur dans les fenêtres 32 et 64 bits. Pour vous aider à vous souvenir de cela, leur précision fait partie du nom du type de données. Voici les types de données à précision fixe.



| Terme                                                                       | Description                        |
|----------------------------------------------------------------------------|------------------------------------|
| <span id="DWORD32"></span><span id="dword32"></span>**DWORD32**<br/> | Entier non signé 32 bits<br/> |
| <span id="DWORD64"></span><span id="dword64"></span>**DWORD64**<br/> | Entier non signé 64 bits<br/> |
| <span id="INT32"></span><span id="int32"></span>**ENTIER**<br/>       | Entier 32 bits signé<br/>   |
| <span id="INT64"></span><span id="int64"></span>**INT64**<br/>       | Entier 64 bits signé<br/>   |
| <span id="LONG32"></span><span id="long32"></span>**LONG32**<br/>    | Entier 32 bits signé<br/>   |
| <span id="LONG64"></span><span id="long64"></span>**LONG64**<br/>    | Entier 64 bits signé<br/>   |
| <span id="UINT32"></span><span id="uint32"></span>**UINT32**<br/>    | Unsigned **Int32**<br/>      |
| <span id="UINT64"></span><span id="uint64"></span>**UINT64**<br/>    | Unsigned **Int64**<br/>      |
| <span id="ULONG32"></span><span id="ulong32"></span>**ULONG32**<br/> | Unsigned **LONG32**<br/>     |
| <span id="ULONG64"></span><span id="ulong64"></span>**ULONG64**<br/> | Unsigned **LONG64**<br/>     |



 

## <a name="pointer-precision"></a>Précision du pointeur

Comme la précision du pointeur change (c’est-à-dire qu’elle devient 32 bits sur Windows 32 bits et 64 bits avec Windows 64 bits), les types de données de précision du pointeur reflètent la précision en conséquence. Par conséquent, il est possible d’effectuer un cast d’un pointeur vers l’un de ces types en toute sécurité lors de l’exécution de l’arithmétique de pointeur. Si la précision du pointeur est de 64 bits, le type est 64 bits. Les types de nombre reflètent également la taille maximale à laquelle un pointeur peut faire référence. Voici les types de pointeurs de précision et de nombre.



| Terme                                                                              | Description                                                                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="DWORD_PTR"></span><span id="dword_ptr"></span>**\_ptr DWORD**<br/> | Type long non signé pour la précision du pointeur.<br/>                                                                             |
| <span id="HALF_PTR"></span><span id="half_ptr"></span>**DEMI- \_ ptr**<br/>    | La moitié de la taille d’un pointeur. Utilisez dans une structure qui contient un pointeur et deux petits champs.<br/>                      |
| <span id="INT_PTR"></span><span id="int_ptr"></span>**\_pointeur int**<br/>       | Type entier signé pour la précision du pointeur.<br/>                                                                            |
| <span id="LONG_PTR"></span><span id="long_ptr"></span>**\_ptr long**<br/>    | Type long signé pour la précision du pointeur.<br/>                                                                               |
| <span id="SIZE_T"></span><span id="size_t"></span>**TAILLE \_ T**<br/>          | Nombre maximal d’octets auxquels un pointeur peut faire référence. Utilisez pour un nombre qui doit s’étendre à la plage complète d’un pointeur.<br/> |
| <span id="SSIZE_T"></span><span id="ssize_t"></span>**SSIZE \_ T**<br/>       | **Taille signée \_ T**.<br/>                                                                                                   |
| <span id="UHALF_PTR"></span><span id="uhalf_ptr"></span>**UHALF \_ ptr**<br/> | **Demi- \_ ptr** non signé.<br/>                                                                                               |
| <span id="UINT_PTR"></span><span id="uint_ptr"></span>**UINT \_ ptr**<br/>    | Unsigned **int \_ ptr**.<br/>                                                                                                |
| <span id="ULONG_PTR"></span><span id="ulong_ptr"></span>**ULONG ( \_ PTR)**<br/> | **\_ Ptr long** non signé.<br/>                                                                                               |



 

## <a name="specific-pointer-precision-types"></a>Types de Pointer-Precision spécifiques

Les nouveaux types de pointeurs suivants redimensionnent explicitement le pointeur. Soyez prudent lorsque vous utilisez des pointeurs dans du code 64 bits : Si vous déclarez le pointeur à l’aide d’un type 32 bits, le système d’exploitation crée le pointeur en tronquant un pointeur 64 bits. (Tous les pointeurs sont 64 bits sur Windows 64 bits.)



| Terme                                                                                 | Description                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="POINTER_32"></span><span id="pointer_32"></span>**POINTEUR \_ 32**<br/> | Pointeur 32 bits. Sur Windows 32 bits, il s’agit d’un pointeur natif. Sur Windows 64 bits, il s’agit d’un pointeur 64 bits tronqué.<br/>                                                                                       |
| <span id="POINTER_64"></span><span id="pointer_64"></span>**POINTEUR \_ 64**<br/> | Pointeur 64 bits. Sur Windows 64 bits, il s’agit d’un pointeur natif. Sur Windows 32 bits, il s’agit d’un pointeur 32 bits étendu au niveau du signe. <br/> Notez qu’il n’est pas possible de supposer l’état du bit de pointeur le plus élevé.<br/> |



 

 

