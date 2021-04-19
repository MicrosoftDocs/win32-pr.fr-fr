---
description: La propriété SourceDir est le répertoire racine qui contient le fichier cab source ou l’arborescence des fichiers sources du package d’installation. Cette valeur est utilisée pour la résolution d’annuaire.
ms.assetid: 900b26e8-80dd-4e70-8d79-37f09a0c6e86
title: SourceDir, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a366e4afecdd16722a06ecfbec08552baab8f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541733"
---
# <a name="sourcedir-property"></a>SourceDir, propriété

La propriété **SourceDir** est le répertoire racine qui contient le fichier cab source ou l’arborescence des fichiers sources du package d’installation. Cette valeur est utilisée pour la résolution d’annuaire.

## <a name="default-value"></a>Valeur par défaut

Répertoire qui contient le package d’installation.

## <a name="remarks"></a>Notes

L' [action ResolveSource](resolvesource-action.md) doit être appelée avant d’utiliser la propriété **SourceDir** dans une expression ou une tentative de récupération de la valeur de **SourceDir** avec [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya). L’action ResolveSource ne doit pas être exécutée tant que la source n’est pas disponible, par exemple lors de la désinstallation d’une application, car cela peut entraîner une invite inattendue pour le média source.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




