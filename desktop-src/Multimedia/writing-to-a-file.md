---
title: Écriture dans un fichier
description: Écriture dans un fichier
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- AVIFileWriteData fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7bf46125d9da8b9e5e0668f504028db8b011c99c780b545f9ea99accc0a9ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891769"
---
# <a name="writing-to-a-file"></a>Écriture dans un fichier

Vous pouvez écrire des informations supplémentaires dans un fichier qui a été ouvert avec des privilèges d’écriture à l’aide de la fonction [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) . Cette fonction copie les informations à partir d’une mémoire tampon fournie par l’application et les place dans un ou plusieurs segments du fichier. Le segment « INFO » est un type de bloc RIFF courant dans lequel la fonction stocke des informations supplémentaires. Pour obtenir une description des fichiers RIFF et des segments de données, consultez [services de format de fichier](resource-interchange-file-format-services.md)de l’échange de ressources.

 

 




