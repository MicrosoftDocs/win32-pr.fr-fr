---
description: La propriété TARGETDIR spécifie le répertoire de destination racine pour l’installation.
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: TARGETDIR, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d5e2650dab798c1f6b9e766fc1dcbb61dcfa77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009617"
---
# <a name="targetdir-property"></a>TARGETDIR, propriété

La propriété **targetDir** spécifie le répertoire de destination racine pour l’installation. **TargetDir** doit être le nom d’une racine dans la table [Directory](directory-table.md) . Il ne peut y avoir qu’un seul répertoire de destination racine. Au cours d’une [installation administrative](administrative-installation.md) , cette propriété spécifie l’emplacement de copie du package d’installation. Au cours d’une installation non administrative, cette propriété spécifie le répertoire de destination racine.

Pour spécifier le répertoire de destination racine, définissez la colonne Directory de la table Directory sur la propriété **targetDir** et la colonne DefaultDir sur la propriété [**SourceDir**](sourcedir.md) . Si la propriété **targetDir** est définie, le répertoire de destination est résolu à la valeur de la propriété. Si la propriété **targetDir** n’est pas définie, la propriété [**ROOTDRIVE**](rootdrive.md) est utilisée pour résoudre le chemin d’accès. Pour plus d’informations sur l’utilisation de la propriété **targetDir** , consultez [utilisation de la table Directory](using-the-directory-table.md).

Notez que la valeur de la propriété **targetDir** est généralement définie au niveau de la ligne de commande ou par le biais d’une interface utilisateur. La définition de **targetDir** en créant un chemin dans la [table de propriétés](property-table.md) n’est pas recommandée, car les ordinateurs diffèrent dans la configuration du lecteur local.

Pour plus d’informations sur la modification de TARGETDIR pendant une installation, consultez [modification de l’emplacement cible d’un répertoire](changing-the-target-location-for-a-directory.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




