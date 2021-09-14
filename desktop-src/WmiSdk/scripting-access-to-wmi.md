---
description: Les scripts peuvent accéder à toutes les classes WMI pour les objets matériels et logiciels.
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: Écriture de scripts pour l’accès à WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd487c127c670f9ddee9596e44c4b2b9691ed880
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291867"
---
# <a name="scripting-access-to-wmi"></a>Écriture de scripts pour l’accès à WMI

Les scripts peuvent accéder à toutes les classes WMI pour les objets matériels et logiciels. Windows Les scripts d’hôte de script (WSH) peuvent effectuer des opérations sur les objets du système de fichiers, manipuler les imprimantes réseau ou modifier les variables d’environnement. Vous pouvez trouver une variété de tâches d’administration et des conseils sur la façon de les accomplir dans WMI à l’aide [des tâches WMI pour les scripts et les applications](wmi-tasks-for-scripts-and-applications.md). Pour plus d’informations et d’exemples, consultez le [référentiel de scripts](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx)technet scriptcenter.

Si vous débutez avec des scripts ou des scripts spécifiques à WMI, consultez la section TechNet ScriptCenter [prise en main](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).

Avec l' [API de script pour WMI](scripting-api-for-wmi.md), vous pouvez développer des scripts rapides, simples ou des applications complexes. Les scripts vous permettent d’obtenir des informations ou de configurer la plupart des objets d’une entreprise, comme vous le feriez par le biais d’une application C++ ou C#. Pour plus d’informations, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Vous ne pouvez pas écrire de [*fournisseur WMI*](gloss-p.md) dans un script. Pour plus d’informations, consultez [fourniture de données à WMI](providing-data-to-wmi.md).

les scripts WMI peuvent être écrits dans n’importe quel langage de script pouvant interagir avec les objets ActiveX.

Windows PowerShell fournit un environnement simple pour l’administration et l’écriture de scripts WMI. Pour plus d’informations sur PowerShell, consultez [prise en main avec Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).

Les scripts ADSI (Active Directory Service Interfaces) fournissent l’accès aux objets Active Directory Domain Services (AD DS). Les scripts WSH et ADSI accèdent aux objets et autorisent les procédures non disponibles par le biais de fichiers de commandes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de WMI](about-wmi.md)
</dt> <dt>

[API de script pour WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
