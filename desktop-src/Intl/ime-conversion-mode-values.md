---
description: Passez en revue la liste des valeurs du mode de conversion de l’éditeur de méthode d’entrée (IME). Ces valeurs sont utilisées avec les fonctions ImmGetConversionStatus et ImmSetConversionStatus.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Valeurs du mode de conversion IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c52bc2f8f6f9fc87df48a15c66ce24b33e51742
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240263"
---
# <a name="ime-conversion-mode-values"></a>Valeurs du mode de conversion IME

Ces valeurs sont utilisées avec les fonctions [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) et [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .



| bit                      | Signification                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| IME \_ CMODE \_ alphanumérique | Mode de saisie alphanumérique. Il s’agit de la valeur par défaut, définie comme 0x0000.                          |
| \_CHARCODE CMODE \_ IME     | Défini sur 1 si le mode de saisie du code du caractère ; 0 dans le cas contraire.                                          |
| CMODE de l’IME \_ \_         | Défini sur 1 si le mode de conversion EUDC ; 0 dans le cas contraire.                                               |
| \_CMODE IME \_ corrigé        | **Windows Me/98, Windows 2000, Windows XP :** Défini sur 1 si le mode de conversion est fixe ; 0 dans le cas contraire. |
| IME \_ CMODE \_ FULLSHAPE    | Défini sur 1 en mode de forme complète ; 0 s’il s’agit du mode demi-forme.                                        |
| IME \_ CMODE \_ HANJACONVERT | Défini sur 1 si le mode de conversion HANJA ; 0 dans le cas contraire.                                                 |
| \_CMODE IME \_ Katakana     | Défini sur 1 si le mode KATAKANA ; 0 en mode HIRAGANA.                                            |
| IME \_ CMODE \_ natif       | Défini sur 1 en mode natif ; 0 si le mode est alphanumérique.                                          |
| \_CMODE \_ NOconversion IME | Défini sur 1 pour empêcher le traitement des conversions par l’IME ; 0 dans le cas contraire.                           |
| \_CMODE \_ roman IME        | Défini sur 1 si le mode d’entrée romain ; 0 dans le cas contraire.                                                   |
| IME \_ CMODE \_ SOFTKBD      | Défini sur 1 si le mode de clavier logiciel est activé ; 0 dans le cas contraire.                                                 |
| \_symbole IME CMODE \_       | Défini sur 1 si le mode de conversion des symboles ; 0 dans le cas contraire.                                             |



 

Tous les autres bits sont réservés.

 

 



