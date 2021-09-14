---
description: Le programme d’installation définit la propriété TempFolder sur le chemin d’accès complet au dossier Temp. Les auteurs n’ont pas besoin de définir la propriété TempFolder.
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: Propriété TempFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf042086d8bb174a02a7b421ced1133a70016e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009614"
---
# <a name="tempfolder-property"></a>Propriété TempFolder

Le programme d’installation définit la propriété **TempFolder** sur le chemin d’accès complet au dossier Temp.

Les auteurs n’ont pas besoin de définir la propriété **TempFolder** . Windows Le programme d’installation utilise la fonction [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) pour récupérer le chemin d’accès du répertoire désigné pour les fichiers temporaires et pour définir cette propriété.

## <a name="remarks"></a>Remarques

La valeur courante de cette propriété est C : \\ temp.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 
