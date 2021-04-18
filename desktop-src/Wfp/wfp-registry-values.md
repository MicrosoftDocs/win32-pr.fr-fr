---
description: 'Les valeurs de Registre WFP se trouvent dans la clé de Registre suivante : HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon.'
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: Valeurs de Registre WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb8db23800ebbead68f34eaf0fa9fffd772f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533680"
---
# <a name="wfp-registry-values"></a>Valeurs de Registre WFP

\[Les valeurs de Registre WFP ne sont pas prises en charge à partir de Windows Vista.\]

WFP utilise plusieurs valeurs de Registre pour les paramètres de personnalisation. Les valeurs de Registre WFP se trouvent dans la clé de Registre suivante :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
```

Voici les valeurs de Registre WFP.

<dl> <dt>

<span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**
</dt> <dd>

Emplacement du cache. Il doit s’agir d’un chemin d’accès local. La valeur par défaut est% SystemRoot% \\ system32 \\ dllcache.

</dd> <dt>

<span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**
</dt> <dd>

Options de quota. Cette valeur de Registre peut être l’une des valeurs suivantes.



| Valeur                  | Signification                                                  |
|------------------------|----------------------------------------------------------|
| QUOTA SFC- \_ \_ tous les \_ fichiers | La taille du cache DLL est illimitée. Il s’agit de la valeur par défaut. |
| Autres valeurs           | Taille du cache DLL, dans les fichiers.                         |



 

</dd> <dt>

<span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**
</dt> <dd>

Options d’analyse. Cette valeur de Registre peut être l’une des valeurs suivantes.



| Valeur             | Signification                                                   |
|-------------------|-----------------------------------------------------------|
| \_analyse SFC \_ normale | N’analyse pas les fichiers protégés au démarrage. Il s’agit de la valeur par défaut. |
| \_toujours analyser \_ SFC | Analyser les fichiers protégés à chaque démarrage.                       |
| \_analyse SFC \_ une seule fois   | Analyser les fichiers protégés au prochain démarrage.                    |



 

</dd> </dl>

 

 



