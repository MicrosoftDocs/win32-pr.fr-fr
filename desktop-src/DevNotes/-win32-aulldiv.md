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
ms.openlocfilehash: 2fce346ee9608f20667c76841a63a8a3fb9cfe21
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2020
ms.locfileid: "104462687"
---
# <a name="_aulldiv-routine"></a>\_Routine aulldiv

Divise deux entiers **ULONGLONG** .
Par exemple, pour diviser deux valeurs UInt64, le compilateur peut générer un appel à la routine **\_ aulldiv** .

## <a name="remarks"></a>Notes

La routine **\_ aulldiv** est une routine d’assistance pour le compilateur C.
Le fait que le compilateur utilise **\_ aulldiv** dépend entièrement du jeu d’optimisation.

Cette fonction est utilisée uniquement sur les plateformes x86.
