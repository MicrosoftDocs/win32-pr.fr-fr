---
description: Vous pouvez appliquer la petite mise à jour à une installation locale de MNP2000 avec l’exemple de patch MNPpatch. msp créé lors de la génération d’un package de correctifs.
ms.assetid: 928182ae-5ddb-446f-a9b8-e8b3aa4ce49c
title: Application d’un package de correctifs à une installation locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db0f29c5ced78ff8f5ad4ce8c667ba7265dd7426f9a34a5d17f743e07bfc6ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078119"
---
# <a name="applying-a-patch-package-to-a-local-installation"></a>Application d’un package de correctifs à une installation locale

Vous pouvez appliquer la petite mise à jour à une installation locale de MNP2000 avec l’exemple de patch MNPpatch. msp créé lors de la [génération d’un package de correctifs](generating-a-patch-package.md). La procédure générale est décrite dans la section [application de petites mises à jour en appliquant des correctifs à l’installation locale du produit](applying-small-updates-by-patching-the-local-installation-of-the-product.md).

Installez le produit MNP2000 d’origine localement sur votre ordinateur. Vérifiez que cette erreur est Concert.txt que la mise à jour doit être corrigée. Ensuite, lancez l’installation en entrant la ligne de commande suivante.

**msiexec/p MNP2000. msp REINSTALL = ALL REINSTALLMODE = omus**

Réexaminez les Concert.txt appartenant à MNP2000 pour vérifier que le programme d’installation a appliqué la petite mise à jour pour corriger ce fichier.

Pour appliquer la petite mise à jour à une image administrative, consultez [application d’un package de correctifs à une installation d’administration](applying-a-patch-package-to-an-administrative-installation.md).

[Continuer](applying-a-patch-package-to-an-administrative-installation.md)

 

 



