---
description: Paramètres régionaux \_ S1159 et paramètres régionaux \_ Sam
ms.assetid: dc7058af-1d5f-40a0-8d0b-17d2ff5662ce
title: LOCALE_S1159 et LOCALE_SAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b41f98ea5c07f1d88534c1e47acecfa81a4e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867053"
---
# <a name="locale_s1159-and-locale_sam"></a>Paramètres régionaux \_ S1159 et paramètres régionaux \_ Sam

Chaîne pour l’indicateur AM (12 premières heures de la journée). Le nombre maximal de caractères autorisés pour cette chaîne, y compris un caractère null de fin, est différent pour les différentes versions de Windows.

**Windows XP :** Treize incluant un caractère null de fin pour [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Quinze incluant un caractère null de fin pour [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).

**Windows Me/98/95, Windows NT 4,0, windows 2000 :** Neuf incluant un caractère null de fin.

**Windows Server 2003 et versions ultérieures :** Quinze incluant un caractère null de fin.

Windows 10 a ajouté la valeur **paramètres régionaux \_ Sam** comme synonyme plus lisible pour les **paramètres régionaux \_ S1159**.

 

 



