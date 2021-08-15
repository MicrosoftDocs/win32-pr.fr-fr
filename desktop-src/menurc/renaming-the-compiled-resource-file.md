---
title: Attribution d’un nouveau nom au fichier de ressources compilé
description: Par défaut, lors de la compilation des ressources, RC nomme le fichier de ressources compilé (. res) avec le nom de base du fichier. RC et le place dans le même répertoire que le fichier. rc.
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60f2a920eeed6c1b96b512511b965b0243b89e4f6888120c6183b7a3104963c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733516"
---
# <a name="renaming-the-compiled-resource-file"></a>Attribution d’un nouveau nom au fichier de ressources compilé

Par défaut, lors de la compilation des ressources, RC nomme le fichier de ressources compilé (. res) avec le nom de base du fichier. RC et le place dans le même répertoire que le fichier. rc. CVTRES doit ensuite être appelé pour convertir le fichier. res en un format de ressource binaire (. RBJ) qui peut être compris par l’éditeur de liens. L’exemple suivant compile MyApp. RC et crée un fichier de ressources compilé nommé MyApp. res dans le même répertoire que MyApp. RC :

**RC MyApp. RC**

L’option **/FO** donne au fichier. res qui en résulte un nom différent du nom du fichier. RC correspondant. Par exemple, pour nommer le fichier. res obtenu NewFile. res, utilisez la commande suivante :

**RC-fo newFile. res MyApp. RC**

L’option **/FO** peut également placer le fichier. res dans un répertoire différent. Par exemple, la commande suivante place le fichier de ressources compilé MyApp. res dans le répertoire C : \\ source Resource \\ :

**RC-fo c : \\ \\ ressource source \\ MyApp. res MyApp. RC**

 

 




