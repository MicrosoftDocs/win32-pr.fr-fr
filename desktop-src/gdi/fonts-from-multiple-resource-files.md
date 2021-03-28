---
description: Polices de plusieurs fichiers de ressources
ms.assetid: 4625fe62-d55d-4828-9174-975a731a8f62
title: Polices de plusieurs fichiers de ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3802705ba4b199fa00d2cc2961d3c4472c4e365
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2021
ms.locfileid: "104996448"
---
# <a name="fonts-from-multiple-resource-files"></a>Polices de plusieurs fichiers de ressources

En règle générale, une police est contenue dans un fichier de ressources de police unique. Toutefois, les informations de certaines polices sont réparties entre plusieurs fichiers. Par exemple, tapez 1 plusieurs polices principales requièrent deux fichiers :

-   . PFM pour les métriques de police
-   . PFB pour les bits de police

Pour ajouter une police de plusieurs fichiers au système, utilisez les fonctions [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) ou [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) . Le paramètre *lpszFilename* dans ces fonctions doit pointer vers une chaîne qui contient les noms de fichiers séparés par la barre verticale ou le canal ( \| ). Par exemple, pour spécifier abcxxxxx. PFM et abcxxxxx. PFB pour une police de type 1, utilisez la chaîne « abcxxxxx. PFM \| abcxxxxx. PFB ».

[**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) diffère de [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) en ce que l’application qui appelle **AddFontResourceEx** peut spécifier la police comme étant privée ou non énumérable.

Pour ajouter une police à partir d’une image mémoire, utilisez [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex). Cela permet à une application d’utiliser une police incorporée dans un document ou une page Web.

Pour supprimer une police provenant de plusieurs fichiers de ressources, appelez [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) ou [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), selon la fonction utilisée pour ajouter la police. Vous devez spécifier les mêmes indicateurs que ceux utilisés pour ajouter la police. Pour supprimer une police qui a été ajoutée à partir d’une image mémoire, utilisez [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).

L’utilisation d’une police qui provient de plusieurs fichiers de ressources de police est identique à l’utilisation d’une police d’un fichier de ressources unique.

 

 
