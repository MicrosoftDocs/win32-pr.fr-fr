---
description: '\_Constantes de retour de paramètres régionaux \*'
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: Constantes LOCALE_RETURN *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58714897333f69b058588f9050b9bb52ed29c37d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466026"
---
# <a name="locale_return-constants"></a>\_Constantes de retour de paramètres régionaux \*

Cette rubrique définit les \_ constantes de retour de paramètres régionaux \* utilisées par nls.




| Valeur | Signification | 
|-------|---------|
| LOCALE_RETURN_GENITIVE_NAMES | <strong>Windows 7 et versions ultérieures :</strong> Récupérez les noms génitif des mois, qui sont les noms utilisés lorsque les noms de mois sont combinés à d’autres éléments. Par exemple, en ukrainien, l’équivalent de janvier est écrit « Січень » lorsque le mois est nommé seul. Toutefois, lorsque le nom du mois est utilisé en combinaison, par exemple, dans une date telle que le 5 janvier 2003, la forme génitif du nom est utilisée. Pour l’exemple ukrainien, le nom du mois génitif est affiché sous la forme « 5 січня 2003 ». La liste des noms de mois génitif commence par janvier et est délimitée par des points-virgules. S’il n’y a pas de 13e mois, utilisez un point-virgule à la fin de la liste.<blockquote>[!Note]<br />Les noms de mois génitif n’existent pas dans toutes les langues.</blockquote><br /><br /> | 
| LOCALE_RETURN_NUMBER | <strong>Windows Me/98, Windows NT 4,0 et versions ultérieures :</strong> Récupérez un nombre. Cette constante fait en sorte que <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> ou <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> récupère une valeur sous la forme d’un nombre et non sous forme de chaîne. La mémoire tampon qui reçoit la valeur doit être au moins égale à la longueur d’une valeur DWORD. Cette constante peut être combinée à toute autre constante dont le nom commence par « LOCALE_I ». | 




 

 

 




