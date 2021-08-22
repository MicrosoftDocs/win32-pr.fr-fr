---
description: Les applications peuvent récupérer et définir la date et l’heure de création, de modification ou de dernier accès d’un fichier à l’aide des fonctions GetFileTime et SetFileTime.
ms.assetid: f8930be6-7c2a-4e50-a7a1-d25f6e2a3951
title: Définition et obtention de l’horodateur d’un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e98bd87ae8224ecbebc46e5f9d0ed71ad3522097fb865afc0d16e53a828812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015127"
---
# <a name="setting-and-getting-the-timestamp-of-a-file"></a>Définition et obtention de l’horodateur d’un fichier

Les applications peuvent récupérer et définir la date et l’heure de création, de modification ou de dernier accès d’un fichier à l’aide des fonctions [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) et [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) . Pour plus d’informations, consultez [temps de fichier](/windows/desktop/SysInfo/file-times).

> [!Note]  
> Tous les systèmes de fichiers ne peuvent pas enregistrer les heures de création et de dernier accès, et tous les systèmes de fichiers ne les enregistrent pas de la même manière. Par exemple, sur le système de fichiers FAT, l’heure de création a une résolution de 10 millisecondes, le temps d’écriture a une résolution de 2 secondes et le temps d’accès a une résolution de 1 jour (en réalité, la date d’accès). Le système de fichiers NTFS retarde la mise à jour de l’heure du dernier accès pour un fichier jusqu’à une heure après le dernier accès.

 

 

 
