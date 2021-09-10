---
title: Écriture dans un fichier
description: Écriture dans un fichier
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- AVIFileWriteData fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9a6b9a399d8581909c99da615e32ef4487cbb
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368684"
---
# <a name="writing-to-a-file"></a>Écriture dans un fichier

Vous pouvez écrire des informations supplémentaires dans un fichier qui a été ouvert avec des privilèges d’écriture à l’aide de la fonction [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) . Cette fonction copie les informations à partir d’une mémoire tampon fournie par l’application et les place dans un ou plusieurs segments du fichier. Le segment « INFO » est un type de bloc RIFF courant dans lequel la fonction stocke des informations supplémentaires. Pour obtenir une description des fichiers RIFF et des segments de données, consultez [services de format de fichier](resource-interchange-file-format-services.md)de l’échange de ressources.

 

 




