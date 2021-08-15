---
description: la propriété Intel est définie par la Windows Installer au niveau du processeur numérique lors de l’exécution sur un processeur Intel.
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Intel, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd5b4fe488867a67da1f97ce4564bb8ce530b89417554a91a8734bee6e863f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013237"
---
# <a name="intel-property"></a>Intel, propriété

la propriété **Intel** est définie par la Windows Installer au niveau du processeur numérique lors de l’exécution sur un processeur Intel. Les valeurs sont les mêmes que celles du champ *wProcessorLevel* de la structure des [**\_ informations système**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) . lors de l’exécution sur un processeur x64, le Windows Installer définit la propriété **Intel** pour refléter le processeur x86 émulé par l’ordinateur x64, comme indiqué par le système d’exploitation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 
