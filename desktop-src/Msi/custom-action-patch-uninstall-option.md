---
description: Utilisez l’indicateur d’option suivant pour spécifier que le programme d’installation doit exécuter l’action personnalisée uniquement lorsqu’un correctif est en cours de désinstallation. Pour définir l’option, ajoutez la valeur de ce tableau à la valeur du champ ExtendedType de la table CustomAction.
ms.assetid: aa4d9e21-5316-42b5-a22e-c7a5becd3cae
title: Option de désinstallation corrective de l’action personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24636181ec8fb9695b9d959a25b055a7e7c21d34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091869"
---
# <a name="custom-action-patch-uninstall-option"></a>Option de désinstallation corrective de l’action personnalisée

Utilisez l’indicateur d’option suivant pour spécifier que le programme d’installation doit exécuter l’action personnalisée uniquement lorsqu’un correctif est en cours de désinstallation. Pour définir l’option, ajoutez la valeur de ce tableau à la valeur du champ ExtendedType de la [table CustomAction](customaction-table.md).

**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md):** Non pris en charge. cette option est disponible à partir de Windows Installer 4,5.



| Constante                                | Valeur hexadécimale | Decimal | Description                                                    |
|-----------------------------------------|-------------|---------|----------------------------------------------------------------|
| **msidbCustomActionTypePatchUninstall** | 0x8000      | 32 768   | L’action personnalisée s’exécute uniquement lorsqu’un correctif est en cours de désinstallation. |



 

## <a name="remarks"></a>Notes

cet attribut peut être ajouté à une action personnalisée en le créant dans le package Windows Installer (fichier .msi). Une nouvelle action personnalisée avec cet attribut peut être ajoutée par un correctif. Une action personnalisée ayant cet attribut peut être mise à jour par un correctif. Cet attribut ne peut pas être ajouté ou supprimé par un correctif à une action personnalisée existante.

si un correctif ajoute ou met à jour une action personnalisée avec cet attribut, Windows Installer exécute l’action personnalisée nouvelle ou mise à jour lorsque le correctif est désinstallé. Windows Le programme d’installation rend les mises à jour dans le correctif en cours de désinstallation disponibles pour l’action personnalisée de désinstallation des correctifs. le correctif doit inclure une table [MsiTransformView *&lt; &gt; PatchGUID*](msitransformview.md) pour fournir ces informations à Windows Installer.

lorsqu’un package qui contient une action personnalisée avec l’attribut **msidbCustomActionTypePatchUninstall** est installé à l’aide d’une version du programme d’installation antérieure à Windows Installer 4,0, le programme d’installation n’appelle pas l’action personnalisée lorsque le correctif est désinstallé. L’installation peut exécuter l’action personnalisée pendant l’installation, la réparation ou la mise à jour du package.

les actions personnalisées avec l’attribut **msidbCustomActionTypePatchUninstall** doivent être conditionnées à l’aide de la propriété [**MSIPATCHREMOVE**](msipatchremove.md) pour empêcher l’action personnalisée de s’exécuter lors de l’installation, la réparation ou la mise à jour à l’aide d’un système avec Windows Installer 4,0 ou une version antérieure. lorsque Windows Installer 4,5 et versions ultérieures est installé, tous les correctifs sur le système ayant des actions personnalisées marquées avec l’attribut **msidbCustomActionTypePatchUninstall** exécutent l’action personnalisée pendant la désinstallation des correctifs. si Windows Installer 4,5 ou une version ultérieure est supprimé du système, les correctifs perdent la fonctionnalité de désinstallation des correctifs de l’action personnalisée.

pour plus d’informations sur l’exécution d’une action personnalisée pendant la désinstallation d’un correctif à l’aide d’une version antérieure à Windows Installer 4,5, consultez [patch Uninstall custom Actions](patch-uninstall-custom-actions.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Options d’exécution d’une action personnalisée In-Script](custom-action-in-script-execution-options.md)
</dt> <dt>

[Référence des actions personnalisées](custom-action-reference.md)
</dt> <dt>

[À propos des actions personnalisées](about-custom-actions.md)
</dt> <dt>

[Utilisation d’actions personnalisées](using-custom-actions.md)
</dt> <dt>

[MsiTransformView *&lt; PatchGUID &gt;*](msitransformview.md)
</dt> </dl>

 

 



