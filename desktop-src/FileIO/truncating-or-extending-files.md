---
description: Une application peut tronquer ou étendre un fichier en appelant SetEndOfFile.
ms.assetid: 23a0242d-50e9-4324-bb09-505afe383a80
title: Troncation ou extension des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf8a2d4e7e346bfea41285be97d6d756e2a6b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521133"
---
# <a name="truncating-or-extending-files"></a>Troncation ou extension des fichiers

Une application peut tronquer ou étendre un fichier en appelant [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile). Cette fonction définit le marqueur de fin de fichier à la position actuelle du pointeur de fichier.

Notez que lorsqu’un fichier est étendu, le contenu entre les anciens et les nouveaux emplacements de fin de fichier n’est pas défini.

 

 



