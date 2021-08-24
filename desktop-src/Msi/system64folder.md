---
description: Le programme d’installation définit la propriété System64Folder sur le chemin d’accès complet au dossier System64 prédéfini. La propriété System64Folder existante est définie sur le dossier 32 bits correspondant.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: Propriété System64Folder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d586451ab596f5b480c74f382659596128a12c041596dec3c530b18307af2820
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500429"
---
# <a name="system64folder-property"></a>Propriété System64Folder

Le programme d’installation définit la propriété **System64Folder** sur le chemin d’accès complet au dossier System64 prédéfini. La propriété **System64Folder** existante est définie sur le dossier 32 bits correspondant.

## <a name="remarks"></a>Remarques

Le programme d’installation définit cette propriété sur l’Windows 64 bits. par exemple, sur l’Windows 64 bits, la valeur peut être C : \\ Window \\ System32. Cette propriété n’est pas utilisée sur les Windowss 32 bits.

ce dossier est normalement un sous-répertoire du dossier Windows. Toutefois, il réside sur un serveur lorsqu’il est configuré pour des Windows partagés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




