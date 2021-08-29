---
description: Décrit les opérations de point d’analyse que vous pouvez effectuer à l’aide de DeviceIoControl.
ms.assetid: c7279203-2443-401e-b541-038954094266
title: Opérations de point d’analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7990a402270beb2f85b2355f379d971e72cf7ecb82204ee4a04e5b306e3b57bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914379"
---
# <a name="reparse-point-operations"></a>Opérations de point d’analyse

Pour déterminer si un système de fichiers prend en charge les points d’analyse, appelez la fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) et examinez le **fichier \_ prend en charge \_ \_** l’indicateur de bit points d’analyse.

La fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) vous permet de définir, de modifier, d’obtenir et de supprimer des points d’analyse. Le tableau suivant décrit les opérations de point d’analyse que vous pouvez effectuer à l’aide de **DeviceIoControl**.



| Opération                                                           | Description                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**FSCTL \_ définir le \_ point d’analyse \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)       | Autorise le programme appelant à définir un nouveau point d’analyse ou à en modifier un existant.<br/> |
| [**FSCTL \_ recevoir le \_ point d’analyse \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)       | Obtient les informations stockées dans un point d’analyse existant.<br/>                         |
| [**FSCTL \_ supprimer le \_ point d’analyse \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point) | Supprime un point d’analyse existant.<br/>                                                   |



 

Si vous modifiez, obtenez ou supprimez un point d’analyse, vous devez spécifier la même balise d’analyse dans l’opération qui est contenue dans le fichier. Dans le cas contraire, l’opération échouera avec l’erreur erreur d’analyse de la **\_ \_ balise \_ d’analyse**. Si vous modifiez ou supprimez un point d’analyse, vous devez également spécifier le **GUID** d’analyse dans l’opération contenue dans le fichier. Dans le cas contraire, l’opération échoue avec **le \_ conflit d' \_ attribut \_** d’erreur d’analyse.

Pour déterminer si un fichier ou un répertoire contient un point d’analyse, utilisez la fonction [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) . Si le fichier ou le répertoire est associé à un point d’analyse, l’attribut de **\_ point d' \_ analyse \_** de l’attribut de fichier est défini.

Pour remplacer un point d’analyse existant sans avoir déjà un handle vers le fichier ou le répertoire, appelez [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) avec l' **indicateur de fichier \_ ouvrir le \_ \_ \_ point d’analyse**. Cet indicateur vous permet d’ouvrir le fichier que le filtre de système de fichiers correspondant soit installé et qu’il fonctionne correctement.

 

