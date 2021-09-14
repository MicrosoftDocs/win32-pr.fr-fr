---
description: AppInit_DLLs dans Windows 7 et Windows Server 2008 R2
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs dans Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820fcb9840bbec139ff78f3c6cc082b2dca4eeb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127216769"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a>\_dll AppInit dans Windows 7 et Windows Server 2008 R2

## <a name="platform"></a>Plateforme

**Clients** -Windows 7  
**serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -faible  





## <a name="description"></a>Description

\_Les DLL AppInit sont un mécanisme qui permet de charger une liste arbitraire de dll dans chaque processus en mode utilisateur sur le système. Microsoft modifie la fonction des dll AppInit dans Windows 7 et Windows Server 2008 R2 pour ajouter une nouvelle exigence de signature de code. Cela vous aidera à améliorer la fiabilité et les performances du système, ainsi qu’à améliorer la visibilité de l’origine des logiciels.

## <a name="configuration"></a>Configuration

les valeurs stockées sous la \_ \_ clé de la Windows du logiciel HKEY LOCAL MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ dans le registre déterminent le comportement de l' \_ infrastructure des dll AppInit. Le tableau ci-dessous décrit les valeurs de Registre suivantes :



<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Description</th>
<th>Exemples de valeurs</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">LoadAppInit_DLLs (REG_DWORD) $ {REMOVE} $<br />
</td>
<td rowspan="2">Active ou désactive globalement AppInit_DLLs. $ {REMOVE} $<br />
</td>
<td>0x0 – AppInit_DLLs sont désactivés.</td>
</tr>
<tr class="even">
<td>0x1 – AppInit_DLLs sont activés.</td>


</tr>
<tr class="odd">
<td>AppInit_DLLs (REG_SZ)</td>
<td>Espace ou liste délimitée par des virgules des dll à charger. Le chemin d’accès complet à la DLL doit être spécifié à l’aide de noms courts.</td>
<td>C:\ PROGRA ~ 1 \ WID288 ~ 1 \ MICROS ~1.DLL</td>
</tr>
<tr class="even">
<td rowspan="2">RequireSignedAppInit_DLLs (REG_DWORD) $ {REMOVE} $<br />
</td>
<td rowspan="2">Charge uniquement les dll signées par code. $ {REMOVE} $<br />
</td>
<td>0x0 – charger les dll.</td>
</tr>
<tr class="odd">
<td>0x1 : charge uniquement les dll signées par le code.</td>


</tr>
</tbody>
</table>



 

**Windows 7**

Toutes les dll qui sont chargées par l' \_ infrastructure des DLL AppInit doivent être signées par un code. dans l’intérêt de la compatibilité des applications, le système d’exploitation Windows 7 charge toutes les dll AppInit. toutefois, Microsoft recommande à tous les développeurs d’applications de signer le code de leurs dll afin d’améliorer la fiabilité des Windows et de se préparer à la mise en œuvre de la signature de code dans les futures versions de Windows. la \_ clé de registre RequireSignedAppInit dll contrôle ce comportement et sa valeur sur Windows 7 est définie par défaut sur 0.

**Windows Server 2008 R2**

Toutes les dll qui sont chargées par l' \_ infrastructure des DLL AppInit doivent être signées par un code. la \_ clé de registre RequireSignedAppInit dll contrôle ce comportement et sa valeur sur Windows Server 2008 R2 est définie sur 1 par défaut.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

<dl>

[dll AppInit dans Windows 7 et Windows Server 2008 R2](/windows-hardware/drivers/install/)  
</dl>

 

 
