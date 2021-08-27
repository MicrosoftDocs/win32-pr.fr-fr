---
description: paramètres régionaux \_ ITIMEMARKPOSN
ms.assetid: 4aef2631-c05b-41e8-8f4d-f40da4143ab4
title: LOCALE_ITIMEMARKPOSN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802da8f3d1029dd42c14eb536175d16e897d34a11edbd6be0bfe4f30d44c42db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106458"
---
# <a name="locale_itimemarkposn"></a>paramètres régionaux \_ ITIMEMARKPOSN

Spécificateur indiquant si la chaîne du marqueur d’heure (AM ou PM) précède ou suit la chaîne d’heure. La valeur de Registre est iTimePrefix pour la compatibilité avec les versions asiatiques précédentes de Windows. Le spécificateur doit avoir l’une des valeurs suivantes. Aucune valeur spécifiée par l’utilisateur n’est autorisée. Il est préférable que votre application utilise la constante [ \_ sTimeFormat par de paramètres régionaux](locale-stime-constants.md) au lieu des paramètres régionaux \_ ITIMEMARKPOSN.



| Valeur | Signification        |
|-------|----------------|
| 0     | Utilisez comme suffixe. |
| 1     | Utilisez comme préfixe. |



 

 

 



