---
title: Services personnalisés
description: Services personnalisés
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- e/s de fichier multimédia, services personnalisés
- e/s de fichier, services personnalisés
- entrée et sortie (e/s), services personnalisés
- E/s (entrée et sortie), services personnalisés
- e/s personnalisées
- mmioInstallIOProc fonction)
- mmioOpen fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c2418d3a87669527feda37547674bee83175dd6e4533312e8b89c346048c04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144572"
---
# <a name="custom-services"></a>Services personnalisés

Les services d’e/s de fichier multimédia utilisent des procédures d’e/s pour gérer l’entrée et la sortie physiques associées à la lecture et l’écriture dans différents types de systèmes de stockage, tels que les systèmes d’archivage de fichiers et les systèmes de stockage de bases de données. Des procédures d’e/s prédéfinies existent pour les systèmes de fichiers standard et pour les fichiers de mémoire, mais vous pouvez fournir une procédure d’e/s personnalisée pour accéder à un système de stockage unique à l’aide de la fonction [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) .

Pour ouvrir un fichier à l’aide d’une procédure d’e/s personnalisée, utilisez la fonction [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . Incluez un signe plus (+) ou la constante CFSEPCHAR dans le nom de fichier pour séparer le nom du fichier physique du nom de l’élément du fichier que vous souhaitez ouvrir. L’exemple suivant ouvre un élément file nommé « element » à partir d’un fichier nommé FILENAME. ARC


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



Lorsque le gestionnaire d’e/s de fichier rencontre un signe plus dans un nom de fichier, il examine l’extension de nom de fichier pour déterminer la procédure d’e/s à associer au fichier. Dans l’exemple précédent, le gestionnaire d’e/s de fichier tenterait d’utiliser la procédure d’e/s associée au. Extension de nom de fichier ARC ; Cette procédure d’e/s aurait été installée à l’aide de [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc). Si aucune procédure d’e/s n’est installée, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) renvoie une erreur.

Les procédures d’e/s doivent répondre aux messages suivants :

-   [**MMIOM \_ Fermer**](mmiom-close.md)
-   [**MMIOM \_ ouvrir**](mmiom-open.md)
-   [**\_lecture MMIOM**](mmiom-read.md)
-   [**\_écriture MMIOM**](mmiom-write.md)
-   [**MMIOM \_ Seek**](mmiom-seek.md)
-   [**MMIOM \_ REnommer**](mmiom-rename.md)
-   [**MMIOM \_ WRITEFLUSH**](mmiom-writeflush.md)

Vous pouvez également créer des messages personnalisés et les envoyer à votre procédure d’e/s à l’aide de la fonction [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) . Si vous définissez vos propres messages, assurez-vous qu’ils sont définis au niveau ou au-dessus de la valeur définie par la \_ constante utilisateur MMIOM.

Outre le traitement des messages, une procédure d’e/s doit conserver le membre **lDiskOffset** de la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) (pointée par le paramètre *lpmmioinfo* de la fonction **mmioOpen** ). Le membre **lDiskOffset** doit toujours contenir le décalage de fichier à l’emplacement auquel le prochain \_ message d’écriture de MMIOM ou de lecture MMIOM \_ accédera. L’offset est spécifié en octets et est relatif au début du fichier. La procédure d’e/s peut utiliser le membre **adwInfo** pour conserver les informations d’État requises. La procédure d’e/s ne doit pas modifier les autres membres de la structure **MMIOINFO** .

 

 