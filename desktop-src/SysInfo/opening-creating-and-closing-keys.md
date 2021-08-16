---
description: Pour qu’une application puisse ajouter des données au registre, elle doit créer ou ouvrir une clé.
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: Ouverture, création et fermeture de clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 605d53a00506122c6350abd7f06e9166ed487de98c7910a3b7c3a913978492f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763961"
---
# <a name="opening-creating-and-closing-keys"></a>Ouverture, création et fermeture de clés

Pour qu’une application puisse ajouter des données au registre, elle doit créer ou ouvrir une clé. Pour créer ou ouvrir une clé, une application fait toujours référence à la clé en tant que sous-clé d’une clé actuellement ouverte. Les clés prédéfinies suivantes sont toujours ouvertes : **HKEY \_ local \_ machine**, **HKEY \_ classes \_ root**, **HKEY \_ Users** et **HKEY \_ Current \_ User**. Une application utilise la fonction [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) pour ouvrir une clé et la fonction [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) pour créer une clé. Une arborescence du Registre peut avoir 512 niveaux de profondeur. Vous pouvez créer jusqu’à 32 niveaux à la fois à l’aide d’un appel d’API de Registre unique.

Une application peut utiliser la fonction [**échec RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) pour fermer une clé et écrire les données qu’elle contient dans le registre. **Échec RegCloseKey** n’écrit pas nécessairement les données dans le registre avant de retourner. le vidage du cache sur le disque dur peut prendre jusqu’à plusieurs secondes. Si une application doit écrire explicitement des données du Registre sur le disque dur, elle peut utiliser la fonction [**regflushkey a**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) . Toutefois, **regflushkey a** utilise de nombreuses ressources système et doit être appelé uniquement lorsque cela est absolument nécessaire.

 

 



