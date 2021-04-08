---
title: Plages
description: Plages
ms.assetid: 7488e29e-3409-4db3-98b4-f3438ad7c94e
keywords:
- Text Services Framework (TSF), plages
- TSF (Text Services Framework), plages
- services de texte, plages
- Applications compatibles TSF, plages
- ranges
- Text Services Framework (TSF), ancres
- TSF (Text Services Framework), ancres
- services de texte, ancres
- Applications compatibles TSF, ancres
- Points d’ancrage
- Text Services Framework (TSF), clones
- TSF (Text Services Framework), clones
- services de texte, clones
- Applications compatibles TSF, clones
- clones
- Text Services Framework (TSF), sauvegardes
- TSF (Text Services Framework), sauvegardes
- services de texte, sauvegardes
- Applications compatibles TSF, sauvegardes
- backups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6430f28731f95c0ad9c1beb04b31f0600b8c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940304"
---
# <a name="ranges"></a>Plages

## <a name="anchors"></a>Ancres

Une plage est délimitée par deux points d' *ancrage*, un point d’ancrage de début et un point d’ancrage de fin. Une ancre existe dans un emplacement imaginaire entre deux caractères. L’ancre de début se réfère au texte qui suit l’ancre et le point d’ancrage de fin est associé au texte qui précède l’ancre. Les ancres de début et de fin peuvent se trouver au même emplacement. Dans ce cas, la plage a une longueur de zéro.

Par exemple, commencez par le texte suivant :


```C++
This is text.
```



Appliquez à présent une plage à ce texte avec les ancres de début et de fin à la position 0. Il est représenté visuellement de la façon suivante :


```C++
<anchor></anchor>This is text.
```



Les ancres n’occupent pas d’espace dans le texte proprement dit. Il s’agit d’une plage de longueur nulle et son texte est vide.

Décalez à présent l’ancrage de fin + 3 positions. Il est représenté visuellement de la façon suivante :


```C++
<anchor>Thi</anchor>s is text.
```



L’ancre de début est positionnée juste avant le caractère de la position 0 et l’ancre de fin est positionnée juste après le caractère de la position 3, car l’ancrage de fin est déplacé vers la droite de 3 endroits. La plage de texte est désormais « Thi ».

En outre, l’ancre de début ne peut pas être effectuée pour suivre l’ancre de fin et l’ancre de fin ne peut pas être précédée de l’ancre de début.

## <a name="anchor-gravity"></a>Gravité d’ancrage

Chaque ancre a un paramètre de *gravité* qui détermine le mode de réponse de l’ancre quand du texte est inséré dans le flux de texte à la position d’ancrage. Lorsqu’une insertion est effectuée à la position d’un point d’ancrage, un ajustement doit être effectué à la position de l’ancre. La gravité détermine la façon dont ce réglage de la position d’ancrage est effectué.

Par exemple :


```C++
It is <anchor></anchor>cold today.
```



Si le mot « très » est inséré à la position de la plage, l’ancre de début peut être positionnée avant ou après le mot inséré :


```C++
It is <anchor>very </anchor>cold today.
```



\- Ou -


```C++
It is very <anchor></anchor>cold today.
```



La gravité d’ancrage spécifie la manière dont l’ancrage est repositionné lorsqu’une insertion est effectuée à sa position. La gravité peut être vers l' *arrière* ou *vers l’avant*.

Si l’ancrage a une gravité descendante, l’ancre se déplace vers l’arrière par rapport au point d’insertion, à l’insertion, de sorte que le texte inséré suit le point d’ancrage :


```C++
It is <anchor>very </anchor>cold today.
```



Si le point d’ancrage a une gravité en avant, l’ancrage avance (par rapport au point d’insertion) à l’insertion, de sorte que le texte inséré précède l’ancre :


```C++
It is very <anchor></anchor>cold today.
```



## <a name="clones-and-backups"></a>Clones et sauvegardes

Il existe deux façons de créer une « copie » d’un objet Range. La première consiste à créer un *clone* de la plage à l’aide de [ITfRange :: Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone). La seconde consiste à effectuer une *sauvegarde* de la plage à l’aide de [ITfContext :: CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).

