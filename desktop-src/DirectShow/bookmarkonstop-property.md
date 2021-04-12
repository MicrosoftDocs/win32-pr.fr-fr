---
description: La propriété DVDAdm. BookmarkOnStop définit ou récupère une valeur qui indique à l’objet MSWebDVD s’il faut enregistrer automatiquement un signet de l’emplacement et des paramètres actuels lorsque l’utilisateur clique sur le bouton arrêter.
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: Propriété BookmarkOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355ae01c43ef28a086c76f4716fe3d46d250fbe4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109538"
---
# <a name="bookmarkonstop-property"></a>Propriété BookmarkOnStop

La `DVDAdm.BookmarkOnStop` propriété définit ou récupère une valeur qui indique à l’objet mswebdvd s’il faut enregistrer automatiquement un signet de l’emplacement et des paramètres actuels lorsque l’utilisateur clique sur le bouton **arrêter** .

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur booléenne indiquant si l’objet MSDVDAdm enregistre un signet de tous les paramètres DVD, y compris la position sur le disque, le niveau parental et le pays/région parent.

## <a name="remarks"></a>Notes

Cette propriété est en lecture/écriture et sa valeur par défaut est false.

Les signets sont valides uniquement pour un ordinateur particulier. Un utilisateur ne peut pas enregistrer un signet, puis l’envoyer à un autre utilisateur pour le lire sur un autre ordinateur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BookmarkOnClose**](bookmarkonclose-property.md)
</dt> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



