---
description: La valeur de la propriété ProductVersion est la version du produit au format de chaîne.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: Propriété ProductVersion
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f82fcbd28c4a4132e4c3f76adfd68e33c43b36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543250"
---
# <a name="productversion-property"></a>Propriété ProductVersion

La valeur de la propriété **ProductVersion** est la version du produit au format de chaîne. Cette propriété est obligatoire.

Le format de la chaîne est le suivant :

<dl> major.minor.build  
</dl>

Le premier champ est la version principale et a une valeur maximale de 255. Le deuxième champ est la version mineure et a une valeur maximale de 255. Le troisième champ est appelé version de build ou version de mise à jour et a une valeur maximale de 65 535.

## <a name="remarks"></a>Notes

Au moins l’un des trois champs de **ProductVersion** doit changer pour une mise à niveau à l’aide de la [table de mise à niveau](upgrade-table.md). Toute mise à jour qui modifie uniquement le code du package, mais qui laisse **ProductVersion** et [**ProductCode**](productcode.md) inchangée, est appelée [petite mise à jour](small-updates.md). Les champs de trois versions sont fournis principalement pour des raisons pratiques. Par exemple, si vous souhaitez modifier **ProductVersion**, mais que vous ne voulez pas modifier les versions majeures ou mineures, vous pouvez modifier la version de la Build.

Notez que Windows Installer utilise uniquement les trois premiers champs de la version du produit. Si vous incluez un quatrième champ dans la version de votre produit, le programme d’installation ignore le quatrième champ.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Correctifs et mises à niveau](patching-and-upgrades.md)
</dt> <dt>

[petite mise à jour](small-updates.md)
</dt> </dl>

 

 




