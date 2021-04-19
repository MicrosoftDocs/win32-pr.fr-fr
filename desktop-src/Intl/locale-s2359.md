---
description: Paramètres régionaux \_ S2359 et paramètres régionaux \_
ms.assetid: 8a97073e-84f6-47d9-98fb-65760e8a6cd8
title: LOCALE_S2359 et LOCALE_SPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca0c22d541102fcdf0826778de591dc4100dda55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521085"
---
# <a name="locale_s2359-and-locale_spm"></a>Paramètres régionaux \_ S2359 et paramètres régionaux \_

Chaîne pour l’indicateur PM (les 12 dernières heures du jour). Le nombre maximal de caractères autorisés pour cette chaîne est différent pour les différentes versions de Windows.

**Windows XP :** Treize incluant un caractère null de fin pour [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Quinze incluant un caractère null de fin pour [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).

**Windows Me/98/95, Windows NT 4,0, windows 2000 :** Neuf incluant un caractère null de fin.

**Windows Server 2003 et versions ultérieures :** Quinze incluant un caractère null de fin.

Windows 10 a ajouté la valeur **paramètres régionaux \_ SPM** comme synonyme plus lisible pour les **paramètres régionaux \_ S2359**.

 

 



