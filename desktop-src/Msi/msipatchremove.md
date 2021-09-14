---
description: La propriété MSIPATCHREMOVE spécifie la liste des correctifs à supprimer durant une installation.
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: Propriété MSIPATCHREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf83583c5b15311e175e67a867ff5aca71394b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119717"
---
# <a name="msipatchremove-property"></a>Propriété MSIPATCHREMOVE

La propriété **MSIPATCHREMOVE** spécifie la liste des correctifs à supprimer durant une installation. Les correctifs individuels de la liste sont séparés par des points-virgules et peuvent être représentés par le GUID du code correctif ou par le chemin d’accès complet au correctif. La fonction [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) et la méthode [**RemovePatches**](installer-removepatches.md) de l’objet [installer](installer-object.md) définissent la propriété **MSIPATCHREMOVE** .

La propriété **MSIPATCHREMOVE** peut être définie sur la ligne de commande comme suit pour supprimer un correctif.

**msiexec/i A : \\Example.msi MSIPATCHREMOVE = c : \\ patches \\ qfe1. msp ; { 0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0}; {A86B443B-E3BF-4009-ADED-F716FC735858}/QB**

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




