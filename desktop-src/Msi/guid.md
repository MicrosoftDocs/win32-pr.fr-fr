---
description: Le type de données GUID est une chaîne de texte représentant un identificateur de classe (ID). COM doit être en mesure de convertir la chaîne en un ID de classe valide. Tous les GUID doivent être créés en majuscules.
ms.assetid: 9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8
title: GUID (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297c9995d537f6cf4b9d2ccf35488e27dc35903f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541843"
---
# <a name="guid"></a>GUID

Le type de données GUID est une chaîne de texte représentant un identificateur de classe (ID). COM doit être en mesure de convertir la chaîne en un ID de classe valide. Tous les GUID doivent être créés en majuscules.

Le format valide pour un GUID est {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}, où X est un chiffre hexadécimal (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F).

Notez que les utilitaires tels que GUIDGEN peuvent générer des GUID contenant des lettres minuscules. Ils doivent tous être remplacés par des lettres majuscules avant que le programme d’installation ne puisse utiliser le GUID comme code de produit, code de package ou code de composant valide.

 

 



