---
description: Utilisez le code suivant pour définir la fréquence de rappel.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Définition de la fréquence de rappel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e03c260b6d289e473f27bb3ae6b84a3f42d0878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318522"
---
# <a name="setting-the-callback-frequency"></a>Définition de la fréquence de rappel

Utilisez le code suivant pour définir la fréquence de rappel :

**Valeur DWORD** Valeur = 1 ;


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



Ce fragment de code définit la fréquence de rappel sur 1 seconde (valeur minimale). La valeur maximale doit être supérieure à 1. Si la mémoire tampon du fournisseur de paquets réseau (NPP) est pleine, le NPP rappelle le moniteur plus tôt.

 

 



