---
description: Pendant une installation simultanée, le programme d’installation définit la propriété ParentOriginalDatabase dans la session de l’installation simultanée sur la même valeur que la propriété OriginalDatabase dans la session de l’installation parente.
ms.assetid: 8af1c7e5-313c-47b7-be0f-0e31ef21f6a6
title: Propriété ParentOriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab69dff7058336a5b68fd3373100f4789059ed7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545549"
---
# <a name="parentoriginaldatabase-property"></a>Propriété ParentOriginalDatabase

Pendant une installation simultanée, le programme d’installation définit la propriété **ParentOriginalDatabase** dans la session de l’installation simultanée sur la même valeur que la propriété [**OriginalDatabase**](originaldatabase.md) dans la session de l’installation parente. Les installations parentes utilisent les actions d’installation simultanées pour effectuer une installation simultanée. Un package d’installation peut déterminer s’il est installé par une action d’installation simultanée en vérifiant la valeur de cette propriété.

> [!Note]  
> Les installations simultanées ne sont pas recommandées pour l’installation d’applications destinées à être communiquées au public. Pour plus d’informations sur les installations simultanées, consultez [installations simultanées](concurrent-installations.md).

 

> [!Note]  
> Cette propriété n’est pas définie si l’installation simultanée est exécutée par l’action [RemoveExistingProducts](removeexistingproducts-action.md) .

 

## <a name="remarks"></a>Notes

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
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[**ParentProductCode**](parentproductcode.md)
</dt> </dl>

 

 




