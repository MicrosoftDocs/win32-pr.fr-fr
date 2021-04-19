---
description: La propriété installed est définie uniquement si le produit est installé par ordinateur ou pour l’utilisateur actuel.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Propriété installed
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae5126107fff51f3790fb3ab9a9209490b9627a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531004"
---
# <a name="installed-property"></a>Propriété installed

La propriété **installed** est définie uniquement si le produit est installé par ordinateur ou pour l’utilisateur actuel. Cette propriété n’est pas définie si le produit est installé pour un autre utilisateur.

La propriété **installed** peut être utilisée dans les expressions conditionnelles pour déterminer si un produit est installé par ordinateur ou pour l’utilisateur actuel. Par exemple, la propriété peut être utilisée dans la colonne conditionnelle d’une table de séquences ou pour faire la différence entre une installation initiale et une installation de maintenance.

Pour déterminer si le produit est installé pour un autre utilisateur, vérifiez la propriété [**ProductState**](productstate.md) .

La valeur de la propriété [**ProductVersion**](productversion.md) est la version du produit au format de chaîne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




