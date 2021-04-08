---
description: Un handle vers une ressource de communication est associé à un ensemble de paramètres de délai d’attente qui affectent le comportement des opérations de lecture et d’écriture.
ms.assetid: 271d4c68-1f6d-4483-a9a1-703220de761f
title: Délais d'expiration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db31fafc0f4d98832f1fb7fa5d22b32cba33d73
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748333"
---
# <a name="time-outs"></a>Délais d'expiration

Un handle vers une ressource de communication est associé à un ensemble de paramètres de délai d’attente qui affectent le comportement des opérations de lecture et d’écriture. Les délais d’attente peuvent entraîner la conclusion d’une opération [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)ou [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) lorsqu’un intervalle de délai d’attente arrive à expiration, même si le nombre spécifié de caractères n’a pas été lu ou écrit. Elle n’est pas traitée comme une erreur lorsqu’un délai d’attente se produit pendant une opération de lecture ou d’écriture (autrement dit, la valeur de retour de la fonction de lecture ou d’écriture indique une réussite). Le nombre d’octets lus ou écrits est signalé par **ReadFile** ou **WriteFile** (ou par la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) ou [**FileIOCompletionRoutine**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) , si l’e/s a été effectuée comme une opération avec chevauchement).

Lorsqu’une application ouvre une ressource de communication, le système définit les valeurs de délai d’attente de la ressource en vigueur lors de la dernière utilisation de la ressource. Si la ressource de communication n’a jamais été ouverte, le système définit les valeurs de délai d’attente sur une valeur par défaut. Dans les deux cas, une application doit toujours déterminer les valeurs de délai d’attente actuelles après avoir ouvert la ressource, puis les définir explicitement pour répondre à ses exigences. Pour déterminer les valeurs de délai d’attente actuelles d’une ressource de communication, utilisez la fonction [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) . Pour modifier les valeurs de délai d’attente, utilisez la fonction [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts) .

Deux types de délais d’expiration sont activés par les paramètres de délai d’attente. Un délai d’expiration de l’intervalle se produit lorsque la durée entre deux caractères au maximum est supérieure à un nombre spécifié de millisecondes. Le minutage commence lorsque le premier caractère est reçu et est redémarré à la réception de chaque nouveau caractère. Un délai d’attente total se produit lorsque la durée totale consommée par une opération de lecture dépasse un nombre calculé de millisecondes. Le minutage démarre immédiatement après le début de l’opération d’e/s. Les opérations d’écriture prennent uniquement en charge les délais d’expiration totaux. Les opérations de lecture prennent en charge l’intervalle et les délais d’expiration totaux, qui peuvent être utilisés séparément ou combinés.

Le temps, en millisecondes, du délai d’attente total pour une opération de lecture ou d’écriture est calculé à l’aide des valeurs de multiplicateur et constante de la structure [**COMMTIMEOUTS**](/windows/desktop/api/Winbase/ns-winbase-commtimeouts) spécifiée dans la fonction [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) ou [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts) . La formule utilisée est la suivante :


```C++
Timeout = (MULTIPLIER * number_of_bytes) + CONSTANT
```



L’utilisation d’un multiplicateur et d’une constante permet de modifier le délai d’attente total, en fonction de la quantité de données demandée. Une application peut utiliser uniquement la constante en affectant la valeur zéro au multiplicateur, ou utiliser uniquement le multiplicateur en affectant à la constante la valeur zéro. Si la constante et le multiplicateur sont tous deux nuls, le délai d’attente total n’est pas utilisé.

Si tous les paramètres de délai d’attente de lecture sont nuls, les délais d’attente de lecture ne sont pas utilisés et une opération de lecture n’est pas terminée tant que le nombre d’octets demandé n’a pas été lu ou qu’une erreur se produit. De même, si tous les paramètres de délai d’attente d’écriture sont nuls, une opération d’écriture n’est pas terminée tant que le nombre d’octets demandé n’a pas été écrit ou qu’une erreur se produit.

Si le paramètre de délai d’attente de l’intervalle de lecture est la valeur **MAXDWORD** et que les deux paramètres de délai d’attente du total de lecture sont nuls, une opération de lecture est effectuée immédiatement après la lecture des caractères disponibles dans la mémoire tampon d’entrée, même si elle est vide.

Le minutage de l’intervalle force une opération de lecture à retourner lorsqu’un accalmie est en cours de réception. Un processus utilisant des délais d’expiration de l’intervalle peut définir un paramètre d’intervalle assez court. il peut donc réagir rapidement aux petites rafales isolées d’un ou de plusieurs caractères, mais il peut quand même collecter de grandes mémoires tampons de caractères avec un seul appel lorsque les données sont reçues dans un flux stable.

Les délais d’attente d’une opération d’écriture peuvent être utiles lorsque la transmission est bloquée par un type de contrôle de flow ou lorsque la fonction [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) a été appelée pour suspendre la transmission de caractères.

Le tableau suivant résume le comportement des opérations de lecture en fonction des valeurs spécifiées pour les délais d’expiration totaux et des intervalles.



| Total | Intervalle | Comportement                                                                                                                                                                                 |
|-------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 0        | Retourne lorsque la mémoire tampon est entièrement remplie. Les délais d’attente ne sont pas utilisés.                                                                                                                    |
| T     | 0        | Retourne lorsque la mémoire tampon est entièrement remplie ou lorsque T millisecondes se sont écoulées depuis le début de l’opération.                                                                   |
| 0     | O        | Retourne lorsque la mémoire tampon est entièrement remplie ou lorsque les millisecondes Y se sont écoulées entre la réception de deux caractères quelconques. Le minutage ne commence pas tant que le premier caractère n’a pas été reçu. |
| T     | O        | Retourne lorsque la mémoire tampon est entièrement remplie ou lorsque l’un ou l’autre type de dépassement de délai se produit.                                                                                                     |



 

> [!Note]  
> Toutefois, cette synchronisation est relative au système qui contrôle l’appareil physique. Pour un appareil distant tel qu’un modem, le minutage est relatif au système serveur auquel le modem est attaché. Tout délai de propagation réseau n’est pas pris en compte dans. Par exemple, une application cliente peut spécifier un délai d’expiration total qui se calcule sur 500 millisecondes. Lorsque 500 millisecondes se sont écoulées sur le serveur, une erreur de délai d’attente est retournée au client. En cas de délai de propagation réseau de 50 millisecondes, le client n’est pas notifié du délai d’attente jusqu’à environ 50 millisecondes après l’expiration du délai d’attente.

 

> [!Note]  
> Les paramètres de délai d’attente affectent le comportement des opérations de lecture et d’écriture avec chevauchement sur un appareil de communication. Avec les e/s avec chevauchement, la fonction [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)ou [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) peut être renvoyée avant la fin de l’opération. Les paramètres de délai d’attente peuvent déterminer à quel moment l’opération a été effectuée.

 

 

 
