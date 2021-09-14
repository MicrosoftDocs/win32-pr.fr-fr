---
description: La propriété installed est définie uniquement si le produit est installé par ordinateur ou pour l’utilisateur actuel.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Propriété installed
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae5126107fff51f3790fb3ab9a9209490b9627a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121717"
---
# <a name="installed-property"></a>Propriété installed

La propriété **installed** est définie uniquement si le produit est installé par ordinateur ou pour l’utilisateur actuel. Cette propriété n’est pas définie si le produit est installé pour un autre utilisateur.

La propriété **installed** peut être utilisée dans les expressions conditionnelles pour déterminer si un produit est installé par ordinateur ou pour l’utilisateur actuel. Par exemple, la propriété peut être utilisée dans la colonne conditionnelle d’une table de séquences ou pour faire la différence entre une installation initiale et une installation de maintenance.

Pour déterminer si le produit est installé pour un autre utilisateur, vérifiez la propriété [**ProductState**](productstate.md) .

La valeur de la propriété [**ProductVersion**](productversion.md) est la version du produit au format de chaîne.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




