---
description: Paramètres régionaux \_ S2359 et paramètres régionaux \_
ms.assetid: 8a97073e-84f6-47d9-98fb-65760e8a6cd8
title: LOCALE_S2359 et LOCALE_SPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8690d40907135b88966286c8cb36cf72cf31f372ba2160fc6d49637ac813129d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106319"
---
# <a name="locale_s2359-and-locale_spm"></a>Paramètres régionaux \_ S2359 et paramètres régionaux \_

Chaîne pour l’indicateur PM (les 12 dernières heures du jour). Le nombre maximal de caractères autorisés pour cette chaîne est différent pour les différentes versions de Windows.

**Windows XP :** Treize incluant un caractère null de fin pour [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Quinze incluant un caractère null de fin pour [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).

**Windows Me/98/95, Windows NT 4,0, Windows 2000 :** Neuf incluant un caractère null de fin.

**Windows Server 2003 et versions ultérieures :** Quinze incluant un caractère null de fin.

Windows 10 ajouté la valeur de **paramètres \_ régionaux** en tant que synonyme plus lisible pour les **paramètres régionaux \_ S2359**.

 

 



