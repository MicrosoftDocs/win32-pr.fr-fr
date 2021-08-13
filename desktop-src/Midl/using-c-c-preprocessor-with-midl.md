---
title: Utilisation du préprocesseur C/C++ avec MIDL
description: Le compilateur MIDL ne prétraite pas les fichiers sources.
ms.assetid: 0f62d2a4-cfc3-42a7-b3a6-4e5c67c7c849
keywords:
- MIDL du compilateur MIDL, C-preprocesseur
- MIDL de préprocesseur C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac3952a342b101f0366d2bce8810426e758c4aa5b32fa267e685bc6d658f034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382793"
---
# <a name="using-cc-preprocessor-with-midl"></a>Utilisation du préprocesseur C/C++ avec MIDL

Le compilateur MIDL ne prétraite pas les fichiers sources. Au lieu de cela, le compilateur MIDL utilise un préprocesseur disponible pour préparer le flux d’entrée pour l’analyse. Par défaut, MIDL utilise le préprocesseur pour le compilateur Microsoft C/C++ du même environnement de construction que MIDL. L’utilisateur peut indiquer un préprocesseur différent à utiliser par MIDL, si nécessaire.

MIDL génère des exécutions distinctes de préprocesseur pour les fichiers IDL et ACF de niveau supérieur, et pour chaque fichier importé avec la directive d’importation MIDL. Les fichiers inclus avec la directive **\# include** sont gérés directement par le préprocesseur.

Les rubriques suivantes décrivent les différents aspects de MIDL-interactions du préprocesseur :

-   [C-Configuration requise pour le préprocesseur pour MIDL](c-preprocessor-requirements-for-midl.md)
-   [Vérification des options de préprocesseur](verifying-preprocessor-options.md)
-   [Enregistrement de la sortie du préprocesseur](saving-preprocessor-output.md)
-   [Gestion des \# définitions dans les fichiers IDL](dealing-with-defines-in-idl-files-2.md)

 

 




