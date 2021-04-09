---
description: Les fournisseurs d’associations permettent aux clients Windows Management Instrumentation (WMI) de traverser et de récupérer des profils et des instances de classe associées à partir d’espaces de noms différents.
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: Accès aux données dans l’espace de noms Interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a217a7a44651b1a6c94476b53193eedac7f0d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952866"
---
# <a name="accessing-data-in-the-interop-namespace"></a>Accès aux données dans l’espace de noms Interop

Les fournisseurs d’associations permettent aux clients Windows Management Instrumentation (WMI) de traverser et de récupérer des profils et des instances de classe associées à partir d’espaces de noms différents.

Les fournisseurs d’associations et les classes résident dans l' \\ \\ \\ espace de noms Interop racine. Pour plus d’informations, consultez parcours d’association d’un [espace de noms croisé](cross-namespace-association-traversal.md) et [écriture d’un fournisseur d’associations](writing-an-association-provider-for-interop.md).

Les fournisseurs d’associations exposent des profils standard, comme un profil d’alimentation. Les exemples suivants utilisent le profil d’alimentation pour illustrer la découverte et l’accès aux données par le biais de l’espace de noms Interop.

Windows PowerShell fournit un mécanisme simple pour parcourir l’Association appropriée, récupérer un profil d’appareil et appeler une méthode.

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a>Énumération des profils dans l’espace de noms root/Interop

La commande Windows PowerShell suivante énumère les profils pris en charge par la force de gestion distribuée ([DMTF](https://www.dmtf.org/standards/wsman)) sur un ordinateur Windows 7 :


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a>Récupération des instances d’un profil d’appareil spécifique

La commande Windows PowerShell suivante retourne toutes les instances d’un profil spécifié par le biais de [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)):


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a>Affectation du profil d’alimentation à une variable

La commande Windows PowerShell suivante affecte l’instance de profil d’alimentation à une variable :


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a>Énumération des modes de gestion de l’alimentation d’un ordinateur

La commande Windows PowerShell suivante énumère les plans de profil d’alimentation disponibles :


```PowerShell
$pplan
```



## <a name="calling-a-method"></a>Appel d'une méthode

La commande Windows PowerShell suivante appelle la méthode [**Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) pour le mode de gestion de l’alimentation :


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Traversée des associations entre espaces de noms](cross-namespace-association-traversal.md)
</dt> <dt>

[Écriture d’un fournisseur d’association](writing-an-association-provider-for-interop.md)
</dt> <dt>

[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**\_PowerPlan Win32**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))
</dt> </dl>

 

 
