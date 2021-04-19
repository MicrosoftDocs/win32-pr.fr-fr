---
description: paramètres régionaux \_ ITIMEMARKPOSN
ms.assetid: 4aef2631-c05b-41e8-8f4d-f40da4143ab4
title: LOCALE_ITIMEMARKPOSN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0182235754d8f5b6b95bad6c58b4fee87d394d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542064"
---
# <a name="locale_itimemarkposn"></a>paramètres régionaux \_ ITIMEMARKPOSN

Spécificateur indiquant si la chaîne du marqueur d’heure (AM ou PM) précède ou suit la chaîne d’heure. La valeur de Registre est iTimePrefix pour la compatibilité avec les versions asiatiques précédentes de Windows. Le spécificateur doit avoir l’une des valeurs suivantes. Aucune valeur spécifiée par l’utilisateur n’est autorisée. Il est préférable que votre application utilise la constante [ \_ sTimeFormat par de paramètres régionaux](locale-stime-constants.md) au lieu des paramètres régionaux \_ ITIMEMARKPOSN.



| Valeur | Signification        |
|-------|----------------|
| 0     | Utilisez comme suffixe. |
| 1     | Utilisez comme préfixe. |



 

 

 



