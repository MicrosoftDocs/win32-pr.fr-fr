---
description: La méthode ShowMenu affiche le menu spécifié à l’écran.
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: Méthode ShowMenu
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb9135e2999675dc46774f15ee79afd835085b40fe210d0ca1cfd173f8a99fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050509"
---
# <a name="showmenu-method"></a>Méthode ShowMenu

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `ShowMenu` méthode affiche le menu spécifié à l’écran.

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*
</dt> <dd>

Spécifie l’ID de menu en tant qu’entier.



| Valeur | Description |
|-------|-------------|
| 2     | Titre (haut) |
| 3     | Root        |
| 4     | Sous-titres  |
| 5     | Audio       |
| 6     | Angle       |
| 7     | Chapitre     |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Les noms de menu DVD peuvent être un peu confus. Le menu du titre est un autre nom pour le menu Gestionnaire vidéo, le menu principal de l’ensemble du disque. Elle répertorie généralement tous les jeux de titres vidéo disponibles sur le disque. Le menu racine est le menu d’un jeu de titres vidéo, qui peut contenir un titre ou un groupe de titres. Tous les titres d’un jeu de titres partagent les mêmes menus de sous-image, audio et d’angle.

 

 



