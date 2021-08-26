---
description: Les horodatages sont normalement inclus lorsqu’un fichier est signé à l’aide de SignTool avec l’option-t.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Ajout d’horodatages à des fichiers précédemment signés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988f63e7b5c58f5d8346d074d3ec98d31dc87443670480f7ded2e72f2272275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880229"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a>Ajout d’horodatages à des fichiers précédemment signés

Les horodatages sont normalement inclus lorsqu’un fichier est signé à l’aide de SignTool avec l’option **-t** . En outre, des horodatages peuvent être ajoutés aux fichiers qui ont été signés sans horodatage. La commande suivante ajoute un horodatage à un fichier précédemment signé :

**l’horodateur SignTool-t https : \/ /timestamp.digicert.com *MyControl.exe***

> [!Note]  
> Le fichier à horodatage doit avoir été signé précédemment.

 

Pour plus d’informations sur SignTool, consultez [SignTool](signtool.md).

 

 



