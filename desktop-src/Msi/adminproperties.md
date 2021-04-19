---
description: Le AdminProperties doit être créé dans la table de propriétés.
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: Propriété AdminProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739a0e29526ac7c6d9c094bc492cde1d04cdd0f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535412"
---
# <a name="adminproperties-property"></a>Propriété AdminProperties

Le **AdminProperties** doit être créé dans la [table de propriétés](property-table.md). La valeur de **AdminProperties** est une liste de noms de propriétés séparés par des points-virgules. Le programme d’installation enregistre les valeurs de ces propriétés listées au moment de l' [installation administrative](administrative-installation.md). Lorsque les utilisateurs installent à partir de l’image administrative, l’installation utilise les valeurs enregistrées des propriétés, plutôt que les valeurs du fichier. msi.

## <a name="remarks"></a>Notes

Les noms de propriétés dans la liste peuvent être des lettres majuscules et minuscules (propriétés privées) ou tout en majuscules (propriétés publiques).

Cette propriété ne doit jamais se terminer par un point-virgule.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




