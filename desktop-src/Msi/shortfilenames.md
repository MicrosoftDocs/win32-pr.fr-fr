---
description: La définition de la propriété SHORTFILENAMES entraîne l’utilisation de noms de fichiers courts pour les noms de fichiers cibles, plutôt que pour les noms de fichiers longs. Elle n’affecte pas les noms de fichiers que le programme d’installation recherche à la source.
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: Propriété SHORTFILENAMES
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e347e5ec400a1593858f0cac558f33528e25396e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021246"
---
# <a name="shortfilenames-property"></a>Propriété SHORTFILENAMES

La définition de la propriété **SHORTFILENAMES** entraîne l’utilisation de noms de fichiers courts pour les noms de fichiers cibles, plutôt que pour les noms de fichiers longs. Elle n’affecte pas les noms de fichiers que le programme d’installation recherche à la source.

## <a name="default-value"></a>Valeur par défaut

Les noms longs sont utilisés par le programme d’installation si la propriété **SHORTFILENAMES** n’est pas définie et que le volume cible prend en charge les noms longs. Les noms courts sont utilisés par le programme d’installation si le volume cible ne prend pas en charge les noms longs.

## <a name="remarks"></a>Notes

Lorsque la propriété **SHORTFILENAMES** est définie, le programme d’installation crée des dossiers et installe les fichiers à l’aide de noms de fichiers courts à partir de toute \| paire de caractères courts figurant dans la table de [fichiers](file-table.md) ou le [tableau de répertoire](directory-table.md).

Les applications peuvent utiliser la fonction [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) pour récupérer la forme abrégée d’un chemin d’accès de fichier spécifié.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 
