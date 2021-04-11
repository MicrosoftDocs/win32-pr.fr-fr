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
ms.openlocfilehash: a82a4d56ecb657e19b9849d10c9b51521af6c262
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2020
ms.locfileid: "104030717"
---
# <a name="_allmul-routine"></a>\_Routine allmul

Multiplie deux entiers **LongLong** ou **ULONGLONG** .
Par exemple, pour multiplier deux valeurs Int64, le compilateur peut générer un appel à la routine **\_ allmul** .

## <a name="remarks"></a>Notes

La routine **\_ allmul** est une routine d’assistance pour le compilateur C.
Le fait que le compilateur utilise **\_ allmul** dépend entièrement du jeu d’optimisation.

Cette routine est utilisée uniquement sur les plateformes x86.
