---
description: Représente des informations sur les fonctionnalités de l’imprimante.
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: Structure PRINTPROCESSOR_CAPS_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_2
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3425f9477b153721980e3bb44b919b0baea37aa645caea6a3ee328a9ff923eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824730"
---
# <a name="printprocessor_caps_2-structure"></a>\_Structure PRINTPROCESSOR Cap \_ 2

Représente des informations sur les fonctionnalités de l’imprimante.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTPROCESSOR_CAPS_2 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
  DWORD dwNupDirectionCaps;
  DWORD dwNupBorderCaps;
  DWORD dwBookletHandlingCaps;
  DWORD dwDuplexHandlingCaps;
  DWORD dwScalingCaps;
} PRINTPROCESSOR_CAPS_2, *PPRINTPROCESSOR_CAPS_2;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwLevel**
</dt> <dd>

Valeur qui indique le numéro de version de la structure.

</dd> <dt>

**dwNupOptions**
</dt> <dd>

Masque de bits représentant les différents nombres de pages de document que l’imprimante peut imprimer sur un seul côté d’une feuille physique. Le bit le moins significatif représente une page de document par côté, le bit suivant représente 2 pages de document par côté, et ainsi de suite. Par exemple, 0x0000810B indique que l’imprimante prend en charge les pages de documents 1, 2, 4, 9 et 16 par côté physique.

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

Valeur d’indicateur qui indique l’ordre dans lequel les pages seront imprimées. Il peut s’agir d’une **\_ impression normale**, d’une **\_ impression inversée** ou d’un **livret \_ imprimé**.

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

Nombre maximal de copies que l’imprimante peut gérer.

</dd> <dt>

**dwNupDirectionCaps**
</dt> <dd>

Les modèles disponibles lorsque plusieurs pages de document sont imprimées sur le même côté d’une feuille de papier. Les indicateurs possibles sont les suivants :



| Valeur                     | Signification                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| PPCAPS \_ \_ vers la droite, puis \_ vers le PG. | Les pages apparaissent dans des lignes de droite à gauche, chaque ligne suivante sous son prédécesseur.                 |
| PPCAPS \_ vers le \_ droite, puis vers la \_ droite | Les pages apparaissent dans des colonnes de haut en bas, chaque colonne suivante à droite de son prédécesseur. |
| PPCAPS à gauche et à \_ droite \_ \_  | Les pages apparaissent dans des lignes de gauche à droite, chaque ligne suivante sous son prédécesseur.                 |
| PPCAPS \_ \_ , puis \_ gauche  | Les pages apparaissent dans des colonnes de haut en bas, chaque colonne suivante à gauche de son prédécesseur.  |



 

</dd> <dt>

**dwNupBorderCaps**
</dt> <dd>

Peut être uniquement imprimé PPCAPS \_ Border \_ , ce qui indique que lorsque plusieurs pages de document sont imprimées sur un seul côté d’une feuille physique, l’imprimante peut être informée de l’impression ou non d’une bordure autour de la zone imageable de chaque page de document.

</dd> <dt>

**dwBookletHandlingCaps**
</dt> <dd>

Peut uniquement être \_ un bord de livret PPCAPS \_ , indiquant que l’imprimante peut imprimer le style de livret.

</dd> <dt>**dwDuplexHandlingCaps**</dt> <dd> 

| Valeur                                         | Signification                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PPCAPS \_ les pages inversées \_ \_ pour le \_ \_ duplex inversé  | Lors de l’impression dans l’ordre inverse et le duplexage, le processeur peut imprimer l’ordre de chaque paire de pages. par conséquent, au lieu d’imprimer dans l’ordre 4, 3, 2, 1, il s’imprimera dans l’ordre 3, 4, 1, 2.                                                                                                       |
| PPCAPS ne pas \_ \_ Envoyer \_ \_ de pages supplémentaires \_ pour le \_ duplex | Lors du duplexage, le processeur d’impression peut être invité à ne pas envoyer de page supplémentaire lorsqu’il existe un nombre impair de pages de document. Le processeur honorera la valeur le mieux possible, mais dans les cas où la prévention d’une page vierge supplémentaire entraînerait une sortie incorrecte, les pages supplémentaires seront peut-être encore envoyées. |



 

</dd> <dt>

**dwScalingCaps**
</dt> <dd>

Peut uniquement être PPCAPS de mise à l’échelle \_ carrée \_ , ce qui indique que l’imprimante peut mettre à l’échelle l’image de page.

</dd> </dl>

## <a name="remarks"></a>Remarques

les valeurs de tous les membres de structure sont fournies par la fonction **GetPrintProcessorCapabilities** , qui est documentée dans le Kit de pilotes Windows.

Quand une application appelle [**GetPrinterData**](getprinterdata.md), le spouleur appelle la fonction **GetPrintProcessorCapabilities** d’un processeur d’impression et spécifie un nom de valeur qui a un format _de type de_ données **PrintProcCaps \_**, où *DataType* est le nom d’un type de données d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

 




