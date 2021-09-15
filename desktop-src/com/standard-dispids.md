---
title: DISPID standard
description: Un certain nombre de DISPID standard ont été définis pour la spécification de contrôles.
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657a7cd12ac92504bb5d63dcd486b6a45da47310
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404597"
---
# <a name="standard-dispids"></a>DISPID standard

Un certain nombre de DISPID standard ont été définis pour la spécification de contrôles.

## <a name="dispid_mousepointer"></a>DISPID, \_ MOUSEPOINTER

Propriété de type entier.

``` syntax
#define DISPID_MOUSEPOINTER            -521
```

La propriété MousePointer identifie les icônes de souris standard.



| Valeur         | Description                                                                |
|---------------|----------------------------------------------------------------------------|
| 0<br/>  | Valeurs Forme déterminée par l’objet.<br/>                       |
| 1<br/>  | Flèche<br/>                                                           |
| 2<br/>  | Croix (pointeur réticule)<br/>                                      |
| 3<br/>  | Poutre<br/>                                                          |
| 4<br/>  | Icône (petit carré dans un carré)<br/>                             |
| 5<br/>  | Taille (flèche à quatre branches pointant vers le Nord, le sud, l’est et l’Ouest)<br/> |
| 6<br/>  | Taille ne pas de SW (double flèche pointant vers le nord-est et sud-ouest)<br/>      |
| 7<br/>  | Taille N S (double flèche pointant vers le Nord et le sud)<br/>                |
| 8<br/>  | Taille NW, SE<br/>                                                     |
| 9<br/>  | Taille E W (double flèche pointant vers l’est et Ouest)<br/>                  |
| 10<br/> | Flèche haut<br/>                                                        |
| 11<br/> | Sablier (attente)<br/>                                                |
| 12<br/> | Aucune suppression<br/>                                                         |
| 13<br/> | Flèche et sablier<br/>                                             |
| 14<br/> | Flèche et point d’interrogation<br/>                                         |
| 15<br/> | Ajuster la taille<br/>                                                        |
| 99<br/> | Icône personnalisée spécifiée par la propriété MouseIcon<br/>                 |



 

## <a name="dispid_mouseicon"></a>DISPID \_ MOUSEICON

Propriété de type image.

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a>\_image DISPID

Propriété de type image.

``` syntax
#define DISPID_PICTURE                 -523
```

## <a name="dispid_valid"></a>DISPID \_ valide

Utilisé pour déterminer si le contrôle a ou non des données valides.

Propriété de type BOOL.

``` syntax
#define DISPID_VALID                   -524
```

## <a name="dispid_-ambient_palette"></a>\_palette ambiante \_ DISPID

Utilisé pour permettre au contrôle d’accéder au HPAL du conteneur. Si le conteneur fournit une palette ambiante, il s’agit de la seule palette qui peut être réalisée au premier plan. Les contrôles qui veulent réaliser leurs propres palettes doivent le faire en arrière-plan. Si aucune palette ambiante n’est fournie par le conteneur, le contrôle actif peut réaliser sa palette au premier plan. la gestion de palette est également décrite dans comportement de la palette pour les contrôles OLE qui se trouvent dans le kit de développement logiciel (SDK) ActiveX.

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





