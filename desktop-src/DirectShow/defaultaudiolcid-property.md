---
description: La propriété DVDAdm. DefaultAudioLCID définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour le flux audio.
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: Propriété DefaultAudioLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7ebcd864f8ac3bff8cfd8556703dd091985a72c0dfea4f0eefb9f974213165
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953004"
---
# <a name="defaultaudiolcid-property"></a>Propriété DefaultAudioLCID

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDAdm.DefaultAudioLCID` propriété définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour le flux audio.

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le LCID audio par défaut spécifié par l’utilisateur, tel qu’il est stocké dans les paramètres du Registre pour l’application DVD. Cette valeur n’est pas nécessairement identique à celle du flux audio par défaut tel qu’il a été créé sur le DVD.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture sans valeur par défaut. Si aucun LCID audio par défaut n’est spécifié, l’objet MSDVDAdm lira le flux audio qui est marqué comme flux par défaut sur le disque.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



