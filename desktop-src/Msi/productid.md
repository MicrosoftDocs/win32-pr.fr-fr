---
description: La propriété ProductID est définie sur le ProductID complet après une validation réussie. Cette valeur est affichée par l’interface utilisateur et utilisée par l’action RegisterProduct. Après une validation réussie, cette propriété est définie par l’Action ValidateProductID ou le ControlEvent, ValidateProductID. Notez que l’exemple d’interface utilisateur spécifique fourni avec le kit de développement logiciel (SDK) comme Uisample.msi requiert une valeur pour ProductID. Si vous utilisez cette interface utilisateur, mais que vous ne souhaitez pas utiliser ProductID pour valider des identificateurs de produits, définissez la propriété ProductID sur &\# 0034 ; none&\# 0034 ; dans la table des propriétés.
ms.assetid: 6af23f2d-b22a-470d-b979-da32776e0007
title: Propriété ProductID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf616e2bc34ce70deb5f6b63dba7287002d4fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541410"
---
# <a name="productid-property"></a>Propriété ProductID

La propriété **ProductID** est définie sur le **ProductID** complet après une validation réussie.

Cette valeur est affichée par l’interface utilisateur et utilisée par l' [action RegisterProduct](registerproduct-action.md).

Après une validation réussie, cette propriété est définie par l' [Action ValidateProductID](validateproductid-action.md) ou le [ControlEvent, ValidateProductID](validateproductid-controlevent.md).

Notez que l’exemple d’interface utilisateur spécifique fourni avec le kit de développement logiciel (SDK) comme Uisample.msi requiert une valeur pour **ProductID**. Si vous utilisez cette interface utilisateur, mais que vous ne souhaitez pas utiliser **ProductID** pour valider des identificateurs de produit, définissez la propriété **ProductID** sur « None » dans la [table de propriétés](property-table.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




