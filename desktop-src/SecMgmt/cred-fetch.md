---
description: Définit des valeurs qui déterminent la manière de récupérer les informations d’identification d’un compte de service administré de groupe (gMSA).
ms.assetid: 90891448-22F6-497A-A612-3DAB8622C325
title: Énumération CRED_FETCH (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRED_FETCH
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 6a7c30f29826b017bc7a3badd796955ec31a1ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952506"
---
# <a name="cred_fetch-enumeration"></a>\_Énumération d’extraction de cred

Définit des valeurs qui déterminent la manière de récupérer les informations d’identification d’un compte de service administré de groupe (gMSA).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _CRED_FETCH { 
  CredFetchDefault  = 0,
  CredFetchDPAPI    = 1,
  CredFetchForced   = 2
} CRED_FETCH;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**
</dt> <dd>

Signifie que le système d’exploitation doit tout d’abord tenter de récupérer le mot de passe à partir du cache local. S’il est temps de récupérer le mot de passe, le système d’exploitation doit contacter un contrôleur de domaine pour le mot de passe. En cas d’échec, retourne tous les mots de passe mis en cache avec la valeur d’État Success.

</dd> <dt>

<span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**
</dt> <dd>

Retourne les informations d’identification DPAPI locales à l’appelant. Les fournisseurs SSP ( [*Security Support Provider*](/windows/desktop/SecGloss/s-gly) ) ne nécessitent généralement pas l’utilisation de cette énumération.

</dd> <dt>

<span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**
</dt> <dd>

Force le système d’exploitation à tenter de lire le mot de passe à partir du contrôleur de domaine. Pendant l’heure de substitution du mot de passe, le mot de passe peut avoir changé au niveau du contrôleur de domaine et d’autres hôtes membres, mais l’hôte du membre gMSA reconnaît le mot de passe comme étant toujours valide. Cela peut se produire en raison de problèmes d’inclinaison de l’horloge entre les différents contrôleurs de domaine. Lorsque cette valeur est spécifiée, le système d’exploitation détermine s’il peut y avoir une possibilité de modification de mot de passe en raison de l’inclinaison de l’horloge et, le cas échéant, récupère le mot de passe. Dans le cas contraire, les informations d’identification mises en cache sont retournées. S’il n’y a pas d’informations d’identification mises en cache, le système d’exploitation tente d’en récupérer un à partir du contrôleur de domaine.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Secpkg. h</dt> </dl> |



 

