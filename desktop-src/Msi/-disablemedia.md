---
description: La définition de la propriété DISABLEMEDIA empêche le programme d’installation d’inscrire toute source multimédia, telle qu’un CD-ROM, comme source valide pour le produit. Toutefois, si la navigation est activée, un utilisateur peut toujours accéder à une source multimédia.
ms.assetid: 83c4e7f6-fced-447f-bfa2-847dce660139
title: Propriété DISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc1cad17269541fdb60573ae11065d485af9bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525244"
---
# <a name="disablemedia-property"></a>Propriété DISABLEMEDIA

La définition de la propriété [**DISABLEMEDIA**](disablemedia.md) empêche le programme d’installation d’inscrire toute source multimédia, telle qu’un CD-ROM, comme source valide pour le produit. Toutefois, si la navigation est activée, un utilisateur peut toujours accéder à une source multimédia.

## <a name="remarks"></a>Notes

Notez que la propriété [**DISABLEMEDIA**](disablemedia.md) a un effet différent de la définition de la stratégie DISABLEMEDIA. La définition de **DISABLEMEDIA** empêche l’inscription d’une source de support, ce qui empêche également la première installation d’une application à partir d’une source multimédia.

Pour plus d’informations sur la sécurisation des sources multimédias de l' [*application gérée*](m-gly.md) par rapport à la navigation et l’installation par des utilisateurs non administratifs, consultez [résilience source](source-resiliency.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




