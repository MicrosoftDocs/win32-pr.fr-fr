---
description: La propriété Privileged indique si l’installation est effectuée dans le contexte de privilèges élevés.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Privileged, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfe61f17e5ef3453021c98bac8eb383171a678adfb204886ecdaa840e0df832
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129129"
---
# <a name="privileged-property"></a>Privileged, propriété

La propriété **Privileged** indique si l’installation est effectuée dans le contexte de privilèges élevés. Le programme d’installation définit cette propriété si l’utilisateur dispose de privilèges d’administrateur, si l’application a été affectée par un administrateur système, ou si les stratégies d’utilisateur et d’ordinateur AlwaysInstallElevated a sont définies sur true.

## <a name="default-value"></a>Valeur par défaut

Le programme d’installation ne définit pas cette propriété si l’utilisateur n’est pas autorisé à installer avec des privilèges élevés.

## <a name="remarks"></a>Remarques

Les développeurs de packages d’installation peuvent utiliser la propriété **Privileged** pour rendre l’installation conditionnelle sur la stratégie système, sur l’utilisateur en tant qu’administrateur ou sur une attribution par un administrateur.

en cas d’exécution sur Windows Vista, les **privilèges** et les [**AdminUser**](adminuser.md) sont les mêmes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




