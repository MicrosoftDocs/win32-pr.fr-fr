---
description: La propriété SOURCELIST est une liste délimitée par des points-virgules de chemins d’accès source réseau ou URL au package d’installation de l’application.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: SOURCELIST, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd0ab879d55481f71c663e4375a305232be576d0c923f67fa419530012d1ce89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893749"
---
# <a name="sourcelist-property"></a>SOURCELIST, propriété

La propriété **SourceList** est une liste délimitée par des points-virgules de chemins d’accès source réseau ou URL au package d’installation de l’application. Cette liste est ajoutée à la fin de la liste source existante de chaque utilisateur pour l’application. Le programme d’installation localise une source en énumérant la liste des chemins d’accès source et utilise le premier emplacement accessible trouvé. Seule cette source peut être utilisée pour le reste de l’installation. Chaque chemin d’accès spécifié dans la liste source doit correspondre à un emplacement disposant d’une source complète pour l’application. La totalité de l’arborescence de répertoires à chaque emplacement source doit être la même et doit inclure tous les fichiers sources requis, y compris les armoires. Chaque emplacement doit avoir un fichier .msi avec le même nom de fichier et le même code de produit.

## <a name="default-value"></a>Valeur par défaut

Le programme d’installation vérifie uniquement la propriété **SourceList** si le produit n’a pas déjà été publié ou installé. Dans tous les autres cas, le programme d’installation utilise la liste de sources existante qui se trouve dans le registre.

## <a name="remarks"></a>Remarques

Les sources ajoutées à l’aide de la propriété **SourceList** sont ajoutées directement à la fin de la liste pour chaque type de source et sont toujours postérieures à la source par défaut spécifiée par la propriété [**SourceDir**](sourcedir.md) .

par Windows Installer le nombre de sources dans la propriété **SOURCELIST** est illimité. [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) peut être utilisé pour ajouter des sources réseau.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Résilience source](source-resiliency.md)
</dt> </dl>

 

 




