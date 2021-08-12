---
description: La propriété DVDAdm. BookmarkOnStop définit ou récupère une valeur qui indique à l’objet MSWebDVD s’il faut enregistrer automatiquement un signet de l’emplacement et des paramètres actuels lorsque l’utilisateur clique sur le bouton arrêter.
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: Propriété BookmarkOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c73d8b9829075125437e05da96c78d101f5a7f5df4dc2decc25f044cc3f5f27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662671"
---
# <a name="bookmarkonstop-property"></a>Propriété BookmarkOnStop

La `DVDAdm.BookmarkOnStop` propriété définit ou récupère une valeur qui indique à l’objet mswebdvd s’il faut enregistrer automatiquement un signet de l’emplacement et des paramètres actuels lorsque l’utilisateur clique sur le bouton **arrêter** .

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur booléenne indiquant si l’objet MSDVDAdm enregistre un signet de tous les paramètres DVD, y compris la position sur le disque, le niveau parental et le pays/région parent.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture et sa valeur par défaut est false.

Les signets sont valides uniquement pour un ordinateur particulier. Un utilisateur ne peut pas enregistrer un signet, puis l’envoyer à un autre utilisateur pour le lire sur un autre ordinateur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BookmarkOnClose**](bookmarkonclose-property.md)
</dt> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



