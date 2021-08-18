---
description: La propriété DVDAdm. DefaultSubpictureLCID définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour le flux de sous-image.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: Propriété DefaultSubpictureLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc67be112349a050df45f625fda6488c91b22dee357c820724de5842c156894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952988"
---
# <a name="defaultsubpicturelcid-property"></a>Propriété DefaultSubpictureLCID

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDAdm.DefaultSubpictureLCID` propriété définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour le flux de sous-image.

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le LCID de sous-image par défaut spécifié par l’utilisateur, tel qu’il est stocké dans les paramètres du Registre pour l’application DVD. Cette valeur n’est pas nécessairement identique au flux de sous-image par défaut tel qu’il a été créé sur le DVD. Pour connaître la plage de LCID valides, consultez la documentation Win32 dans le kit de développement logiciel (SDK) de plateforme.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture sans valeur par défaut. Si aucun LCID de sous-image par défaut n’est spécifié, l’objet MSDVDAdm lira le flux de sous-image qui est marqué comme flux par défaut sur le disque.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



