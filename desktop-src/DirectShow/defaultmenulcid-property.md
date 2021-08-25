---
description: La propriété DVDAdm. DefaultMenuLCID définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour les menus.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: Propriété DefaultMenuLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 939f65ad41cb184f38e2a30392030ca67066fe203f7952441cc2f77b1db95242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906889"
---
# <a name="defaultmenulcid-property"></a>Propriété DefaultMenuLCID

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDAdm.DefaultMenuLCID` propriété définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour les menus.

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le LCID tel qu’il est stocké dans les paramètres du Registre pour l’application DVD. Cette valeur n’est pas nécessairement la même que la langue de menu par défaut créée sur le DVD. Pour connaître la plage de LCID valides, consultez la documentation Win32 dans le kit de développement logiciel (SDK) de plateforme.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture sans valeur par défaut. Si aucun LCID de menu par défaut n’est spécifié, l’objet MSDVDAdm utilise la langue qui est marquée en tant que langue de menu par défaut sur le disque.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



