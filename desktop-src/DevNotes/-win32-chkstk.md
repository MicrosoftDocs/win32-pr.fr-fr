---
description: Appelée par le compilateur lorsque votre fonction contient plusieurs pages de variables locales.
ms.assetid: 154dd992-88b5-44a4-9594-5d13afb71c28
title: Routine de _chkstk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a58b31836947dfb1816bea72a54f820354c792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950375"
---
# <a name="_chkstk-routine"></a>\_Routine chkstk

Appelée par le compilateur lorsque votre fonction contient plusieurs pages de variables locales.

## <a name="remarks"></a>Notes

\_la routine chkstk est une routine d’assistance pour le compilateur C. Pour les compilateurs x86, \_ la routine chkstk est appelée lorsque les variables locales dépassent 4 Ko. pour les compilateurs x64, elle est de 8 Ko.

 

 