Un clone est une copie d’une plage qui n’inclut pas de données statiques. Les ancres de la plage sont copiées, mais le clone couvre toujours une plage de texte dans le contexte. Un clone est un objet Range à tous égards. Cela signifie que le texte et les propriétés d’une plage clonée sont dynamiques et changent si le texte et/ou les propriétés de la plage couverte par le clone changent.

Une sauvegarde stocke le texte et les propriétés d’une plage au moment où la sauvegarde est effectuée sous forme de données statiques. Une sauvegarde clone également la plage d’origine afin que les modifications apportées à la taille et à la position de la plage d’origine puissent être suivies. Cela signifie que le texte et les propriétés d’une plage sauvegardée sont statiques et ne changent pas si le texte et/ou les propriétés de la plage couverte par la sauvegarde sont modifiés.

Par exemple, la plage suivante (pRange) dans le contexte :


```C++
"This is some <pRange>text</pRange>."
```



Créez maintenant un clone et une sauvegarde de cette plage :


```C++
ITfRange *pClone;
ITfRangeBackup *pBackup;

pRange->Clone(&pClone);
pContext->CreateRangeBackup(ec, pRange, &pBackup);
```



À présent, les objets contiennent les éléments suivants :


```C++
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



À présent, modifiez le texte de pRange :


```C++
WCHAR wsz[] = L"other words";
pRange->SetText(ec, 0, wsz, lstrlenW(wsz));
```



À présent, les objets contiennent les éléments suivants :


```C++
Context = "This is some other words."
pRange  = "other words"
pClone  = "other words"
pBackup = "text"
```



La définition du texte a entraîné la modification du texte dans le contexte. Elle a également provoqué la modification de l’ancre de fin de pRange et pClone. pClone contient maintenant « other words », car le texte a été modifié dans la plage et ces modifications sont suivies par toutes les plages. Lorsque le texte couvert à la fois par pRange et pClone a changé, le texte de pClone a également changé.

Le texte dans pBackup n’a pas été modifié par rapport au pRange d’origine, car les données (texte et propriétés) de la sauvegarde ne sont pas liées au contexte et sont stockées séparément. Le clone contenu dans la sauvegarde change en réalité, mais les données sont statiques.

Lors de la restauration d’une sauvegarde, la sauvegarde peut être appliquée au clone au sein de la sauvegarde ou à une plage différente. Pour appliquer la sauvegarde au clone au sein de la sauvegarde, transmettez la **valeur null** à [ITfRangeBackup :: Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) , comme indiqué dans l’exemple de code suivant :


```C++
pBackup->Restore(ec, NULL);
```



À présent, les objets contiennent les éléments suivants :


```C++
Context = "This is some text."
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



Pour restaurer la sauvegarde dans une autre plage, transmettez un pointeur vers l’objet Range lors de l’appel de **ITfRangeBackup :: Restore**. Le texte et les propriétés sauvegardés seront appliqués à la nouvelle plage. Par exemple, à l’aide de l’exemple ci-dessus, avant l’appel **Restore** , Prange sera modifié pour illustrer ceci :


```C++
LONG lShifted;
pRange->ShiftEnd(ec, -2, &lShifted, NULL);
```



À présent, les objets contiennent les éléments suivants :


```C++
Context = "This is some other words."
pRange  = "other wor"
pClone  = "other words"
pBackup = "text"
```



Lorsque l’ancrage de fin de pRange a été déplacé vers les deux emplacements de gauche, l’ancrage de fin de pClone n’a pas changé.

À présent, restaurez la sauvegarde à l’aide de pRange avec l’exemple de code suivant :


```C++
pBackup->Restore(ec, pRange);
```



À présent, les objets contiennent les éléments suivants :


```C++
Context = "This is some textds."
pRange  = "text"
pClone  = "textds"
pBackup = "text"
```



Le texte couvert par pRange a été remplacé par « Text », une partie du texte couvert par pClone a changé et pBackup change pour correspondre à pRange.

 

 




