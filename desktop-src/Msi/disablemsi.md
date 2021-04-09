---
description: Si la valeur de cette stratégie système par ordinateur est définie sur &\# 0034 ; 2&\# 0034 ; le programme d’installation est toujours désactivé pour toutes les applications. Si cette valeur de stratégie est définie sur &\# 0034 ; 1&\# 0034 ;, le programme d’installation est désactivé pour les applications non gérées, mais il est toujours activé pour les applications managées.
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf8a784f5e8090bf6ba2007091c22cf4bc070c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034647"
---
# <a name="disablemsi"></a>DisableMSI

Si la valeur de cette [stratégie système](system-policy.md) par ordinateur est définie sur « 2 », le programme d’installation est toujours désactivé pour toutes les applications. Si cette valeur de stratégie est définie sur « 1 », le programme d’installation est désactivé pour les applications non gérées, mais il est toujours activé pour les applications managées.

Le tableau suivant répertorie les configurations possibles.



| DisableMSI | Description                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Par défaut*  | Sur Windows Server 2003, Windows Server 2003 R2, Windows Server 2008 et Windows Server 2008 R2, si la valeur de stratégie est null, absente ou un nombre autre que 1 ou 2, le Windows Installer est activé pour les applications managées. Les installations d’applications non gérées sont bloquées.<br/> Sur Windows XP, Windows Vista et Windows 7, le Windows Installer est activé pour toutes les applications. Toutes les opérations d’installation sont autorisées.<br/> |
| 0          | Windows Installer est activé pour toutes les applications. Toutes les opérations d’installation sont autorisées.                                                                                                                                                                                                                                                                                                                                                      |
| 1          | La Windows Installer est désactivée pour les applications non managées, mais elle est toujours activée pour les applications managées. Les installations par utilisateur non élevées sont bloquées. Les installations par utilisateur avec élévation de privilèges et par ordinateur sont autorisées.                                                                                                                                                                                                                        |
| 2          | Windows Installer est toujours désactivée pour toutes les applications. Aucune installation n’est autorisée, y compris les réparations, les réinstallations ou les installations à la demande.                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




