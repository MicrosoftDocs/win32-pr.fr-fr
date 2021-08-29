---
title: Routine de _allmul
description: Multiplie deux entiers LONGLONG ou ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _allmul, ntoskrnl.exe!_allmul
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _allmul
targetos: Windows
ms.openlocfilehash: 38795bf755574ecf1a21ddcdb3655b14a4751a51fc6eca61118734f42e0bc3e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386859"
---
# <a name="_allmul-routine"></a>\_Routine allmul

Multiplie deux entiers **LongLong** ou **ULONGLONG** .
Par exemple, pour multiplier deux valeurs Int64, le compilateur peut générer un appel à la routine **\_ allmul** .

## <a name="remarks"></a>Remarques

La routine **\_ allmul** est une routine d’assistance pour le compilateur C.
Le fait que le compilateur utilise **\_ allmul** dépend entièrement du jeu d’optimisation.

Cette routine est utilisée uniquement sur les plateformes x86.
