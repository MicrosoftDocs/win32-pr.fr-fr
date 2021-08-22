---
description: Appelée par le compilateur lorsque votre fonction contient plusieurs pages de variables locales.
ms.assetid: 154dd992-88b5-44a4-9594-5d13afb71c28
title: Routine de _chkstk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b129b73801c6c18b63b10ac61898ee13a9c5d4f1f0422678bbfe5af82d5b44f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538832"
---
# <a name="_chkstk-routine"></a>\_Routine chkstk

Appelée par le compilateur lorsque votre fonction contient plusieurs pages de variables locales.

## <a name="remarks"></a>Remarques

\_la routine chkstk est une routine d’assistance pour le compilateur C. Pour les compilateurs x86, \_ la routine chkstk est appelée lorsque les variables locales dépassent 4 Ko. pour les compilateurs x64, elle est de 8 Ko.

 

 



