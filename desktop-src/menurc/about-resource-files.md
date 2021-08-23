---
title: À propos des fichiers de ressources
description: décrit comment inclure des ressources dans votre application Windows avec RC.
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f351592c57cb628204ad6528a48bfa1a10507f5e7aad90a524ea2f6034f304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034467"
---
# <a name="about-resource-files"></a>À propos des fichiers de ressources

pour inclure des ressources dans votre application basée sur Windows avec RC, procédez comme suit :

1.  Créez des fichiers individuels pour vos curseurs, icônes, bitmaps, boîtes de dialogue et polices.
2.  Créez un script de définition de ressources (fichier. RC) qui décrit les ressources utilisées par votre application.
3.  Compilez le script avec RC. Pour plus d’informations, consultez [utilisation de RC (ligne de commande RC)](using-rc-the-rc-command-line-.md).
4.  Liez le fichier de ressources compilé (. res) au fichier exécutable de l’application avec votre éditeur de liens.

Un fichier de ressources est un fichier texte avec l’extension. rc. Le fichier peut utiliser des caractères codés sur un octet, codés sur deux octets ou Unicode. La syntaxe et la sémantique du préprocesseur RC sont similaires à celles du compilateur Microsoft C/C++. Toutefois, RC prend en charge un sous-ensemble des directives de préprocesseur, des définitions et des pragmas dans un script.

Le fichier de script définit les ressources. Pour une ressource qui existe dans un fichier distinct, tel qu’une icône ou un curseur, le script spécifie la ressource et le fichier qui la contient. Pour certaines ressources, telles qu’un menu, la définition complète de la ressource existe dans le script.

Les rubriques suivantes décrivent les informations qu’un fichier de script peut contenir :

-   [Commentaires](comments.md), qui sont des remarques à ignorer par RC.
-   [Macros prédéfinies](predefined-macros.md), qui ne prennent pas d’arguments et ne peuvent pas être redéfinies.
-   Les [directives de préprocesseur](preprocessor-directives.md), qui indiquent à RC d’effectuer des actions sur le script avant de le compiler.
-   Les [opérateurs de préprocesseur](preprocessor-operators.md), qui sont utilisés avec la directive **\# define** .
-   [Directives pragma](pragma-directives.md)
-   Les [instructions de définition de ressource](resource-definition-statements.md), qui renomment et décrivent les ressources.

 

 




