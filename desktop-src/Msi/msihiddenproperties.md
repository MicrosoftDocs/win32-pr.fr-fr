---
description: La propriété MsiHiddenProperties peut être utilisée pour empêcher le programme d’installation d’afficher des mots de passe ou d’autres informations confidentielles dans le fichier journal.
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: Propriété MsiHiddenProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6124f7002edd8ab7d3d5e6691b7b0a322b93c285
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011849"
---
# <a name="msihiddenproperties-property"></a>Propriété MsiHiddenProperties

La propriété **MsiHiddenProperties** peut être utilisée pour empêcher le programme d’installation d’afficher des mots de passe ou d’autres informations confidentielles dans le fichier journal. Pour empêcher une propriété d’être écrite dans le fichier journal, définissez la valeur de la propriété **MsiHiddenProperties** sur le nom de la propriété que vous souhaitez masquer. Vous pouvez masquer plusieurs propriétés en spécifiant une chaîne de noms de propriétés délimitée par des points-virgules (;).

> [!Note]  
> Lorsque la stratégie de [débogage](debug.md) est définie sur 7, le programme d’installation écrit les informations entrées sur une ligne de commande dans le journal. Cela rend les propriétés publiques entrées sur une ligne de commande visibles, même si la propriété est incluse dans la propriété **MsiHiddenProperties** . Cela peut rendre les informations confidentielles entrées sur une ligne de commande visible dans le journal. Pour plus d’informations, consultez [la page empêcher l’écriture d’informations confidentielles dans le fichier journal](preventing-confidential-information-from-being-written-into-the-log-file.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




