---
description: La propriété DVDAdm. DefaultAudioLCID définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour le flux audio.
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: Propriété DefaultAudioLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe302adaa555d59b2c1dcd50d749e9afdc2de740
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515752"
---
# <a name="defaultaudiolcid-property"></a>Propriété DefaultAudioLCID

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDAdm.DefaultAudioLCID` propriété définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour le flux audio.

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le LCID audio par défaut spécifié par l’utilisateur, tel qu’il est stocké dans les paramètres du Registre pour l’application DVD. Cette valeur n’est pas nécessairement identique à celle du flux audio par défaut tel qu’il a été créé sur le DVD.

## <a name="remarks"></a>Notes

Cette propriété est en lecture/écriture sans valeur par défaut. Si aucun LCID audio par défaut n’est spécifié, l’objet MSDVDAdm lira le flux audio qui est marqué comme flux par défaut sur le disque.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



