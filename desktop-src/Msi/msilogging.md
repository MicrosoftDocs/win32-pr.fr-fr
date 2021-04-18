---
description: La propriété MsiLogging définit le mode de journalisation par défaut pour le package Windows Installer.
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: Propriété MsiLogging
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e53df57723157f7184a904e512aac9035a9f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526654"
---
# <a name="msilogging-property"></a>Propriété MsiLogging

La propriété **MsiLogging** définit le mode de journalisation par défaut pour le package Windows Installer. Si cette propriété facultative est présente dans la [table de propriétés](property-table.md), le programme d’installation génère un fichier journal nommé MSI \* . Sign. Le chemin d’accès complet au fichier journal est donné par la valeur de la propriété [**MsiLogFileLocation**](msilogfilelocation.md) .

## <a name="value"></a>Valeur

La valeur de cette propriété doit être une chaîne des caractères suivants qui spécifient le mode de journalisation par défaut.



| Valeur                                                                        | Signification                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>Cliqu</dt> </dl> | Messages d’État.<br/>                                                    |
| <dl> <dt>w</dt> </dl> | Avertissements non irrécupérables.<br/>                                                  |
| <dl> <dt>Envoyer</dt> </dl> | Tous les messages d’erreur.<br/>                                                 |
| <dl> <dt>un</dt> </dl> | Démarrage des actions.<br/>                                                |
| <dl> <dt>r</dt> </dl> | Enregistrements spécifiques aux actions.<br/>                                            |
| <dl> <dt>u</dt> </dl> | Demandes de l’utilisateur.<br/>                                                      |
| <dl> <dt>c</dt> </dl> | Paramètres initiaux de l’interface utilisateur.<br/>                                              |
| <dl> <dt>m</dt> </dl> | Informations de sortie insuffisantes ou irrécupérables.<br/>                            |
| <dl> <dt>o</dt> </dl> | Messages d’espace disque insuffisants.<br/>                                         |
| <dl> <dt>p</dt> </dl> | Propriétés du terminal.<br/>                                                |
| <dl> <dt>v</dt> </dl> | Sortie détaillée.<br/>                                                     |
| <dl> <dt>x</dt> </dl> | Informations supplémentaires sur le débogage. Disponible uniquement sur Windows Server 2003.<br/> |
| <dl> <dt>!</dt> </dl> | Videz chaque ligne dans le journal.<br/>                                         |



 

## <a name="remarks"></a>Notes

Cette propriété est disponible à partir de Windows Installer 4,0.

Vous ne pouvez pas utiliser les valeurs « + » et « \* » de l’option/l dans la valeur de la propriété **MsiLogging** .

Le mode de journalisation peut être défini à l’aide d’une stratégie, d’une option de ligne de commande ou par programme. Cela remplace le mode de journalisation par défaut. Pour plus d’informations sur toutes les méthodes qui sont disponibles pour définir le mode de journalisation, consultez [journalisation normale](normal-logging.md) dans la section [journalisation Windows Installer](windows-installer-logging.md) .

Si la propriété **MsiLogging** est présente dans la [table de propriétés](property-table.md), le mode de journalisation par défaut du package peut être modifié en modifiant la valeur de cette propriété à l’aide d’une [transformation de base de données](database-transforms.md). Le mode de journalisation par défaut ne peut pas être modifié à l’aide d’un [package correctif](patch-packages.md) (un fichier. msp).

Si la propriété **MsiLogging** a été définie dans la [table de propriétés](property-table.md), le mode de journalisation par défaut pour tous les utilisateurs de l’ordinateur peut être spécifié en définissant la stratégie [DisableLoggingFromPackage](disableloggingfrompackage.md) et la stratégie de [journalisation](logging.md) . La définition de la stratégie DisableLoggingFromPackage et de la stratégie de journalisation remplace la propriété **MsiLogging** pour tous les packages.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 4,5 sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




