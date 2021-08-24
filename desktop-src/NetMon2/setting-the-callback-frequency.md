---
description: Utilisez le code suivant pour définir la fréquence de rappel.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Définition de la fréquence de rappel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f235377865583e48d6a4b9c16abce4209e6449f74ed3cf42688dfa417287bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363245"
---
# <a name="setting-the-callback-frequency"></a>Définition de la fréquence de rappel

Utilisez le code suivant pour définir la fréquence de rappel :

**Valeur DWORD** Valeur = 1 ;


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



Ce fragment de code définit la fréquence de rappel sur 1 seconde (valeur minimale). La valeur maximale doit être supérieure à 1. Si la mémoire tampon du fournisseur de paquets réseau (NPP) est pleine, le NPP rappelle le moniteur plus tôt.

 

 



