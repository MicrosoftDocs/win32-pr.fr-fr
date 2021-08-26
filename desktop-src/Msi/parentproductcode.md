---
description: Pendant une installation simultanée, le programme d’installation définit la propriété ParentProductCode dans la session de l’installation simultanée sur la même valeur que la propriété ProductCode dans la session de l’installation parente.
ms.assetid: 7bf2b9b1-9efd-4d47-9fa3-253421f1ba4f
title: Propriété ParentProductCode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a56e7a120455723eb95f2bd7f5ea08c59894d3a1951aeb042afb30e3b0e2fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042449"
---
# <a name="parentproductcode-property"></a>Propriété ParentProductCode

Pendant une installation simultanée, le programme d’installation définit la propriété **ParentProductCode** dans la session de l’installation simultanée sur la même valeur que la propriété [**ProductCode**](productcode.md) dans la session de l’installation parente. Les installations parentes exécutent les actions d’installation simultanée pour effectuer une installation simultanée. Un package d’installation peut déterminer s’il est installé par une action d’installation simultanée en vérifiant la valeur de cette propriété.

> [!Note]  
> Les installations simultanées ne sont pas recommandées pour l’installation d’applications destinées à être communiquées au public. Pour plus d’informations sur les installations simultanées, consultez [installations simultanées](concurrent-installations.md).

 

> [!Note]  
> Cette propriété n’est pas définie si l’installation simultanée est exécutée par l’action [RemoveExistingProducts](removeexistingproducts-action.md) .

 

## <a name="remarks"></a>Remarques

Pour empêcher l’installation d’un package en tant qu’installation simultanée, ajoutez l’une des instructions conditionnelles suivantes à la table [LaunchCondition](launchcondition-table.md) . Cela évite que le package ne soit installé par une action d’installation simultanée exécutée par une autre installation. Cela n’empêche pas l’installation du package par l’action [RemoveExistingProducts](removeexistingproducts-action.md) .

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[**ParentOriginalDatabase**](parentoriginaldatabase.md)
</dt> </dl>

 

 




