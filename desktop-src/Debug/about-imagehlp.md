---
description: Les fonctions ImageHlp sont principalement utilisées par les outils de programmation, les utilitaires d’installation d’application et d’autres programmes qui ont besoin d’accéder aux données contenues dans une image PE.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: À propos de ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aee63eba22293fe1fb56cb6608110f4343a0c6bc26a4be597bfbd884cdf87cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815649"
---
# <a name="about-imagehlp"></a>À propos de ImageHlp

Les fonctions ImageHlp sont principalement utilisées par les outils de programmation, les utilitaires d’installation d’application et d’autres programmes qui ont besoin d’accéder aux données contenues dans une image PE. Toutes les fonctions ImageHlp sont à thread unique. Par conséquent, les appels à partir de plusieurs threads à cette fonction entraîneront probablement un comportement inattendu ou une altération de la mémoire. Pour éviter cela, vous devez synchroniser tous les appels simultanés à partir de plusieurs threads à cette fonction.

Les rubriques suivantes décrivent les images PE et les fonctionnalités fournies par les fonctions ImageHlp.

-   [Format PE](pe-format.md)
-   [Fonctions d’accès aux images](image-access-functions.md)
-   [Fonctions d’intégrité de l’image](image-integrity-functions.md)
-   [Fonctions de modification d’image](image-modification-functions.md)

 

 



