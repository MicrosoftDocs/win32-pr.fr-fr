---
title: Vérification de l’état d’un paramètre d’accessibilité
description: Le fragment de code suivant utilise la fonction GetSystemMetrics pour vérifier le paramètre son texte. Si GetSystemMetrics retourne la valeur TRUE, l’application doit présenter toutes les informations importantes sous forme visuelle.
ms.assetid: fb6a0adf-ca38-4e21-9edd-1abb2efd59e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374520612ce96522edc1b879a49f5f30a9c7a857f9bb46a562a4ab48effebe9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122249"
---
# <a name="checking-the-state-of-an-accessibility-parameter"></a>Vérification de l’état d’un paramètre d’accessibilité

Le fragment de code suivant utilise la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) pour vérifier le paramètre son texte. Si **GetSystemMetrics** retourne la **valeur true**, l’application doit présenter toutes les informations importantes sous forme visuelle.


```C++
BOOL fShowSounds; 
fShowSounds = GetSystemMetrics(SM_SHOWSOUNDS); 
```



 

 