---
description: La propriété REINSTALLMODE est une chaîne qui contient des lettres spécifiant le type de réinstallation à effectuer.
ms.assetid: 756d2899-2cfe-473a-bebf-a7f7bbe7d229
title: REINSTALLMODE, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab48043ef92770cbc3a1f5ab92e459128c9945ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523632"
---
# <a name="reinstallmode-property"></a>REINSTALLMODE, propriété

La propriété **REINSTALLMODE** est une chaîne qui contient des lettres spécifiant le type de réinstallation à effectuer. Les options ne respectent pas la casse et sont indépendantes de la commande. Normalement, cette propriété doit toujours être utilisée conjointement avec la propriété [**REINSTALL**](reinstall.md) . Toutefois, cette propriété peut également être utilisée pendant l’installation, et pas seulement pour la réinstallation.

> [!Note]  
> Le Windows Installer ignore la propriété **REINSTALLMODE** pendant une [installation d’administration](administrative-installation.md).

 

## <a name="reinstall-option-codes"></a>Réinstaller les codes d’option

Par défaut, **REINSTALLMODE** est « omus ».



| Code | Option                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| p    | Réinstallez uniquement si le fichier est manquant.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| o    | Réinstallez si le fichier est manquant ou s’il s’agit d’une version antérieure.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| e    | Réinstallez si le fichier est manquant ou s’il s’agit d’une version égale ou antérieure.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| d    | Réinstallez si le fichier est manquant ou si une version différente est présente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| c    | Vérifiez les valeurs de somme de contrôle, puis réinstallez le fichier s’il est manquant ou endommagé. Cet indicateur répare uniquement les fichiers qui ont msidbFileAttributesChecksum dans la colonne attributs de la [table file](file-table.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| a    | Forcer la réinstallation de tous les fichiers, indépendamment de la somme de contrôle ou de la version.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| u    | Réécrit toutes les entrées de Registre nécessaires à partir de la [table de Registre](registry-table.md) qui sont dirigées vers l'**\_ \_ utilisateur HKEY CURRENT**<br/> ou **HKEY \_ Users**<br/> ruche du Registre.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| m    | Réécrivez toutes les entrées de Registre requises à partir de la [table de Registre](registry-table.md) qui accède à l' **\_ \_ ordinateur local HKEY** .<br/> ou **HKEY \_ classes \_ root**<br/> ruche du Registre. Réécrivez toutes les informations à partir de la [table de classe](class-table.md), de la table de [verbes](verb-table.md), de la [table PublishComponent](publishcomponent-table.md), de la [table ProgID](progid-table.md), de la [table MIME](mime-table.md), de la table d' [icônes](icon-table.md), de la [table d’extension](extension-table.md)et de la [table AppID](appid-table.md) indépendamment de l’attribution d’ordinateur Réinstallez tous les [**composants qualifiés.**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) Lors de la réinstallation d’une application, cette option exécute les actions [RegisterTypeLibraries](registertypelibraries-action.md) et [InstallODBC](installodbc-action.md) .<br/> |
| s    | Réinstallez tous les raccourcis et remettez en cache toutes les icônes en écrasant les raccourcis et les icônes existants.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| v    | Utilisez pour exécuter à partir du package source et remettre en cache le package local. N’utilisez pas le code d’option de réinstallation v pour la première installation d’une application ou d’une fonctionnalité.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

Si la propriété **REINSTALLMODE** est définie sans définir également la propriété [**REINSTALL**](reinstall.md) , les modes « détection » spécifiés s’appliquent toujours et spécifient le mode de « remplacement » pour une installation normale. La propriété **REINSTALLMODE** affecte uniquement les fonctionnalités qui sont sélectionnées normalement pour l’installation. La présence de la propriété **REINSTALLMODE** ne réinstalle pas les fonctionnalités. La réinstallation des fonctionnalités nécessite la présence de la propriété **réinstaller** .

Les codes d’option de cette propriété correspondent à l' [option de ligne de commande](command-line-options.md) « /f ». L’option de ligne de commande a la valeur par défaut « pecms ».

> [!Note]  
> Seuls les fichiers contenant des informations sur les sommes de contrôle sont vérifiés et réparés. L' \_ indicateur FILEVERIFY REINSTALLMODE (le CCODE ci-dessus) répare uniquement les fichiers qui ont msidbFileAttributesChecksum dans la colonne attributs de la [table file](file-table.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




