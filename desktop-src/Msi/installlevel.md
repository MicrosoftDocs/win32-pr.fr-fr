---
description: La propriété INSTALLLEVEL est le niveau initial auquel les fonctionnalités sont sélectionnées &\# 0034 ; sur&\# 0034 ; pour une installation par défaut.
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: Propriété INSTALLLEVEL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e349e8d92a2c480866b04a1ca57885ffa1cdb230d8346b357318fa239ead72a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629958"
---
# <a name="installlevel-property"></a>Propriété INSTALLLEVEL

La propriété **INSTALLLEVEL** est le niveau initial auquel les fonctionnalités sont sélectionnées par défaut pour l’installation. Une fonctionnalité est installée uniquement si la valeur du champ niveau de la [table de fonctionnalités](feature-table.md) est inférieure ou égale à la valeur actuelle de INSTALLLEVEL. Le niveau d’installation de n’importe quelle installation est spécifié par la propriété **INSTALLLEVEL** et peut être un entier compris entre 1 et 32 767. Pour plus d’informations sur les niveaux d’installation, consultez [table des fonctionnalités](feature-table.md).

## <a name="default-value"></a>Valeur par défaut

Si aucune valeur n’est spécifiée, le niveau d’installation par défaut est 1.

## <a name="remarks"></a>Remarques

Le niveau d’installation spécifié par la propriété **INSTALLLEVEL** peut être remplacé par les propriétés suivantes :

-   [**ADDLOCAL**](addlocal.md)
-   [**ADDSOURCE**](addsource.md)
-   [**ADDDEFAULT**](adddefault.md)
-   [**COMPADDLOCAL**](compaddlocal.md)
-   [**COMPADDSOURCE**](compaddsource.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**Installez**](remove.md)
-   [**INSTALLÉ**](reinstall.md)
-   [**PUBLIÉS**](advertise.md)

Par exemple, la définition de ADDLOCAL = ALL installe toutes les fonctionnalités localement, quelle que soit la valeur de la propriété **INSTALLLEVEL** . Si la valeur de la colonne Level dans la [table Feature](feature-table.md) est 0, cette fonctionnalité n’est pas installée et n’est pas affichée dans l’interface utilisateur.

Un administrateur peut désactiver définitivement une fonctionnalité en appliquant une transformation de personnalisation qui définit 0 dans la colonne de niveau pour cette fonctionnalité. L’application de la transformation de personnalisation empêche l’installation et l’affichage de la fonctionnalité même si l’utilisateur sélectionne une installation complète à l’aide de l’interface utilisateur ou en affectant à ADDLOCAL la valeur ALL sur la ligne de commande. Consultez [un exemple de transformation de personnalisation](a-customization-transform-example.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




