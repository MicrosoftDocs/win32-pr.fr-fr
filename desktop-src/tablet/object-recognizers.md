---
description: En plus de reconnaître du texte, les module de reconnaissance peuvent reconnaître une classe d’objets connexes.
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: Identificateurs d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a258c8486bcf773f5f94c4de51c501e107fac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952535"
---
# <a name="object-recognizers"></a>Identificateurs d’objets

En plus de reconnaître du texte, les module de reconnaissance peuvent reconnaître une classe d’objets connexes. Les détecteurs d’objets reconnaissent les formes générales, en fonction de leur rôle. Les identificateurs d’objet sont utilisés pour reconnaître :

-   Notes musicales
-   Formes géométriques
-   Équations mathématiques
-   Éléments de l’organigramme

En règle générale, les objets reconnus par ce module de reconnaissance sont dans une relation spatiale ou fonctionnelle à deux dimensions. Par exemple, dans les relations complexes d’une équation mathématique, un module de reconnaissance peut retourner des résultats différents pour une limite supérieure sur un entier défini, par opposition à un numérateur dans une fraction.

En raison de la nature très générale de ces relations, il est extrêmement difficile de définir l’ensemble des interfaces qui fonctionnent pour chaque module de reconnaissance d’objets.

La technologie Tablet PC fournit une infrastructure de base pour les identificateurs d’objet dans la bibliothèque managée et les interfaces d’automatisation. Toutefois, vous devez développer des interfaces personnalisées qui décrivent des relations spatiales complexes entre des objets reconnus pour chaque module de reconnaissance d’objet. Plus précisément, pour les regroupements d’objets, la plateforme fournit l’objet [**RecognizerContext**](inkrecognizercontext-class.md) de base permettant d’associer l’objet [**Ink**](inkdisp-class.md) au contexte du module de reconnaissance et d’appeler le module de reconnaissance pour effectuer la reconnaissance.

 

 



