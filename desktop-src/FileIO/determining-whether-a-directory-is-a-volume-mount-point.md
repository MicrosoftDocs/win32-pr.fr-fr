---
description: Comment déterminer si un répertoire spécifié est un dossier monté.
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: Déterminer si un répertoire est un dossier monté
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c0af53a63f64164604a5f8f22532add3dded1a46d19d96354c0da37e12d4d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150592"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a>Déterminer si un répertoire est un dossier monté

Il est utile de déterminer si un répertoire est un dossier monté lorsque, par exemple, vous utilisez une application de sauvegarde ou de recherche limitée à un volume. Une telle application peut atteindre des informations sur plusieurs volumes si vous utilisez des fonctions telles que [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) pour créer des dossiers montés pour les autres volumes sur le volume auquel l’application est limitée. Pour plus d’informations, consultez [création de dossiers montés](mounting-and-dismounting-a-volume.md).

Pour déterminer si un répertoire spécifié est un dossier monté, appelez d’abord la fonction [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) , puis examinez l’indicateur de point d’analyse d’attribut de fichier dans la valeur de retour pour voir si le répertoire a un point d’analyse associé. **\_ \_ \_** Si c’est le cas, utilisez les fonctions [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) et [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) pour obtenir la balise d’analyse dans le membre **dwReserved0** de la structure de [**\_ \_ données de recherche Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) . Pour déterminer si le point d’analyse est un dossier monté (et non une autre forme de point d’analyse), testez si la valeur de balise est égale au **point de montage d’étiquette d’analyse d’e/s \_ \_ \_ \_** de valeur. Pour plus d’informations, consultez [points d’analyse](reparse-points.md).

Pour obtenir le volume cible d’un dossier monté, utilisez la fonction [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .

De la même façon, vous pouvez déterminer si un point d’analyse est un lien symbolique en testant si la valeur de balise est un lien de **\_ \_ BALIse \_ d’analyse d’e/s**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Constantes d’attribut de fichier**](file-attribute-constants.md)
</dt> </dl>

 

 



