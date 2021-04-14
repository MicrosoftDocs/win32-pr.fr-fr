---
description: La propriété DVDAdm. DefaultSubpictureLCID définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour le flux de sous-image.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: Propriété DefaultSubpictureLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f52227dc220bef474e872cbd695c78dc65f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522783"
---
# <a name="defaultsubpicturelcid-property"></a>Propriété DefaultSubpictureLCID

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDAdm.DefaultSubpictureLCID` propriété définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour le flux de sous-image.

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le LCID de sous-image par défaut spécifié par l’utilisateur, tel qu’il est stocké dans les paramètres du Registre pour l’application DVD. Cette valeur n’est pas nécessairement identique au flux de sous-image par défaut tel qu’il a été créé sur le DVD. Pour connaître la plage de LCID valides, consultez la documentation Win32 dans le kit de développement logiciel (SDK) de plateforme.

## <a name="remarks"></a>Notes

Cette propriété est en lecture/écriture sans valeur par défaut. Si aucun LCID de sous-image par défaut n’est spécifié, l’objet MSDVDAdm lira le flux de sous-image qui est marqué comme flux par défaut sur le disque.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



