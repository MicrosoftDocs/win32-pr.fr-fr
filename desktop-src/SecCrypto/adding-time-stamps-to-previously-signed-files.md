---
description: Les horodatages sont normalement inclus lorsqu’un fichier est signé à l’aide de SignTool avec l’option-t.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Ajout d’horodatages à des fichiers précédemment signés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e750dcb178b2a089bfbde0b2aea882b097c86
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106522560"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a>Ajout d’horodatages à des fichiers précédemment signés

Les horodatages sont normalement inclus lorsqu’un fichier est signé à l’aide de SignTool avec l’option **-t** . En outre, des horodatages peuvent être ajoutés aux fichiers qui ont été signés sans horodatage. La commande suivante ajoute un horodatage à un fichier précédemment signé :

**l’horodateur SignTool-t https : \/ /timestamp.digicert.com *MyControl.exe***

> [!Note]  
> Le fichier à horodatage doit avoir été signé précédemment.

 

Pour plus d’informations sur SignTool, consultez [SignTool](signtool.md).

 

 



