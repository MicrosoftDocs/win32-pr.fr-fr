---
description: Le programme d’installation définit la valeur de la propriété UserSID sur la représentation sous forme de chaîne de l’identificateur de sécurité (SID) de l’utilisateur qui exécute l’installation. Pour plus d’informations, consultez structures d’autorisation.
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: UserSID, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26185c886117b39355241151ffef6d8615bd5f8d10a7f50bd5937a301f7b398
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809159"
---
# <a name="usersid-property"></a>UserSID, propriété

Le programme d’installation définit la valeur de la propriété **UserSid** sur la représentation sous forme de chaîne de l’identificateur de sécurité (SID) de l’utilisateur qui exécute l’installation. Pour plus d’informations, consultez [structures d’autorisation](../secauthz/authorization-structures.md).

## <a name="default-value"></a>Valeur par défaut

Aucun.

## <a name="remarks"></a>Notes

la Windows Installer définir cette propriété sur Windows 2000, Windows XP et Windows Vista. Cette propriété n’est pas définie sur tous les autres systèmes d’exploitation.

Notez que cette propriété a l’attribut spécial qu’elle peut être récupérée à partir d’une action personnalisée différée. Une action personnalisée exécutée avec des privilèges élevés peut toujours retourner le SID de l’utilisateur dans la propriété **UserSid** . Pour plus d’informations, consultez [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 
