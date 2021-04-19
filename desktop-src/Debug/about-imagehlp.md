---
description: Les fonctions ImageHlp sont principalement utilisées par les outils de programmation, les utilitaires d’installation d’application et d’autres programmes qui ont besoin d’accéder aux données contenues dans une image PE.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: À propos de ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76da517a396536640df0e9bfcfa05368e4d0b76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514521"
---
# <a name="about-imagehlp"></a>À propos de ImageHlp

Les fonctions ImageHlp sont principalement utilisées par les outils de programmation, les utilitaires d’installation d’application et d’autres programmes qui ont besoin d’accéder aux données contenues dans une image PE. Toutes les fonctions ImageHlp sont à thread unique. Par conséquent, les appels à partir de plusieurs threads à cette fonction entraîneront probablement un comportement inattendu ou une altération de la mémoire. Pour éviter cela, vous devez synchroniser tous les appels simultanés à partir de plusieurs threads à cette fonction.

Les rubriques suivantes décrivent les images PE et les fonctionnalités fournies par les fonctions ImageHlp.

-   [Format PE](pe-format.md)
-   [Fonctions d’accès aux images](image-access-functions.md)
-   [Fonctions d’intégrité de l’image](image-integrity-functions.md)
-   [Fonctions de modification d’image](image-modification-functions.md)

 

 



