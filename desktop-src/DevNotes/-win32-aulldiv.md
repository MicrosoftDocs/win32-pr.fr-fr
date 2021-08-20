---
title: Routine de _aulldiv
description: Divise deux entiers ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _aulldiv, ntoskrnl.exe!_aulldiv
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _aulldiv
targetos: Windows
ms.openlocfilehash: 0a37dd5a88d668ed92d79f7bc939119068840741a54cfacb5a15119fcefb774e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538899"
---
# <a name="_aulldiv-routine"></a>\_Routine aulldiv

Divise deux entiers **ULONGLONG** .
Par exemple, pour diviser deux valeurs UInt64, le compilateur peut générer un appel à la routine **\_ aulldiv** .

## <a name="remarks"></a>Remarques

La routine **\_ aulldiv** est une routine d’assistance pour le compilateur C.
Le fait que le compilateur utilise **\_ aulldiv** dépend entièrement du jeu d’optimisation.

Cette fonction est utilisée uniquement sur les plateformes x86.
