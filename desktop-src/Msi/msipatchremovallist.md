---
description: Le programme d’installation définit la valeur de la propriété MsiPatchRemovalList sur une liste des correctifs en cours de suppression lors de l’installation.
ms.assetid: 6e0b391a-d840-4f01-af12-4708ce6c9ce8
title: Propriété MsiPatchRemovalList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93df2cdfc658875526c049ca7503e66a5c318df896a604a82c18751ac3358285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065979"
---
# <a name="msipatchremovallist-property"></a>Propriété MsiPatchRemovalList

Le programme d’installation définit la valeur de la propriété **MsiPatchRemovalList** sur une liste des correctifs en cours de suppression lors de l’installation. Les correctifs sont représentés dans la liste par leurs GUID de code correctif séparés par des points-virgules.

les développeurs peuvent utiliser la propriété **MsiPatchRemovalList** pour créer un package Windows Installer ou un correctif qui effectue des [actions personnalisées](custom-actions.md) sur la suppression d’un correctif. L’action personnalisée peut être créée dans le package d’installation d’origine, un correctif qui a déjà été appliqué au package ou un correctif logiciel qui ne peut pas être [installé](uninstallable-patches.md). L’action personnalisée peut être conditionnée sur la propriété **MsiPatchRemovalList** dans les tables de séquence. Pour plus d’informations sur l’inconditionnel des actions, consultez [utilisation des propriétés dans les instructions conditionnelles](using-properties-in-conditional-statements.md) .

L’action personnalisée peut obtenir les GUID des correctifs qui sont supprimés de la valeur de la propriété **MsiPatchRemovalList** . L’action personnalisée peut déterminer si l’état d’installation du correctif est appliqué, obsolète ou remplacé en appelant la fonction [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) ou la propriété [**PatchProperty**](patch-patchproperty.md) de l' [objet patch](patch-object.md).

## <a name="remarks"></a>Remarques

Pour plus d’informations sur la suppression des correctifs, consultez [suppression des correctifs](removing-patches.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




