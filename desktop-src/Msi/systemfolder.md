---
description: Le programme d’installation définit la propriété SystemFolder sur le chemin d’accès complet du dossier système.
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: Propriété SystemFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1567942e981af161654d41988ef797b64116af5cdb25e07a3d4f1465fc4ce975
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142007"
---
# <a name="systemfolder-property"></a>Propriété SystemFolder

Le programme d’installation définit la propriété **SystemFolder** sur le chemin d’accès complet du dossier système.

## <a name="remarks"></a>Remarques

Le programme d’installation définit cette propriété. par exemple, sur 32 bits Windows la valeur peut être C : \\ Windows \\ System32. sur la Windows 64 bits, la valeur peut être C : \\ Windows \\ SysWow64.

ce dossier est normalement un sous-répertoire du dossier Windows. Toutefois, il réside sur un serveur lorsqu’il est configuré pour des Windows partagés.

Ce dossier est local, même s’il est configuré pour des Windows partagés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




