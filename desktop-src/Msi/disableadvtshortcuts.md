---
description: La définition de la propriété DISABLEADVTSHORTCUTS désactive la génération de raccourcis prenant en charge l’installation à la demande et la publication. La définition de cette propriété spécifie que ces raccourcis doivent plutôt être remplacés par des raccourcis standard.
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: Propriété DISABLEADVTSHORTCUTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86fd8465620abab56ebfe18f68254bf6d29b6e752a7550157231a0b1abe95ecd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745559"
---
# <a name="disableadvtshortcuts-property"></a>Propriété DISABLEADVTSHORTCUTS

La définition de la propriété **DISABLEADVTSHORTCUTS** désactive la génération de raccourcis prenant en charge l' [installation à la demande](installation-on-demand.md) et la [publication](advertisement.md). La définition de cette propriété spécifie que ces raccourcis doivent plutôt être remplacés par des raccourcis standard.

## <a name="default-value"></a>Valeur par défaut

Par défaut, la génération de raccourcis d’installation à la demande est activée.

## <a name="remarks"></a>Remarques

Les raccourcis qui prennent en charge la publication ont le nom d’une fonctionnalité, plutôt qu’un chemin de fichier mis en forme au format \[ \# filekey \] , entré dans la colonne cible de la [table de raccourcis](shortcut-table.md). Si cette propriété est définie et que la fonctionnalité est installée, le programme d’installation génère un raccourci standard vers la fonctionnalité.

Cette propriété est couramment utilisée par les administrateurs pour les utilisateurs qui se déplacent entre des environnements qui ne prennent pas en charge la publicité. Cette propriété peut être définie par une transformation, dans le flux d’administration, ou dans la [table de propriétés](property-table.md). S’il est défini à l’aide de la ligne de commande ou d’un appel à [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), il doit être réinitialisé à nouveau lors de chaque installation suivante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




