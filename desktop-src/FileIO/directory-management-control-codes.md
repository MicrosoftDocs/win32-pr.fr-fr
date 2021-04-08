---
description: Codes de contrôle utilisés avec la compression et la décompression de fichiers et avec des points d’analyse.
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: Codes de contrôle de gestion d’annuaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0463860e3c899178ec5b8f9d44bd05cf4278e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867694"
---
# <a name="directory-management-control-codes"></a>Codes de contrôle de gestion d’annuaire

Les codes de contrôle suivants sont utilisés avec la [compression et la décompression des fichiers](file-compression-and-decompression.md).



| Code de contrôle                                             | Signification                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ recevoir la \_ compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | Récupère l’état de compression actuel d’un fichier ou d’un répertoire sur un volume dont le système de fichiers prend en charge la compression par flux.<br/>    |
| [**FSCTL \_ définir la \_ compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | Définit l’état de compression d’un fichier ou d’un répertoire sur un volume dont le système de fichiers prend en charge la compression par fichier et par répertoire.<br/> |



 

Les codes de contrôle suivants sont utilisés avec des [points d’analyse](reparse-points.md).

## <a name="in-this-section"></a>Dans cette section



| Code de contrôle                                                                   | Description                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ supprimer le \_ point d’analyse \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | Supprime un point d’analyse du fichier ou du répertoire spécifié.<br/>                                              |
| [**FSCTL \_ recevoir le \_ point d’analyse \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | Récupère les données du point d’analyse associées au fichier ou au répertoire identifié par le handle spécifié.<br/> |
| [**FSCTL \_ définir le \_ point d’analyse \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | Définit un point d’analyse sur un fichier ou un répertoire.<br/>                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codes de contrôle de gestion des fichiers](file-management-control-codes.md)
</dt> <dt>

[Codes de contrôle de gestion des volumes](volume-management-control-codes.md)
</dt> </dl>

 

