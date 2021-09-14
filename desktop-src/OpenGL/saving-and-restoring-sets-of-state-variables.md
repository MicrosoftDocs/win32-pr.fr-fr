---
title: Enregistrement et restauration de jeux de variables d’État
description: Vous pouvez enregistrer et restaurer les valeurs d’une collection de variables d’État sur une pile d’attributs avec les fonctions glPushAttrib et glPopAttrib.
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- Variables d’État OpenGL
- enregistrement des variables d’État OpenGL
- restauration des variables d’État OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3192c228ea35005c5755802d3cd1b873f7b7fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009283"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a>Enregistrement et restauration de jeux de variables d’État

Vous pouvez enregistrer et restaurer les valeurs d’une collection de variables d’État sur une pile d’attributs avec les fonctions [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md) . La profondeur de la pile d’attributs est au moins égale à 16. Pour obtenir la profondeur réelle, utilisez la \_ profondeur de la \_ pile Max \_ . d’attrib GL \_ avec [**glGetIntegerv**](glgetintegerv.md). Le push d’une pile complète ou le dépilament d’une pile vide génère une erreur.

Il est généralement plus rapide d’utiliser **glPushAttrib** et **glPopAttrib** que pour récupérer et restaurer les valeurs vous-même. Certaines valeurs peuvent être envoyées et dépilées dans le matériel, et l’enregistrement et la restauration peuvent nécessiter beaucoup de ressources. En outre, si vous utilisez un client distant, toutes les données d’attribut doivent être transférées via la connexion réseau, puis à nouveau enregistrées et restaurées. Toutefois, votre implémentation OpenGL conserve la pile d’attributs sur le serveur, ce qui évite les retards de réseau inutiles.

Le prototype de **glPushAttrib** est le suivant :

**void** **glPushAttrib**( *masque* GLbitfield);

L’utilisation de [**glPushAttrib**](glpushattrib.md) enregistre tous les attributs indiqués par bits dans *Mask* en les envoyant sur la pile d’attributs. Pour obtenir la liste des bits de masque possibles que vous pouvez logiquement ou ensemble pour enregistrer n’importe quelle combinaison d’attributs, consultez [groupes](attribute-groups.md)d’attributs. Chaque bit correspond à une collection de variables d’État individuelles. Par exemple, le \_ bit d’éclairage GL \_ fait référence à toutes les variables d’état associées à l’éclairage, y compris la couleur de matériau actuelle, la lumière ambiante, diffuse, spéculaire et émise, une liste des lumières activées et les directions des lumières. Lorsque vous appelez [**glPopAttrib**](glpopattrib.md), toutes ces variables sont restaurées. Pour savoir exactement quels attributs sont enregistrés pour des valeurs de masque particulières, consultez la page [variables d’État OpenGL](opengl-state-variables.md).

 

 




