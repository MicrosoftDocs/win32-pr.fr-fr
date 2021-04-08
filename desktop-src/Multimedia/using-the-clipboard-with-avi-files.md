---
title: Utilisation du presse-papiers avec des fichiers AVI
description: Utilisation du presse-papiers avec des fichiers AVI
ms.assetid: 76ef7cc9-9afd-462a-b9fe-2b62f8113a9a
keywords:
- AVIPutFileOnClipboard fonction)
- AVIGetFromClipboard fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe46f463f22aa2d015d4ffd8496eb95c37053a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673281"
---
# <a name="using-the-clipboard-with-avi-files"></a>Utilisation du presse-papiers avec des fichiers AVI

Le presse-papiers offre un stockage temporaire et pratique qu’une application peut utiliser pour copier ou transférer des fichiers AVI. AVIFile comprend des fonctions de presse-papiers que vous pouvez utiliser avec des fichiers de disque ou de mémoire.

Vous pouvez copier un fichier dans le presse-papiers à l’aide de la fonction [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) . Pour écrire un fichier qui se trouve dans le presse-papiers sur la mémoire ou sur le disque, utilisez la fonction [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) .

Vous pouvez effacer un fichier du presse-papiers à l’aide de la fonction [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) . Cette fonction n’efface pas les autres types d’informations, tels que le texte, à partir du presse-papiers. Si vous utilisez les fonctions du presse-papiers dans votre application, effacez le presse-papiers avec **AVIClearClipboard** avant de fermer l’application ou de fermer le fichier dans le presse-papiers. Vous pouvez appeler **AVIClearClipboard** dans votre application, que **AVIPutFileOnClipboard** ait ou non été utilisé.

> [!Note]  
> Si votre application copie un fichier dans le presse-papiers et que le fichier contient des données de flux susceptibles de changer, vous pouvez créer un fichier de mémoire de flux clonés à l’aide de la fonction [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) . Vous pouvez ensuite placer le fichier dans le presse-papiers, puis libérer le fichier d’origine sans l’invalider.

 

 

 




