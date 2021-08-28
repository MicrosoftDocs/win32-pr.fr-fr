---
description: Un descripteur HRECOGNIZER est utilisé pour créer un contexte de module de reconnaissance, récupérer les attributs et les propriétés du module de reconnaissance et déterminer les propriétés de paquet requises par le module de reconnaissance pour effectuer la reconnaissance.
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: Handle HRECOGNIZER (Récapitulatifis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192890991dcb7e8b0a0086bbca68a6ccbc2af790d9c7d78e76fe963d268c8240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092449"
---
# <a name="hrecognizer-handle"></a>Handle HRECOGNIZER

Un descripteur **HRECOGNIZER** est utilisé pour créer un contexte de module de reconnaissance, récupérer les attributs et les propriétés du module de reconnaissance et déterminer les propriétés de paquet requises par le module de reconnaissance pour effectuer la reconnaissance.


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a>Remarques

Les fonctions suivantes utilisent un **HRECOGNIZER**.



| Fonction                                                               | Description                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**CreateRecognizer**](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | Crée un module de reconnaissance.<br/>                                                                   |
| [**DestroyRecognizer**](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | Détruit un module de reconnaissance.<br/>                                                                  |
| [**GetRecoAttributes**](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | Retourne les attributs du module de reconnaissance.<br/>                                               |
| [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | Crée un contexte de module de reconnaissance.<br/>                                                           |
| [**DestroyContext**](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | Détruit un contexte de module de reconnaissance.<br/>                                                          |
| [**GetAllRecognizers**](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | Obtient tous les module de reconnaissance.<br/>                                                                   |
| [**GetResultPropertyList**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | Récupère une liste de propriétés que le module de reconnaissance peut retourner pour une plage de résultats.<br/>            |
| [**GetPreferredPacketDescription**](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | Récupère une description de paquet qui contient les propriétés de paquet utilisées par le module de reconnaissance.<br/> |
| [**GetUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | Récupère les plages de points Unicode que le module de reconnaissance prend en charge.<br/>                    |
| [**LoadCachedAttributes**](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | Charge les attributs mis en cache d’un module de reconnaissance.<br/>                                            |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                        |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Récapitulatif</dt> </dl> |



 

 




