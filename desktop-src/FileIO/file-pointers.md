---
description: Un pointeur de fichier est une valeur de décalage de 64 bits qui spécifie l’octet suivant à lire ou l’emplacement de réception de l’octet suivant écrit.
ms.assetid: 1e8bc657-affa-4a17-8435-c93de5075a1d
title: Pointeurs de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4fc804711665c045361d40c69fb71a4959b4c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202218"
---
# <a name="file-pointers"></a>Pointeurs de fichiers

Lorsqu’un fichier est ouvert, Windows associe un *pointeur de fichier* avec le flux par défaut. Ce pointeur de fichier est une valeur de décalage de 64 bits qui spécifie l’octet suivant à lire ou l’emplacement de réception de l’octet suivant écrit. Chaque fois qu’un fichier est ouvert, le système place le pointeur de fichier au début du fichier, qui est le décalage zéro. Chaque opération de lecture et d’écriture avance le pointeur de fichier du nombre d’octets lus et écrits. Par exemple, si le pointeur de fichier se trouve au début du fichier et qu’une opération de lecture de 5 octets est demandée, le pointeur de fichier se trouvera au décalage 5 immédiatement après l’opération de lecture. À mesure que chaque octet est lu ou écrit, le système avance le pointeur de fichier. Le pointeur de fichier peut également être repositionné en appelant la fonction [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) .

Quand le pointeur de fichier atteint la fin d’un fichier et que l’application tente de lire à partir du fichier, aucune erreur ne se produit, mais aucun octet n’est lu. Par conséquent, la lecture de zéro octet sans erreur signifie que l’application a atteint la fin du fichier. L’écriture de zéro octet ne fait rien.

Une application peut tronquer ou étendre un fichier à l’aide de la fonction [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) . Cette fonction définit la fin du fichier à la position actuelle du pointeur de fichier.

 

 



