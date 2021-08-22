---
description: Si la propriété LIMITUI est définie, le niveau d’interface utilisateur (IU) utilisé lors de l’installation du package est limité au niveau de base.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: Propriété LIMITUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969b6e1c1de5a55581fa8d24f6d538c829e18fb48afb9bdc2fd04bae69c15162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013137"
---
# <a name="limitui-property"></a>Propriété LIMITUI

Si la propriété **LIMITUI** est définie, le niveau d’interface utilisateur (IU) utilisé lors de l’installation du package est limité au niveau de base. Cette propriété est requise dans les packages qui n’ont pas d’interface utilisateur créée, mais qui contiennent toujours des tables d’interface utilisateur telles que la [table de dialogue](dialog-table.md). Pour obtenir une description des niveaux de l’interface utilisateur, consultez [ **MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

## <a name="remarks"></a>Remarques

Les packages d’installation contenant la propriété **LIMITUI** doivent également contenir la propriété [**ARPNOMODIFY**](arpnomodify.md) . Cela est nécessaire pour qu’un utilisateur obtienne le comportement correct à partir de l’utilitaire **Ajout/suppression de programmes** dans le **panneau** de configuration lors de la tentative de configuration d’un produit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[**ARPNOMODIFY**](arpnomodify.md)
</dt> </dl>

 

 




