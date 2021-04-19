---
description: La propriété ROOTDRIVE spécifie le lecteur par défaut pour le répertoire de destination de l’installation.
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: Propriété ROOTDRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f64b50105727d307867b5ed2910aed042cd28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537426"
---
# <a name="rootdrive-property"></a>Propriété ROOTDRIVE

La propriété **ROOTDRIVE** spécifie le lecteur par défaut pour le répertoire de destination de l’installation. Si la colonne Directory de la [table Directory](directory-table.md) indique le répertoire de destination racine par un nom de propriété qui n’est pas défini, le programme d’installation utilise la valeur de la propriété **ROOTDRIVE** pour résoudre le chemin d’accès au répertoire de destination.

Si **ROOTDRIVE** n’est pas défini sur une ligne de commande ou qu’il a été créé dans la [table de propriétés](property-table.md), le programme d’installation définit cette propriété. Au cours d’une [installation d’administration](administrative-installation.md) , le programme d’installation définit **ROOTDRIVE** sur le premier lecteur réseau connecté qu’il trouve dans lequel il est possible d’écrire. S’il ne s’agit pas d’une installation d’administration, ou si le programme d’installation ne peut pas trouver de lecteurs réseau, le programme d’installation définit **ROOTDRIVE** sur le lecteur local qui peut être écrit avec le plus d’espace libre.

La valeur de cette propriété doit se terminer par' \\ '.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




