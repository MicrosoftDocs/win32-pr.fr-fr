---
description: La propriété Privileged indique si l’installation est effectuée dans le contexte de privilèges élevés.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Privileged, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d28a7079e7ab12b9832447172f1b3b2c8650a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110946"
---
# <a name="privileged-property"></a>Privileged, propriété

La propriété **Privileged** indique si l’installation est effectuée dans le contexte de privilèges élevés. Le programme d’installation définit cette propriété si l’utilisateur dispose de privilèges d’administrateur, si l’application a été affectée par un administrateur système, ou si les stratégies d’utilisateur et d’ordinateur AlwaysInstallElevated a sont définies sur true.

## <a name="default-value"></a>Valeur par défaut

Le programme d’installation ne définit pas cette propriété si l’utilisateur n’est pas autorisé à installer avec des privilèges élevés.

## <a name="remarks"></a>Notes

Les développeurs de packages d’installation peuvent utiliser la propriété **Privileged** pour rendre l’installation conditionnelle sur la stratégie système, sur l’utilisateur en tant qu’administrateur ou sur une attribution par un administrateur.

en cas d’exécution sur Windows Vista, les **privilèges** et les [**AdminUser**](adminuser.md) sont les mêmes.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




