---
description: Le programme d’installation définit la propriété System64Folder sur le chemin d’accès complet au dossier System64 prédéfini. La propriété System64Folder existante est définie sur le dossier 32 bits correspondant.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: Propriété System64Folder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e05f9067c4f5a77b5361fdefe0f5b47b9116ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543940"
---
# <a name="system64folder-property"></a>Propriété System64Folder

Le programme d’installation définit la propriété **System64Folder** sur le chemin d’accès complet au dossier System64 prédéfini. La propriété **System64Folder** existante est définie sur le dossier 32 bits correspondant.

## <a name="remarks"></a>Notes

Le programme d’installation définit cette propriété sur Windows 64 bits. Par exemple, sur Windows 64 bits, la valeur peut être C : \\ Window \\ system32. Cette propriété n’est pas utilisée sur Windows 32 bits.

Ce dossier est normalement un sous-répertoire du dossier Windows. Toutefois, il réside sur un serveur lorsqu’il est configuré pour les fenêtres partagées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




