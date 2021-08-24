---
description: Le programme d’installation définit la propriété RollbackDisabled lorsque la restauration a été désactivée.
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: Propriété RollbackDisabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1df5b392a69a04811853a449106858445969fed3b2c0598266ff3f8a1bcb51a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039869"
---
# <a name="rollbackdisabled-property"></a>Propriété RollbackDisabled

Le programme d’installation définit la propriété **RollbackDisabled** lorsque la restauration a été désactivée. **RollbackDisabled** est utilisé par les auteurs du package qui doivent s’assurer que le programme d’installation n’a pas désactivé la restauration. La propriété **RollbackDisabled** peut être utilisée dans une expression conditionnelle qui refuse effectivement de poursuivre l’installation si la propriété **RollbackDisabled** est définie.

## <a name="default-value"></a>Valeur par défaut

Par défaut, la restauration est activée.

## <a name="remarks"></a>Remarques

Étant donné que la [restauration](rollback-custom-actions.md) et la [validation](commit-custom-actions.md) ne sont pas exécutées alors que la restauration est désactivée, le programme d’installation ne peut pas installer correctement un package qui utilise ces types d’actions personnalisées dans une transaction au cours de l’installation. Dans ce cas, l’auteur du package doit inclure une condition utilisant DisableRollback, qui empêche l’installation de se poursuivre si la restauration est désactivée.

La valeur de la stratégie DisableRollback peut être définie par un administrateur dans le cadre de l’attribution de la stratégie système. Les administrateurs sont invités à ne pas désactiver la restauration, sauf si cela est nécessaire. Pour plus d’informations sur la valeur de stratégie DisableRollback, consultez [stratégie système](system-policy.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Restauration de l’installation](rollback-installation.md)
</dt> <dt>

[Stratégie système](system-policy.md)
</dt> <dt>

[restaurer les actions personnalisées](rollback-custom-actions.md)
</dt> <dt>

[valider des actions personnalisées](commit-custom-actions.md)
</dt> </dl>

 

 




