---
title: Utilisation des bibliothèques de types par Outils de développement
description: Utilisation des bibliothèques de types par Outils de développement
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e829459176d96beab3fd818b7bafe3cddfb7969ff46531d26709ef6391ecc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993072"
---
# <a name="how-developer-tools-use-type-libraries"></a>Utilisation des bibliothèques de types par Outils de développement

Le diagramme suivant illustre comment les différents outils de développement interagissent avec la bibliothèque de types d’un objet COM. Chaque bibliothèque de types expose des interfaces de programmation standard que les outils peuvent appeler pour obtenir des informations sur les éléments décrits dans cette bibliothèque de types. Dans ce diagramme, GUID correspond à un identificateur global unique et à RPC pour un appel de procédure distante.

![Diagramme qui montre comment l’outil de développement interagit avec la bibliothèque de types d’un objet C O M.](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

dans le diagramme précédent, les outils de conversion C++, tels que le compilateur MIDL et les assistants fournis par le système de développement Microsoft Visual C++, génèrent des fichiers d’en-tête et stub. Vous pouvez ajouter ces fichiers à votre projet afin d’utiliser l’objet COM décrit par la bibliothèque de types.

De même, dans Java, les outils de développement génèrent des fichiers source et de classe Java, que vous pouvez ensuite importer dans votre application.

dans Visual Basic, le scénario est un peu plus simple. Vous n’avez pas besoin de générer des fichiers supplémentaires. l’environnement Visual Basic fournit des boîtes de dialogue qui répertorient les objets COM actuellement installés sur votre ordinateur. Vous sélectionnez le composant que vous souhaitez appeler à partir de votre application et il est ajouté à votre projet, comme un composant ou une référence.

La visionneuse OLE-COM lit une bibliothèque de types, génère un fichier IDL temporaire basé sur la bibliothèque de types et l’affiche pour les utilisateurs. La visionneuse OLE-COM affiche également la syntaxe C++ pour les éléments COM listés dans la bibliothèque de types.

Pour plus d’informations sur les bibliothèques de types, consultez [bibliothèques de types et le langage de description d’objet](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).

 

 