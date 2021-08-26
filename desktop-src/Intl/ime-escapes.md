---
description: Ces séquences d’échappement sont utilisées avec la fonction ImmEscape.
ms.assetid: ede886dc-8a92-428c-8975-3feadc1d4f90
title: Échappements IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4764e884a65069d73c535d38d5ee2896b1d2ecaeb66600bd868f8830cddcfc4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107209"
---
# <a name="ime-escapes"></a>Échappements IME

Ces séquences d’échappement sont utilisées avec la fonction [**ImmEscape**](/windows/desktop/api/Imm/nf-imm-immescapea) .



| Caractère d'échappement                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IME \_ ESC d' \_ extraction de \_ l’IME \_  | Récupérez le chemin d’accès du fichier de dictionnaire EUDC. En entrée, le paramètre *lpData* doit être le pointeur vers la mémoire tampon pour recevoir le chemin d’accès. Cette mémoire tampon doit être supérieure ou égale à 80 \* sizeof (TCHAR). Au retour, la mémoire tampon contient la chaîne terminée par le caractère null qui spécifie le chemin d’accès complet du dictionnaire. Pour une utilisation par l’éditeur EUDC chinois uniquement ; n’utilisez pas dans d’autres applications.                                                                                  |
| \_ \_ mode hanja ESC \_ IME            | Conversion de hangul en hanja. À l’entrée, *lpData* doit pointer vers la mémoire tampon qui contient le caractère Hangul à convertir ; lors de la sortie, elle reçoit le hanja converti sous la forme d’une chaîne terminée par le caractère null. Pour une utilisation par l’éditeur coréen ; n’utilisez pas dans d’autres applications.                                                                                                                                                                                                           |
| \_ \_ nom IME ESC \_ IME              | Récupérez le nom de l’IME. En entrée, le paramètre *lpData* doit être le pointeur vers la mémoire tampon pour recevoir le nom. Au retour, la mémoire tampon contient la chaîne terminée par le caractère null qui spécifie le nom de l’IME. Pour une utilisation par l’éditeur EUDC chinois uniquement ; n’utilisez pas dans d’autres applications. **Windows Me/98/95 :** La mémoire tampon ne doit pas être inférieure à 16 \* sizeof (TCHAR).<br/> **Windows NT, Windows 2000, Windows XP :** La mémoire tampon ne doit pas être inférieure à 64 caractères.<br/> |
| \_ \_ clé Max IME \_ ESC               | La valeur de retour de la fonction est le nombre maximal de Stokes de clé pour un caractère EUDC. Pour une utilisation par l’éditeur EUDC chinois uniquement ; n’utilisez pas dans d’autres applications.                                                                                                                                                                                                                                                                                                         |
| \_ \_ prise en charge des requêtes ESC IME \_         | Vérifiez l’implémentation. En entrée, *lpData* pointe vers la mémoire tampon qui contient la valeur d’échappement IME. La fonction retourne 0 si l’échappement n’est pas implémenté.                                                                                                                                                                                                                                                                                                             |
| \_séquence IME \_ ESC \_ vers \_ interne | Retourne le code de caractère qui correspond au code de séquence spécifié. En entrée, le paramètre *lpData* est le pointeur vers une variable 32 bits qui contient le code de séquence. Pour une utilisation par l’éditeur EUDC chinois uniquement ; n’utilisez pas dans d’autres applications. Normalement, l’IME chinois encode ses codes de caractères en lecture dans la séquence 1 à n.                                                                                                                               |
| IME \_ ESC \_ définir \_ le \_ dictionnaire EUDC  | Définissez le fichier de dictionnaire EUDC. En entrée, le paramètre *lpData* est le pointeur vers une chaîne se terminant par un caractère null qui spécifie le chemin d’accès complet. Le chemin d’accès doit être inférieur à 80 \* sizeof (TCHAR). Pour une utilisation par l’éditeur EUDC chinois uniquement ; n’utilisez pas dans d’autres applications.                                                                                                                                                                                                           |
| IME \_ ESC \_ GETHELPFILENAME        | **Windows Me/98, Windows 2000, Windows XP :** Retourne le nom du fichier d’aide de l’IME. En cas de retour, le paramètre *lpData* est le chemin d’accès complet du fichier d’aide de l’IME. Le chemin d’accès doit être inférieur à 80 \* sizeof (TCHAR).                                                                                                                                                                                                                                                           |



 

Le système d’exploitation réserve les séquences d’échappement de la plage IME \_ ESC \_ réservée \_ d’abord à l’IME \_ ESC \_ réservé en \_ dernier pour sa propre utilisation.

Le système d’exploitation réserve les séquences d’échappement de l’IME de portée \_ ESC \_ privé \_ d’abord à IME \_ ESC \_ privé \_ en dernier pour une utilisation privée par les IME.

 

 




