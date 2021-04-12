---
description: La propriété DVDAdm. DefaultMenuLCID définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour les menus.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: Propriété DefaultMenuLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907fbef0d04306b5ddc4f9a59749c96573d05bb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109618"
---
# <a name="defaultmenulcid-property"></a>Propriété DefaultMenuLCID

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDAdm.DefaultMenuLCID` propriété définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour les menus.

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le LCID tel qu’il est stocké dans les paramètres du Registre pour l’application DVD. Cette valeur n’est pas nécessairement la même que la langue de menu par défaut créée sur le DVD. Pour connaître la plage de LCID valides, consultez la documentation Win32 dans le kit de développement logiciel (SDK) de plateforme.

## <a name="remarks"></a>Notes

Cette propriété est en lecture/écriture sans valeur par défaut. Si aucun LCID de menu par défaut n’est spécifié, l’objet MSDVDAdm utilise la langue qui est marquée en tant que langue de menu par défaut sur le disque.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



