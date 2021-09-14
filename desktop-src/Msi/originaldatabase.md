---
description: l’Windows Installer définit la propriété OriginalDatabase sur le chemin d’accès de la base de données d’installation utilisée pour lancer l’installation.
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: Propriété OriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 592bc86a9ef53602f686e48b3c98dad17a49cfe1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218873"
---
# <a name="originaldatabase-property"></a>Propriété OriginalDatabase

l’Windows Installer définit la propriété **OriginalDatabase** sur le chemin d’accès de la base de données d’installation utilisée pour lancer l’installation. Si l’installation est lancée à partir d’une ligne de commande, la valeur varie selon que l’option de package recache (l’indicateur-v) est présente ou non dans la propriété [**REINSTALLMODE**](reinstallmode.md) .



| Méthode d’installation                                                                                                                                                                                  | Valeur OriginalDatabase                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Toute installation lancée en appelant le chemin d’accès du package d’installation (fichier .msi).                                                                                                              | Chemin d’accès au package d’installation (fichier .msi). |
| Installation lancée à partir d’une ligne de commande. L’installation n’est pas lancée à partir d’un chemin d’accès au package. L’option recache (indicateur-v) est présente dans la propriété [**REINSTALLMODE**](reinstallmode.md) .     | Chemin d’accès à la base de données sur la source.           |
| Installation lancée à partir d’une ligne de commande. L’installation n’est pas lancée à partir d’un chemin d’accès au package. L’option recache (indicateur-v) n’est pas présente dans la propriété [**REINSTALLMODE**](reinstallmode.md) . | Chemin d’accès à la base de données mise en cache.                  |



 

## <a name="remarks"></a>Notes

Lors de la première installation, une séquence d’action personnalisée avant l' [action ResolveSource](resolvesource-action.md) peut utiliser la propriété **OriginalDatabase** pour déterminer l’emplacement de la source d’installation.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




