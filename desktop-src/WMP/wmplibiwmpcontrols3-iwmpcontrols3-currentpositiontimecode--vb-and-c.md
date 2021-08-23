---
title: IWMPControls3 propriété currentPositionTimecode
description: La propriété currentPositionTimecode obtient ou définit la position actuelle dans l’élément multimédia actuel à l’aide d’un format de code d’heure. Cette propriété prend actuellement en charge le code de temps SMPTE.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- Lecteur Windows Media de la propriété currentPositionTimecode
- Lecteur Windows Media de la propriété currentPositionTimecode, interface IWMPControls3
- Lecteur Windows Media de l’interface IWMPControls3, propriété currentPositionTimecode
topic_type:
- apiref
api_name:
- IWMPControls3.currentPositionTimecode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b91c00c166050f4f3a3bc05861fa92d4fb66efcfa139e726c7cc799e21623fa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760919"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a>IWMPControls3 :: currentPositionTimecode, propriété

La propriété **currentPositionTimecode** obtient ou définit la position actuelle dans l’élément multimédia actuel à l’aide d’un format de code d’heure. Cette propriété prend actuellement en charge le code de temps SMPTE.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a>Valeur de la propriété

**System. String** qui est le code de temps SMPTE.

## <a name="remarks"></a>Remarques

Le code temporel SMPTE offre un moyen standard d’identifier une image vidéo individuelle, ce qui est utile pour synchroniser la lecture. si un fichier multimédia numérique prend en charge le code temporel SMPTE, Lecteur Windows Media pouvez récupérer les informations de position du code d’heure actuelles ou rechercher une image vidéo identifiée par un code de temps particulier.

Le code temporel SMPTE identifie une trame particulière en fonction du nombre d’heures, de minutes, de secondes et de frames qui le séparent d’une trame de référence particulière. En règle générale, la trame de temps zéro est le début du fichier et une valeur de code temporel SMPTE particulière représente le temps écoulé depuis le début du fichier.

Le code d’heure est au format \[  \] *hh*:*mm*:*SS*.*FF* où \[ *Range* \] représente la plage, HH représente les heures, *mm* représente les minutes, *SS* représente les secondes et *FF* représente les images. Lorsque vous définissez une valeur pour **currentPositionTimecode**, vous devez inclure les huit chiffres, en utilisant des zéros comme espaces réservés.

\[*plage* \] correspond au membre **wRange** de la structure de données d' **\_ EXTENSION du \_ code \_ temporel WMT** Windows Media Format. pour plus d’informations sur les plages de codes de temps, consultez le kit de développement logiciel (SDK) Windows Media Format.

La définition et l’obtention de **currentPositionTimecode** sont prises en charge uniquement pour les fichiers qui contiennent des informations de code de temps SMPTE.

## <a name="examples"></a>Exemples

L’exemple de code suivant spécifie **currentPositionTimecode** comme 1 heure, zéro minute, 30 secondes et 5 frames. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
// so that you can use the currentPositionTimecode property.
WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

// Seek to a frame using SMPTE time code.
controls.currentPositionTimecode = "[00000]01:00:30.05";
```


```VB

' Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
&#39; so that you can use the currentPositionTimecode property.
Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

&#39; Seek to a frame using SMPTE time code.
Controls.currentPositionTimecode = &quot;[00000]01:00:30.05&quot;
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPControls3 (VB et C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





