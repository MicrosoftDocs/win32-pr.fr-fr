---
description: 'les valeurs de registre WFP se trouvent dans la clé de registre suivante : HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon.'
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: Valeurs de Registre WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a363a462e32d797b2032d222d6c6195a65493481668620401bc31daa3eb53fb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999179"
---
# <a name="wfp-registry-values"></a>Valeurs de Registre WFP

\[les valeurs de registre WFP ne sont pas prises en charge à partir de Windows Vista.\]

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

 

 



