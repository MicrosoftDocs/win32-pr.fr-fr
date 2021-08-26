---
description: La propriété DVDAdm. BookmarkOnClose définit ou récupère une valeur qui indique à l’objet MSDVDAdm s’il faut enregistrer automatiquement un signet de l’emplacement et des paramètres actuels lorsque l’utilisateur ferme l’application.
ms.assetid: 54901ad6-7989-4fb3-bb28-f54c7a2bca44
title: Propriété BookmarkOnClose
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83ed0ef05e2efe7edb3b6494e8f9709b23259207af257957551077dfbbddaba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103339"
---
# <a name="bookmarkonclose-property"></a>Propriété BookmarkOnClose

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDAdm.BookmarkOnClose` propriété définit ou récupère une valeur qui indique à l’objet MSDVDAdm s’il faut enregistrer automatiquement un signet de l’emplacement et des paramètres actuels lorsque l’utilisateur ferme l’application.

``` syntax
[ bBookmarkOnClose = ] DVD.DVDAdm.BookmarkOnClose
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur booléenne qui, si la valeur est true, indique que le contrôle MSDVDAdm enregistre un signet de tous les paramètres DVD, y compris la position sur le disque, le niveau parental et le pays/région parent lorsque l’utilisateur ferme l’application lecteur DVD.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture et sa valeur par défaut est true.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BookmarkOnStop**](bookmarkonstop-property.md)
</dt> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



