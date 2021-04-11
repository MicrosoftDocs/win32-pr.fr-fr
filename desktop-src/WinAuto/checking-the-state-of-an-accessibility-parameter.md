---
title: Vérification de l’état d’un paramètre d’accessibilité
description: Le fragment de code suivant utilise la fonction GetSystemMetrics pour vérifier le paramètre son texte. Si GetSystemMetrics retourne la valeur TRUE, l’application doit présenter toutes les informations importantes sous forme visuelle.
ms.assetid: fb6a0adf-ca38-4e21-9edd-1abb2efd59e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75409f5af96f83bf13f4834f83503579862caa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031331"
---
# <a name="checking-the-state-of-an-accessibility-parameter"></a>Vérification de l’état d’un paramètre d’accessibilité

Le fragment de code suivant utilise la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) pour vérifier le paramètre son texte. Si **GetSystemMetrics** retourne la **valeur true**, l’application doit présenter toutes les informations importantes sous forme visuelle.


```C++
BOOL fShowSounds; 
fShowSounds = GetSystemMetrics(SM_SHOWSOUNDS); 
```



 

 