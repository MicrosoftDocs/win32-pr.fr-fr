---
description: Le programme d’installation définit la dernière propriété enregistrée par Résumé sur une valeur qui varie selon qu’il s’agit d’un package d’installation, d’une transformation ou d’un package de correctifs. Dans un package d’installation, le programme d’installation définit cette propriété sur la valeur de la propriété LogonUser au cours d’une installation d’administration. Les développeurs d’outils d’édition de base de données peuvent utiliser cette propriété pendant le processus de développement pour suivre la dernière personne à modifier la base de données d’installation. Cette propriété doit avoir la valeur null dans une base de données d’expédition finale. Le programme d’installation n’utilise jamais cette propriété et un utilisateur n’a jamais besoin de le modifier. Dans une transformation, cette propriété Summary contient les ID de plateforme et de langue qu’une base de données doit avoir une fois qu’elle a été transformée. La propriété spécifie ce que le résumé de modèle doit être défini dans la nouvelle base de données. Dans un package correctif, cette propriété Summary contient une liste délimitée par des points-virgules de noms de sous-stockage de transformation dans l’ordre dans lequel ils sont appliqués par ce correctif.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Dernier enregistrement par propriété de résumé
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfd1c00863eee3bc31728783042ada8298b2067
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011983"
---
# <a name="last-saved-by-summary-property"></a>Dernier enregistrement par propriété de résumé

Le programme d’installation définit la **dernière propriété enregistrée par Résumé** sur une valeur qui varie selon qu’il s’agit d’un package d’installation, d’une transformation ou d’un package de correctifs.

Dans un package d’installation, le programme d’installation définit cette propriété sur la valeur de la propriété [**LogonUser**](logonuser.md) au cours d’une [installation d’administration](administrative-installation.md). Les développeurs d’outils d’édition de base de données peuvent utiliser cette propriété pendant le processus de développement pour suivre la dernière personne à modifier la base de données d’installation. Cette propriété doit avoir la valeur null dans une base de données d’expédition finale. Le programme d’installation n’utilise jamais cette propriété et un utilisateur n’a jamais besoin de le modifier.

Dans une transformation, cette propriété Summary contient les ID de plateforme et de langue qu’une base de données doit avoir une fois qu’elle a été transformée. La propriété spécifie ce que le [**Résumé de modèle**](template-summary.md) doit être défini dans la nouvelle base de données.

Dans un package correctif, cette propriété Summary contient une liste délimitée par des points-virgules de noms de sous-stockage de transformation dans l’ordre dans lequel ils sont appliqués par ce correctif.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Descriptions des propriétés de synthèse](summary-property-descriptions.md)
</dt> </dl>

 

 




