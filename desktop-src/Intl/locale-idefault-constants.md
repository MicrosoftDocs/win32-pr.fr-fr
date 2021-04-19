---
description: Cette rubrique définit les \_ \* constantes IDEFAULT des paramètres régionaux utilisés par nls.
ms.assetid: 4fa8b5f3-8c01-44fb-b6fd-8dbf38e3d361
title: Constantes LOCALE_IDEFAULT *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9c440c27a2fe551eae7d03d66cc43b500e8f68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517431"
---
# <a name="locale_idefault-constants"></a>Paramètres régionaux \_ IDEFAULT \* constantes

Cette rubrique définit les \_ \* constantes IDEFAULT des paramètres régionaux utilisés par nls.



| Valeur                          | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| paramètres régionaux \_ IDEFAULTANSICODEPAGE   | Page de codes ANSI utilisée par des paramètres régionaux pour les applications qui ne prennent pas en charge Unicode. Le nombre maximal de caractères autorisés pour cette chaîne est de six, y compris un caractère null de fin. Si aucune page de codes ANSI n’est disponible, seul Unicode peut être utilisé pour les paramètres régionaux. Dans ce cas, la valeur est CP \_ ACP (0). Ces paramètres régionaux ne peuvent pas être définis comme paramètres régionaux système. Les applications qui ne prennent pas en charge Unicode ne fonctionnent pas correctement avec les paramètres régionaux marqués comme « Unicode uniquement ». Pour obtenir une liste d’ANSI et d’autres pages de codes, consultez [identificateurs de page de codes](code-page-identifiers.md). |
| paramètres régionaux \_ IDEFAULTCODEPAGE       | Page de codes OEM (Original Equipment Manufacturer) associée au pays ou à la région. La page de codes OEM est utilisée pour la conversion à partir d’applications en mode texte MS-DOS. Si les paramètres régionaux n’utilisent pas de page de codes OEM, la valeur est CP \_ OEMCP (1). Le nombre maximal de caractères autorisés pour cette chaîne est de six, y compris un caractère null de fin. Pour obtenir la liste des OEM et des autres pages de codes, consultez [identificateurs de page de codes](code-page-identifiers.md).                                                                                                               |
| paramètres régionaux \_ IDEFAULTCOUNTRY        | Obsolète. Ne pas utiliser. Cette valeur a été fournie afin que les paramètres régionaux partiellement spécifiés puissent être exécutés avec des valeurs par défaut. Les paramètres régionaux partiellement spécifiés sont désormais déconseillés.                                                                                                                                                                                                                                                                                                                                                                                               |
| paramètres régionaux \_ IDEFAULTEBCDICCODEPAGE | **Windows 2000 :** Page de codes Extended Binary Coded Decimal Interchange Code par défaut (EBCDIC) associée aux paramètres régionaux. Le nombre maximal de caractères autorisés pour cette chaîne est de six, y compris un caractère null de fin. Pour obtenir une liste des pages de codes EBCDIC et autres, consultez [identificateurs de page de codes](code-page-identifiers.md).                                                                                                                                                                                                                                     |
| paramètres régionaux \_ IDEFAULTLANGUAGE       | Obsolète. Ne pas utiliser. Cette valeur a été fournie afin que les paramètres régionaux partiellement spécifiés puissent être exécutés avec des valeurs par défaut. Les paramètres régionaux partiellement spécifiés sont désormais déconseillés.                                                                                                                                                                                                                                                                                                                                                                                               |
| paramètres régionaux \_ IDEFAULTMACCODEPAGE    | Page de codes Macintosh par défaut associée aux paramètres régionaux. Le nombre maximal de caractères autorisés pour cette chaîne est de six, y compris un caractère null de fin. Si les paramètres régionaux n’utilisent pas de page de codes Macintosh, la valeur est CP \_ MACCP (2). Pour obtenir la liste des Macintosh (MAC) et d’autres pages de codes, consultez [identificateurs de page de codes](code-page-identifiers.md).                                                                                                                                                                                                              |



 

 

 



